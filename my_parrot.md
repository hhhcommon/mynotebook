+ 更新源设置:
`$ vim /etc/apt/sources.list.d/parrot.list`
```
# 清华源：
deb https://mirrors.tuna.tsinghua.edu.cn/parrot/ parrot main contrib non-free
#deb-src https://mirrors.tuna.tsinghua.edu.cn/parrot/ parrot main contrib non-free
```

+ 匿名模式
AnonSurf（匿名模式）

Anonymous为全局tor代理（由于众所周知的原因，需要做一些前置设置，但有时候通过多次重新连接可以直连）

i2p为隐形网络计划（俗称大葱路由）
`i2prouter start`

> （i2p不能在Root身份下运行，但是Anonsurf需要sudo权限）
> 启动后会自动打开i2p控制台

torchat
> 一个通过Tor的隐藏服务实现点对点聊天的小程序，内容不受第三方的监视或过滤。Tor可以加密聊天内容，隐藏使用者的IP

GNUnet
> 一种用于匿名抗审查的文件共享P2P网络架构

onionshare
> 基于tor网络的匿名文件分享工具（使用参考http://www.freebuf.com/sectool/122910.html）

临时改变语言：
`$ LANG=en_US.UTF-8`
显示系统语言：
`echo $LANG`

安装软件：
`sudo apt-get install gimp virtualbox`

```
sudo apt-get install mongodb
sudo apt-get install flashplugin-nonfree 
```

`sudo apt-get install virtualbox-guest-x11`


`sudo apt-get install libssl-dev`
`apt-get install libcurl4-gnutls-dev`
`git clone git://github.com/gitster/git`
`cd git`
`make`
`make install`

+ 安装flash:
`sudo apt-get install pepperflashplugin-nonfree`
> 参考：https://askubuntu.com/questions/449103/chromium-34-and-later-cannot-detect-flash-plugin
Chromium 34 in the main repos have started using Aura (early), which does not include support for NPAPI (this is a planned phaseout of NPAPI in Chromium). Therefore, you need to use Pepper Flash to be able to use Flash.
Installing Flash
Ubuntu 14.04 (Trusty) and newer
If you have Trusty, you can just run sudo apt-get install pepperflashplugin-nonfree.
Ubuntu 12.04 (Precise) and newer
If you don't have Trusty, you can use this PPA to install Pepper Flash for any supported Ubuntu version above Precise. Run the following commands to add the PPA and install Pepper Flash:
sudo apt-add-repository ppa:skunk/pepper-flash
sudo apt-get update
sudo apt-get install pepflashplugin-installer
Note that you need to configure Chromium to use Pepper Flash. To do this, open /etc/chromium-browser/default and add the following line to the end of the file on a new line:
. /usr/lib/pepflashplugin-installer/pepflashplayer.sh
Close all windows and re-open.
Updating Pepper Flash (on Trusty)
You can run sudo update-pepperflashplugin-nonfree --status to see what version of Pepper Flash you have installed. If there is a newer version available, you can just run sudo update-pepperflashplugin-nonfree --install.



`sudo service stop postgresql`
`sudo /etc/init.d/postgresql restart`
`sudo -u postgres psql`
`\password myuser`
`\q`

msf: Database not connected


+ sudo apt-get remove ...
> dpkg 被中断，您必须手工运行 ‘sudo dpkg --configure -a’ 解决此问题。
`sudo dpkg --configure -a`

+ remove software
`sudo apt-get remove geany leafpad atom abiword gnumeric`

+ install
`sudo apt-get install chromium`
`sudo apt-get install gimp`
    + install xmind:
download xmind.zip
`mkdir xmind`
`mv xmind.zip /xmind`
`cd xmind`
`unzip xmind.zip`
`ln -s ./app/xmind/Xmind-amd64/ ./xmind`
    + `sudo apt-get install transmission`
    + `sudo apt-get install inkscape`




+ font size:
sudo vim /etc/default/locale
sudo apt-get install fcitx-table-wbpy
fcitx-m17n fcitx-tools kdebase-bin `plasma-widgets-kimpanel fcitx-table-all`
apt-get -u dist-upgrade

`mkfs.fat /dev/sda11`
> 9.1GB

