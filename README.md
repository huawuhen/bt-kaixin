# 前言
宝塔面板自7.8开始，违背了宝塔开源协议，竟然在免费版的源码里面加入了加密的授权验证模块。除此之外，7.8版本使用各种方法均无法绕过面板强制绑定账号，如果不绑定账号插件就无法下载。

安装前，请先部署环境后再重新安装（此处以Debian系统为例，其他系统参照）
```
apt update -y && apt dist-upgrade -y && apt install -y curl && apt install ufw -y && apt install -y socat 
apt-get install -y xz-utils openssl gawk file wget screen && screen -S os
```

## 开心版系列
开心版11.6
```
wget -O install.sh https://raw.githubusercontent.com/huawuhen/bt-kaixin/main/install-11.6.sh && bash install.sh
```
开心版11.0
```
curl -sSO https://raw.githubusercontent.com/huawuhen/bt-kaixin/main/install_latest.sh && bash install_latest.sh
```
开心版8.0
```
wget -O install.sh https://raw.githubusercontent.com/huawuhen/bt-kaixin/main/install-8.sh && bash install.sh
```
开心版7.7
```
curl -sSO https://raw.githubusercontent.com/huawuhen/bt-kaixin/main/one_key_happy.sh && bash one_key_happy.sh
```

### 升级到14
```
curl https://io.bt.sb/install/update_panel.sh|bash -s -- 11.4.1
```

## 其他
开心版安装完成后使用 bt 命令可能出现报错，只需要将终端设置为中文语言即可。（可以查阅LocaleCN.sh文件中对应系统的修改命令，先备份好原始文件，然后使用该命令修改语言并重启，尝试 bt 命令正常后，再恢复原有语言文件。这样做的目的是因为在后期使用时个别程序会因为语言不一致，而导致程序无法正常运行。）
更改SSH终端中文语言
```
wget -N --no-check-certificate https://raw.githubusercontent.com/huawuhen/bt-kaixin/main/LocaleCN.sh && bash LocaleCN.sh
```

- [baotsbs](https://baota.sbs/)
- [btsb](https://bt.sb/bbs/forum-37-1.html)