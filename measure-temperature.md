# 给Jetson安装温度监控

1. 先进行软件更新`sudo apt update`
2. 安装对应的软件`sudo apt install lm-sensors`
3. 开启软件检测`sudo sensors-detect`
4. 开启软件`sensors`
5. 安装图形化显示的界面`sudo apt install psensor`