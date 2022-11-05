### ARM机可用
自用魔改一键DD脚本，仅支持密钥登录，SSH端口22345<br>
```
bash <(curl -k https://raw.githubusercontent.com/daoke123/ssh/main/dddebian.sh) 
```
```
默认为Debian11，下参数可手动调整
--version 10
默认64位系统，下参数可指定为ARM
--architecture arm64
默认为Debian的CDN源，下参数可指定为清华源，加快下载速度
--china
指定apt源地址
--mirror-host ftp.hk.debian.org
大陆源
--mirror 'http://mirrors.ustc.edu.cn/debian/'
香港源
--mirror 'http://ftp.hk.debian.org/debian/'
台湾源
--mirror 'http://ftp.tw.debian.org/debian/'
日本源
--mirror 'http://ftp.jp.debian.org/debian/'
韩国
--mirror 'http://ftp.kr.debian.org/debian/'
新加坡
--mirror 'http://mirror.0x.sg/debian/'
俄罗斯
--mirror 'http://ftp.ru.debian.org/debian/'

指定网卡，貌似尚不支持，建议在 preed.cfg 里手动添加 d-i netcfg/choose_interface select ens4
```


### 免密登录，公钥换成自己的
```
mkdir /root/.ssh;echo "ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEA5qK3fDbxZshKP3MbQo4xm1YNmTQsHcapbF8wAXJJcCgxtzujH9QuFCeQzsQ3QET2qZgG1k0GfTV6slRdrJJeI8fdwFgRc28JEhXh4rGx8MUdotJh8eVAnygWATBtet2Au5gpn3s3s44XqgnWXY+bRGJ6WoB58/3fjPG1YZIR5wh9knNxRt/9VO8YCTBqQP3z5hdPuNldx3jgIuFNhcI1qBVnQZ2czC2Zv8sHDDuiuNoaomKsg7LgbhKPnvRfEGb+yZaU/KKwbEJwbFcZkT7QiW90OhYVKT2+K8xEsUpR4ocH+SxgvFrpyKAXkSqF/Wwe32baAlzrNwucLdsS+jBk3w== OpenSSH-rsa-import-061520" >>/root/.ssh/authorized_keys

```
