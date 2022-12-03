### 脚本会安装最新的Alpine Linux，并会清除服务器数据，请先备份好数据
`wget https://raw.githubusercontent.com/daoke123/ssh/main/alpine.sh && bash alpine.sh`
### ARM机可用
自用魔改一键DD脚本，仅支持密钥登录，SSH端口22345<br>
```
bash <(curl -k https://raw.githubusercontent.com/daoke123/ssh/main/InstallNET.sh) -d 10 -v 64 -a
```
-d 10 为Debian 10<br>
-v 为64位系统<br>
-a 自动运行，无需在VNC里手动操作(理想情况下)<br>
-i 指定网卡，多网卡的时候需要指定，单网卡可以忽略<br>
--mirror 指定源，同地区的源装系统会更快，默认是美国源，下方为Debian源<br>
```

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
