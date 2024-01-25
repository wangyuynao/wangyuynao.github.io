---
title: astrometry
top: false
cover: false
toc: true
mathjax: true
date: 2021-02-12 05:34:59
tags:
- astrometry.net
categories:
- Photometry
---

# 安装Astrometry.net

[官方教程](https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/Anaconda3-2019.10-Linux-x86_64.sh)

<!--more-->

## 系统准备

>yum install出现Loaded plugins: fastestmirror, langpacks
>
>1、修改插件配置文件
>
>`vi /etc/yum/pluginconf.d/fastestmirror.conf`
>
>将`enable=1`改为`enable=0`
>
>2、修改yum配置文件
>
>`# vi /etc/yum.conf`
>
>将`plugins=1`改为`plugins=0`
>
>然后`yum clean all` `yum makecache`

* GNU build tools 

```
sudo yum install cairo-1.15.12-4 cairo-devel-1.15.12-4 libpng-1.5.13-7 libpng-devel-1.5.13-7 libjpeg-turbo-1.2.90-8 libjpeg-turbo-devel-1.2.90-8 zlib-1.2.7-18 zlib-devel-1.2.7-18 bzip2-libs-1.0.6-13 bzip2-devel-1.0.6-13 python-2.7.5-86 numpy-1.7.1-13
```

* Python 3

```
sudo yum -y install python3 python3-devel python3-pip
sudo pip3 install numpy
sudo pip3 install astropy
```

* NetPBM

```
sudo yum -y install netpbm netpbm-devel netpbm-progs
```

* pyfits and cfitsio

```
sudo yum -y install epel-release
sudo yum -y install pyfits pyfits-tools cfitsio cfitsio-devel
```

* 安装g++ gcc

```
sudo yum -y install gcc gcc-c++ kernel-devel
```



## Building astrometry.net

```
wget http://astrometry.net/downloads/astrometry.net-0.80.tar.gz
tar zxvf astrometry.net-0.80.tar.gz
cd astrometry.net-0.80/util/
# Edit 'makefile.netpbm'
# NETPBM_INC ?= -I/usr/include/netpbm
# NETPBM_LIB ?= -L/usr/lib64 -lnetpbm

cd ..
make
make py
make extra
sudo make install

#配置环境变量
export PATH=${PATH}:/usr/local/astrometry/bin
```

