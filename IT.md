# JetsonNano 安装 TensorFlow的教程
首先

在终端输入
`sudo nano ~/.bashrc`

在末尾加上:
```
export PATH=/usr/local/cuda-10.0/bin:$PATH
export LD_LIBRARY_PATH=/usr/local/cuda/lib64:$LD_LIBRARY_PATH
export CUDA_HOME=$CUDA_HOME:/usr/local/cuda-10.0
```
` Ctrl+o`保存后`Ctrl+x`退出

`source ~/.bashrc`重载设置

输入`nvcc -V`

如输出CUDA版本信息正确，添加变量完成

依次输入以下三条命令：
```
sudo apt install python3 python3-pip python3-dev
python3 -m pip install --upgrade pip
sudo nano /usr/bin/pip3
```

进入nano编辑器后，将文件更改为:
```
from pip import __main__
if __name__ == '__main__':
    sys.exit(__main__._main())
```

最后，依次输入：
```
sudo apt-get install libhdf5-serial-dev hdf5-tools
sudo pip3 install --pre --extra-index-url https://developer.download.nvidia.com/compute/redist/jp/v42 tensorflow-gpu
```
