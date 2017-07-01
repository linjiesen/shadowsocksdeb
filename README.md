# debian install shadowsocks-qt5 client

在 https://github.com/shadowsocks/shadowsocks-qt5/wiki 中没有debian的安装方法，所以Google了一下，
先安装依赖包

> apt-get -y install qt5-qmake qtbase5-dev libbotan1.10-dev pkg-config debhelper libqrencode-dev libzbar-dev libappindicator-dev


git clone shadowsocks依赖

```
 git clone https://github.com/shadowsocks/libQtShadowsocks.git
 cd libQtShadowsocks/
 dpkg-buildpackage -uc -us -b              //打包的文件在当前目录的父目录里
 dpkg -i ../libqtshadowsocks_1.10.0-1_amd64.deb ../libqtshadowsocks-dev_1.10.0-1_amd64.deb
```

git clone shadowsocks-qt5项目

```
 git clone https://github.com/shadowsocks/shadowsocks-qt5.git
 cd shadowsocks-qt5/
 dpkg-buildpackage -uc -us -b
 dpkg -i ../shadowsocks-qt5_2.8.0-1_amd64.deb
```

> sudo dpkg -i shadowsocks-qt5_2.8.0-1_amd64.deb
