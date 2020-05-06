#2.1.2　Bochs的安装 2.1.3　Bochs的使用

下载地址:
bochs:https://sourceforge.net/projects/bochs/


===============================================
问题一:
描述:x11/xlib no such file or directory
参考:https://stackoverflow.com/questions/5299989/x11-xlib-h-not-found-in-ubuntu
apt-cache search Xlib.h

sudo apt-get install libx11-dev

问题二:
描述: x11/extensions/Xrandr.h no such file or directory
参考: https://blog.csdn.net/Sunnil/article/details/79243192
sudo apt-get install xorg-dev
及其他包

问题三:
描述:undefined reference to symbol 'xsetforeground'
参考:
https://askubuntu.com/questions/375624/gui-libgui-ax-o-undefined-reference-to-symbol-xsetforeground-when-compiling
https://blog.csdn.net/cloudblaze/article/details/52752912
configure时添加 LIBS='-lX11'，如下:
./configure --enable-debugger --enable-disasm LIBS='-lX11'


安装完成后:
/usr/local/bin目录下有: bochs bximage 两个程序
/usr/local下的 sbin share etc include 均没有相关程序
/usr/local/share 目录下有 bochs目录
/usr/local/share/doc 目录下有 bochs目录的示例配置文件 bochsrc-sample.txt

问题四:
描述: bochs 启动时 报错
quit_sim called with exit code 1
参考: https://sourceforge.net/p/bochs/discussion/39592/thread/d718e25e/
https://groups.google.com/forum/#!topic/osfromscratch/apeIsZzDhGk
暂未查明原因，网上找的一份配置可实现debug模式启动: https://www.wandouip.com/t5i33394/
