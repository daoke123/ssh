<font size="5"><strong>网络重装脚本</strong></font><br />
<font color="Red">PS：自定义密码直接 -p 你想要的密码就行！！！</font><br />
部分机器需要设置网卡，否则可以VNC，但是不能远程SSH<br />
<div class="blockcode"><div id="code_qr1"><ol><li>-firmware&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 额外的驱动支持<br />
<li>-d&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Debian系统 后面是系统版本号<br />
<li>-c&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Centos系统 后面是系统版本号<br />
<li>-v &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 后面写64位 32位<br />
<li>-a&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 不清楚这个干啥的但是每个脚本都带<br />
<li>--mirror&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 后面是镜像源地址<br />
<li>-p&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 后面写自定义密码<br />
<li>–ip-addr &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; ifconfig -a 后获取到的 例：194.87.xxx.xxx<br />
<li>–ip-gate &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; route -n&nbsp; &nbsp; 后获取到的 例&nbsp; &nbsp;194.87.xxx.xxx<br />
<li>–ip-mask &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; 255.255.xxx.xx</ol></div><em onclick="copycode($('code_qr1'));">复制代码</em></div><br />

<br />
· 甲骨文、三毛、Vir、RN等大部分VPS通用，<font color="Red">支持ARM、AMD</font><br />
<div class="blockcode"><div id="code_Pdm"><ol><li>bash &lt;(wget --no-check-certificate -qO- 'https://moeclub.org/attachment/LinuxShell/InstallNET.sh') -d 11 -v 64 -a -firmware -p 自定义密码</ol></div><em onclick="copycode($('code_Pdm'));">复制代码</em></div><br />
· gcore （<font color="Red">优先使用上面那个脚本</font>，如果不行再使用这个，这家我没用过）<br />
<div class="blockcode"><div id="code_a8Y"><ol><li>wget git.io/auto.sh<br />
<li>bash auto.sh -d 9 -v 64 -a -p 密码</ol></div><em onclick="copycode($('code_a8Y'));">复制代码</em></div><br />
· 国内VPS需要更换镜像源否则很慢！我这里使用的华为源，如果你是腾讯云后面可以换成内网源，节省流量，下面有写！<br />
<div class="blockcode"><div id="code_hO9"><ol><li>bash &lt;(wget --no-check-certificate -qO- 'https://moeclub.org/attachment/LinuxShell/InstallNET.sh') -d 11 -v 64 -a --mirror 'https://mirrors.huaweicloud.com/debian/' -p 自定义密码</ol></div><em onclick="copycode($('code_hO9'));">复制代码</em></div><br />
镜像站地址<br />
官方给出的地址列表：https://www.debian.org/mirror/list<br />
<div class="blockcode"><div id="code_fND"><ol><li>一些国内的<br />
<li>ftp.cn.debian.org<br />
<li>mirror.bjtu.edu.cn<br />
<li>mirror.lzu.edu.cn&nbsp; &nbsp; &nbsp; &nbsp; <br />
<li>mirror.nju.edu.cn&nbsp; &nbsp; &nbsp; &nbsp; <br />
<li>mirrors.163.com&nbsp; &nbsp; &nbsp; &nbsp; <br />
<li>mirrors.bfsu.edu.cn&nbsp; &nbsp; &nbsp; &nbsp; <br />
<li>mirrors.hit.edu.cn&nbsp; &nbsp; &nbsp; &nbsp; <br />
<li>mirrors.huaweicloud.com&nbsp; &nbsp; &nbsp; &nbsp; <br />
<li>mirror.sjtu.edu.cn&nbsp; &nbsp; &nbsp; &nbsp; <br />
<li>mirrors.tuna.tsinghua.edu.cn&nbsp; &nbsp; &nbsp; &nbsp; <br />
<li>mirrors.ustc.edu.cn&nbsp; &nbsp; &nbsp; &nbsp; <br />
<li><br />
<li>使用方法：（大致都是一样的）<br />
<li><br />
<li>清华源<br />
<li>--mirror 'https://mirrors.ustc.edu.cn/debian/'<br />
<li>腾讯源<br />
<li>--mirror 'http://mirrors.tencent.com/debian/'<br />
<li>--mirror 'http://mirrors.cloud.tencent.com/debian/'<br />
<li>腾讯源内网（dd完毕后可以修改 走内网不费额外流量）<br />
<li>http://mirrors.tencentyun.com/<br />
<li>阿里源<br />
<li>--mirror 'https://mirrors.aliyun.com/debian/'<br />
<li>华为源<br />
<li>--mirror 'https://mirrors.huaweicloud.com/debian/'</ol></div><em onclick="copycode($('code_fND'));">复制代码</em></div><br />

<br />
· DD windows<br />
<div class="blockcode"><div id="code_Dkb"><ol><li>wget --no-check-certificate -qO InstallNET.sh 'https://moeclub.org/attachment/LinuxShell/InstallNET.sh' &amp;&amp; bash InstallNET.sh -dd 'http://d.nat.ee/win/lite/win7-ent-sp1-x64-cn/win7-ent-sp1-x64-cn.vhd.gz'</ol></div><em onclick="copycode($('code_Dkb'));">复制代码</em></div><br />
后面的链接为windows系统直链 可以去 dd.nat.ee 下载 感谢 @nat.ee&nbsp;&nbsp;大佬 <a href="https://hostloc.com/forum.php?mod=viewthread&amp;tid=921383" target="_blank">大佬文章地址 新增LTSC 2021</a><br />
<br />
<br />
· 带 WebUI 可查看进度的<br />
<div class="blockcode"><div id="code_Mm5"><ol><li>https://raw.githubusercontent.com/flyqie/dd-shell/master/Core_Install.sh</ol></div><em onclick="copycode($('code_Mm5'));">复制代码</em></div><br />
国内机可使用<br />
<div class="blockcode"><div id="code_WgB"><ol><li>https://ghproxy.com/https://raw.githubusercontent.com/flyqie/dd-shell/master/Core_Install.sh</ol></div><em onclick="copycode($('code_WgB'));">复制代码</em></div><br />
感谢 @flyqie&nbsp;&nbsp;大佬 <a href="https://hostloc.com/forum.php?mod=viewthread&amp;tid=921407" target="_blank">原帖地址</a><br />
<br />
<br />
<br />
<font size="5"><strong>宝塔面板&amp;AApanel</strong></font><br />
<br />
Debian系统<br />
<div class="blockcode"><div id="code_rjm"><ol><li># 宝塔<br />
<li>wget -O install.sh http://download.bt.cn/install/install-ubuntu_6.0.sh &amp;&amp; bash install.sh<br />
<li><br />
<li># aapanel<br />
<li>wget -O install.sh http://www.aapanel.com/script/install-ubuntu_6.0_en.sh &amp;&amp; bash install.sh</ol></div><em onclick="copycode($('code_rjm'));">复制代码</em></div><br />

<br />
有次无聊看了看文件发现aapanel就是宝塔的换皮，语言换成了英语，所以破解方法一样。<br />
<div class="blockcode"><div id="code_k1E"><ol><li># 宝塔去实名认证<br />
<li>rm -rf /www/server/panel/data/bind.pl<br />
<li><br />
<li># 宝塔&amp;aapanel破解<br />
<li>编辑 /www/server/panel/class/panelplugin.py<br />
<li>找到 softList['list'] = tmpList 这行代码<br />
<li>在下面添加以下代码，注意缩进<br />
<li><br />
<li>softList['pro'] = 1<br />
<li>for soft in softList['list']:<br />
<li>soft['endtime'] = 0<br />
<li><br />
<li>修改宝塔标识（企业版ltd、专业版pro）<br />
<li>编辑 /www/server/panel/data/plugin.json<br />
<li>搜索 &quot;pro&quot;: 把后面的-1 改为0 即可<br />
<li>编辑完毕后保存重启面板即可</ol></div><em onclick="copycode($('code_k1E'));">复制代码</em></div><br />

<br />
<font size="5"><strong>常用脚本</strong></font><br />
<br />
一键开启BBR（适用于<font color="Red">较新</font>的Debian、Ubuntu）<br />
<div class="blockcode"><div id="code_GhK"><ol><li>echo &quot;net.core.default_qdisc=fq&quot; &gt;&gt; /etc/sysctl.conf<br />
<li>echo &quot;net.ipv4.tcp_congestion_control=bbr&quot; &gt;&gt; /etc/sysctl.conf<br />
<li>sysctl -p<br />
<li>sysctl net.ipv4.tcp_available_congestion_control<br />
<li>lsmod | grep bbr</ol></div><em onclick="copycode($('code_GhK'));">复制代码</em></div><br />

<br />
superbench<br />
<div class="blockcode"><div id="code_IhY"><ol><li>wget -qO- git.io/superbench.sh | bash</ol></div><em onclick="copycode($('code_IhY'));">复制代码</em></div><br />

<br />
Bench.sh<br />
<div class="blockcode"><div id="code_PW6"><ol><li>wget -qO- bench.sh | bash</ol></div><em onclick="copycode($('code_PW6'));">复制代码</em></div><br />

<br />
三网测速<br />
<div class="blockcode"><div id="code_XlJ"><ol><li>bash &lt;(curl -Lso- http://yun.789888.xyz/speedtest.sh)</ol></div><em onclick="copycode($('code_XlJ'));">复制代码</em></div><br />

<br />
流媒体<br />
<div class="blockcode"><div id="code_Jy3"><ol><li>#第一个<br />
<li>bash &lt;(curl -L -s https://raw.githubusercontent.com/lmc999/RegionRestrictionCheck/main/check.sh)<br />
<li><br />
<li># 第二个<br />
<li>bash &lt;(curl -sSL &quot;https://github.com/CoiaPrant/MediaUnlock_Test/raw/main/check.sh&quot;)</ol></div><em onclick="copycode($('code_Jy3'));">复制代码</em></div><br />

<br />
回程<br />
<div class="blockcode"><div id="code_RmM"><ol><li># 第一个<br />
<li>wget https://raw.githubusercontent.com/nanqinlang-script/testrace/master/testrace.sh<br />
<li>bash testrace.sh<br />
<li><br />
<li># 第二个<br />
<li>wget -qO- git.io/besttrace | bash<br />
<li><br />
<li># 第三个<br />
<li>curl http://tutu.ovh/bash/returnroute/test.sh | bash</ol></div><em onclick="copycode($('code_RmM'));">复制代码</em></div><br />

<br />
yabs 机器跑分<br />
<div class="blockcode"><div id="code_Z6I"><ol><li>curl -sL yabs.sh | bash</ol></div><em onclick="copycode($('code_Z6I'));">复制代码</em></div><br />

<br />
一件安装docker<br />
国外机<br />
<div class="blockcode"><div id="code_toP"><ol><li>curl -sSL https://get.docker.com/ | sh</ol></div><em onclick="copycode($('code_toP'));">复制代码</em></div><br />
国内机<br />
<div class="blockcode"><div id="code_aH8"><ol><li>curl -sSL https://get.daocloud.io/docker | sh</ol></div><em onclick="copycode($('code_aH8'));">复制代码</em></div><br />
卸载docker<br />
<div class="blockcode"><div id="code_OEJ"><ol><li>sudo apt-get remove docker docker-engine<br />
<li>rm -fr /var/lib/docker/</ol></div><em onclick="copycode($('code_OEJ'));">复制代码</em></div><br />
安装docker-compose<br />
国外机<br />
<div class="blockcode"><div id="code_q28"><ol><li>sudo curl -L &quot;https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)&quot; -o /usr/local/bin/docker-compose<br />
<li>sudo chmod +x /usr/local/bin/docker-compose</ol></div><em onclick="copycode($('code_q28'));">复制代码</em></div><br />
国内机<br />
<div class="blockcode"><div id="code_WCc"><ol><li>curl -L https://get.daocloud.io/docker/compose/releases/download/v2.1.1/docker-compose-`uname -s`-`uname -m` &gt; /usr/local/bin/docker-compose<br />
<li>chmod +x /usr/local/bin/docker-compose</ol></div><em onclick="copycode($('code_WCc'));">复制代码</em></div></td></tr></table>
