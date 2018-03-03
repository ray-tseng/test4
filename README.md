# HappyNewYear-Ai

# 環境部屬
#安裝Anaconda
wget https://repo.continuum.io/archive/Anaconda3-5.0.1-Linux-x86_64.sh
bash Anaconda3-5.0.1-Linux-x86_64.sh
export PATH="$HOME/Anaconda3/bin:$PATH"

#建立virtualenv
conda create -n HappyNewYear python=3.5
source activate HappyNewYear

#安裝package 
conda install -c https://conda.anaconda.org/menpo opencv3
conda install -c conda-forge tensorflow
conda install jupyter
conda install libiconv
conda install pyqt=4
conda install pillow
pip install keras
sudo apt update
sudo apt-get install libgtk2.0-0
pip install -r requirements.txt

#調整Keras參數
vi ~/.keras/keras.json   #開啟此檔
channels_last 改成 channels_first  

#(可選)設定jupyter 
jupyter-notebook --generate-config
jupyter notebook password
jupyter notebook --ip=0.0.0.0 --port=8888

# 啟動程式
#Streaming模式(影像從相機來)
run imageStreaming.py

#imageFile模式(影像從檔案來)
run imageFile.py

# 訓練模型
按照data/train中的格式，要分幾類就開幾個資料夾，Keras imageGenerator會自動檔把資料夾名稱當類別名稱