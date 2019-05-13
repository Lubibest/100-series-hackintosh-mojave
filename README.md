#Hackintosh
教程作者：Genius-lbesT 对本教程如有疑问，请添加QQ好友：2489050703

本教程制作为6代台式机CPU通用的安装及完善驱动。
AMD / NVDIA / INTEL均可通过EFI-for-install.zip安装到机器上
EFI蓝本为黑果小兵daliansky博客blog.daliansky.net的mojave镜像with clover 4903提取，感谢黑果小兵daliansky
镜像下载：https://blog.daliansky.net/macOS-Mojave-10.14.4-18E226-official-version-with-Clover-4903-original-image.html

准备工作：

一、安装前：
  所需要使用的软件
    Etcher（https://www.balena.io/etcher/）
    DG分区工具(win下制作）/苹果制作启动U盘命令（https://www.iplaysoft.com/macos-usb-install-drive.html）

二、安装
1.NVDIA显卡的机器
  nvdia显卡推荐安装10.13.6（17G65)，镜像下载地址：
  https://blog.daliansky.net/macOS-High-Sierra-10.13.6-17G65-Release-Version-with-Clover-4596-original-mirror.html
  使用Etcher制作U盘，完成后用DG分区工具将EFI-for-install.zip解压出来的EFI替换掉U盘的ESP分区中的所有文件
  修改BIOS，通过搜索引擎查找自己主板需要调整的BIOS设置
  修改U盘为第一启动项，并启动四叶草引导，参考教程
  https://blog.daliansky.net/Lenovo-Xiaoxin-Air-13-macOS-Mojave-installation-tutorial.html
  请在安装完成后使用终端运行下面的命令，并用clover configurator替换U盘的ESP分区的EFI文件为EFI-for-after install-nvdia.zip
  bash <(curl -s https://raw.githubusercontent.com/Benjamin-Dobell/nvidia-update/master/nvidia-update.sh)
  重启生效
2.AMD显卡
  AMD免驱显卡推荐安装10.14.4，镜像下载地址：
  https://blog.daliansky.net/macOS-Mojave-10.14.4-18E226-official-version-with-Clover-4903-original-image.html
  使用Etcher制作U盘，完成后用DG分区工具将EFI-for-install.zip解压出来的EFI替换掉U盘的ESP分区中的所有文件
  修改BIOS，通过搜索引擎查找自己主板需要调整的BIOS设置
  修改U盘为第一启动项，并启动四叶草引导，参考教程
  https://blog.daliansky.net/Lenovo-Xiaoxin-Air-13-macOS-Mojave-installation-tutorial.html
  用clover configurator替换U盘的ESP分区的EFI文件为EFI-for-after install-AMD.zip
  重启生效
3.intel
  
