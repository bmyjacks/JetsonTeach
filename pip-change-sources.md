# 给python的pip更换软件源

1.更新软件列表并安装nano

```bash
sudo apt update -y && sudo apt install nano -y
```

2.使用命令更新到最新的pip

```bash
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple pip -U
```

3.使用以下命令切换软件源(pip >= 10.0.0)

```bash
pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
```

