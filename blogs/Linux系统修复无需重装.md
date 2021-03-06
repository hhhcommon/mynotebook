
## Linux 系统修复，无需重装
前几天，我的Xubuntu系统无法重起，开机进入 `emergency mode`：
![emergency mode](https://s2.ax1x.com/2019/01/31/k1Bdbt.jpg)
```
You are in emergency mode. After logging in, type "journalctl -xb" to view system logs, "systemctl reboot" to reboot, "systemctl default" or "exit" to boot into default mode.
```
`system logs` 显示：
```
A TPM error (6) occurred attempting to read a pcr value.
......
1-1-port3: unable to enumerate USB device
......
```
![error: read a pcr value](https://s2.ax1x.com/2019/01/31/k1tI6x.jpg)
![logs](https://s2.ax1x.com/2019/01/31/k1t4pR.md.jpg)
就试着修复系统，在网上搜到一个办法，但是没有成功，也记在这里：
> 开机按`ThinkVantag`键，进入`BIOS`的`security chip`里面，选择`activate`或`disable`

#### 最后我是这样修复的：

制作一个 USB LiveCD启动盘，用启动盘中的 `Ubuntu`系统启动，然后依次操作：
+ 在外部存储器备份自己的重要数据，以防这个办法失败后，重要数据丢失。
+ 依次输入以下命令：

```
sudo apt-get update && sudo apt-get upgrade -y
sudo rm /var/lib/apt/lists/lock
sudo rm /var/lib/dpkg/lock
sudo rm /var/lib/dpkg/lock-frontend
sudo dpkg --configure -a
sudo apt clean
sudo apt-get update --fix-missing
sudo apt install -f
sudo dpkg --configure -a
sudo apt-get upgrade
```
+ 然后， `sudo reboot` 重启。
Eenjoy it!