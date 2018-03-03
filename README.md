# HappyNewYear-Ai

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
pip install -r requirements.txt

#設定jupyter 密碼
jupyter-notebook --generate-config
jupyter notebook password

#調整Keras參數


#最後run main.py啟動本範例PS:需要有攝影機的筆電
run main.py
