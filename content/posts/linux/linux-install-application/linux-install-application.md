+++
title = "My Install Application in Linux"
author = ["Shawn Dennis Lin"]
date = 2021-03-16T00:00:00+08:00
lastmod = 2021-04-17T21:37:28+08:00
tags = ["linux"]
categories = ["OS"]
draft = false
hero = "/posts/linux/linux-install-application/images/linux.png"
[menu.sidebar]
  parent = "linux"
  weight = "auto"
  identifier = "linux-install-app"
  name = "Linux Install Application"
+++

These are the applications I installed in Linux. If you have any questions about these apps, you can contact me.  

<!--more-->

My OS information  

``````sh
                         ./+o+-       shdennlin@nb
                 yyyyy- -yyyyyy+      OS: Ubuntu 20.04 focal
              ://+//////-yyyyyyo      Kernel: x86_64 Linux 5.8.0-48-generic
          .++ .:/++++++/-.+sss/`      Uptime: 52m
        .:++o:  /++++++++/:--:/-      Packages: 2706
       o:+o+:++.`..```.-/oo+++++/     Shell: bash 5.0.17
      .:+o:+o/.          `+sssoo+/    Resolution: 1920x1080
 .++/+:+oo+o:`             /sssooo.   DE: GNOME 3.36.5
/+++//+:`oo+o               /::--:.   WM: Mutter
\+/+o+++`o++o               ++////.   WM Theme: 
 .++.o+++oo+:`             /dddhhh.   GTK Theme: Yaru-dark [GTK2/3]
      .+.o+oo:.          `oddhhhh+    Icon Theme: Yaru
       \+.++o+o``-````.:ohdhhhhh+     Font: Ubuntu 11
        `:o+++ `ohhhhhhhhyo++os:      Disk: 89G / 471G (20%)
          .o:`.syhhhhhhh/.oo++o`      CPU: Intel Core i5-9300H @ 8x 2.4GHz [52.0°C]
              /osyyyyyyo++ooo+++/     GPU: GeForce GTX 1050
                  ````` +oo+++o\:     RAM: 4700MiB / 15891MiB
                         `oo++.     
``````


## System {#system}


### boot-repair {#boot-repair}

``````shell
sudo add-apt-repository ppa:yannubuntu/boot-repair &&\
sudo apt-get update &&\
sudo apt-get install -y boot-repair && boot-repair
``````

-   Ref: <https://help.ubuntu.com/community/Boot-Repair>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-19 Fri&gt;</span></span>  


### Dotfiles {#dotfiles}

``````shell
mkdir ~/.dotfiles &&\
git clone https://github.com/shdennlin/dotfiles.git ~/.dotfiles/. &&\
cd ~/.dotfiles &&\
bash install.sh &&\
``````

-   GitHub: <https://github.com/shdennlin/dotfiles>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-19 Fri&gt;</span></span>  


### extra-cmake-modules {#extra-cmake-modules}

``````shell
cd ~/Downloads &&\
git clone https://github.com/KDE/extra-cmake-modules.git &&\
cd extra-cmake-modules &&\
mkdir build &&\
cd build &&\
cmake ..  &&\
make &&\
sudo make install
``````

-   GitHub: [KDE/extra-cmake-modules](https://github.com/KDE/extra-cmake-modules)


### fcitx & boshiamy {#fcitx-and-boshiamy}

``````shell
sudo apt-get install -y fcitx fcitx-table-boshiamy fcitx-chewing
``````

-   Ref: [Linux Ubuntu 嘸蝦米輸入法的FCITX安裝](https://thorasgard520.blogspot.com/2019/04/linux-ubuntu-fcitx.html)

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-19 Fri&gt;  </span></span>    


### font {#font}

``````shell
# cd ~/Downloads &&\
# git clone https://github.com/shdennlin/linux-configuration.git &&\
# cd ~/Downloads/linux-configuration/fonts &&\
# bash install.sh
cd ~/Downloads
git clone --depth 1 https://github.com/ryanoasis/nerd-fonts.git
cd nerd-fonts
./install.sh

sudo apt-get install fonts-powerline


``````

-   GitHub: <https://github.com/powerline/fonts>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-04-11 Sun&gt;</span></span>  


### GNOME {#gnome}

Install gnome extensions and web plugins  

``````shell
sudo apt install -y gnome-tweaks gnome-shell-extensions &&\
sudo apt install -y chrome-gnome-shell
gnome-shell --version
``````

-   Ref: [針對Gnome 3的Linux桌面進行美化](https://www.itread01.com/content/1544311459.html)

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-19 Fri&gt;</span></span>  


#### My extensions {#my-extensions}

1.  [Auto Move Windows](https://extensions.gnome.org/extension/16/auto-move-windows/)
2.  [Caffeine](https://extensions.gnome.org/extension/517/caffeine/)
3.  [Dash to Dock](https://extensions.gnome.org/extension/307/dash-to-dock/)
4.  [Desktop Icons](https://extensions.gnome.org/extension/1465/desktop-icons/)
5.  [Hide Top Bar](https://extensions.gnome.org/extension/545/hide-top-bar/)
6.  [OpenWeather](https://extensions.gnome.org/extension/750/openweather/)
7.  [Remove Dropdown Arrows](https://extensions.gnome.org/extension/800/remove-dropdown-arrows/)
8.  [system-monitor](https://extensions.gnome.org/extension/120/system-monitor/)


### <span class="org-todo todo TODO">TODO</span> NFS {#nfs}

``````shell
sudo apt install -y nfs-kernel-server nfs-common
``````

show status  

``````shell
systemctl status rpcbind.service
systemctl status 
``````

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-18 Thu&gt;</span></span>  


### systemback {#systemback}

``````shell
sudo apt install systemback
``````

-   Install tutorial: <https://ubuntuqa.com/zh-tw/article/10012.html>
-   Install tutorial: <https://www.linuxbabe.com/ubuntu/install-systemback-ubuntu-18-04-bionic-18-10>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-18 Thu&gt;</span></span>  


### update & upgrade {#update-and-upgrade}

``````shell
sudo apt-get update && sudo apt-get -y upgrade
``````

or  

``````shell
sudo apt-get update && sudo apt-get -y dist-upgrade
``````

-   Ref: [APT upgrade 和 dist-upgrade 的差別](https://blog.longwin.com.tw/2008/03/debian%5Fubuntu%5Fapt%5Fdist%5Fupgrade%5Fdifference%5F2008/)


### 中文 Language pack {#中文-language-pack}

``````shell
echo $LANG

sudo apt-get install -y language-pack-zh-han* &&\
sudo apt install $(check-language-support)

sudo apt-get install language-pack-gnome-zh-han*
``````

-   Ref: [Ubuntu 18.04 LTS 命令行方式安裝中文語言包](https://www.twblogs.net/a/5c38452dbd9eee35b21d8750)

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-19 Fri&gt;</span></span>  


### System Problem {#system-problem}


#### OS Information {#os-information}

`cat /etc/os-release`  

``````shell
NAME="Ubuntu"
VERSION="20.04.2 LTS (Focal Fossa)"
ID=ubuntu
ID_LIKE=debian
PRETTY_NAME="Ubuntu 20.04.2 LTS"
VERSION_ID="20.04"
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
VERSION_CODENAME=focal
UBUNTU_CODENAME=focal
``````

`lshw -class display`  

``````shell
*-display                 
      description: VGA compatible controller
      product: GP107M [GeForce GTX 1050 3 GB Max-Q]
      vendor: NVIDIA Corporation
      physical id: 0
      bus info: pci@0000:01:00.0
      version: a1
      width: 64 bits
      clock: 33MHz
      configuration: driver=nvidia latency=0
      resources: irq:138 memory:a3000000-a3ffffff memory:90000000-9fffffff memory:a0000000-a1ffffff ioport:4000(size=128) memory:a4080000-a40fffff

*-display
      description: VGA compatible controller
      product: UHD Graphics 630 (Mobile)
      vendor: Intel Corporation
      physical id: 2
      bus info: pci@0000:00:02.0
      version: 00
      width: 64 bits
      clock: 33MHz
      capabilities: pciexpress msi pm vga_controller bus_master cap_list rom
      configuration: driver=i915 latency=0
      resources: irq:137 memory:a2000000-a2ffffff memory:b0000000-bfffffff ioport:5000(size=64) memory:c0000-dffff
``````

`nvidia-smi`  

``````shell
+-----------------------------------------------------------------------------+
| NVIDIA-SMI 460.67       Driver Version: 460.67       CUDA Version: 11.2     |
|-------------------------------|----------------------|----------------------+
| GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
| Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
|                               |                      |               MIG M. |
|===============================+======================+======================|
|   0  GeForce GTX 1050    Off  | 00000000:01:00.0  On |                  N/A |
| N/A   43C    P0    N/A /  N/A |    335MiB /  3020MiB |      0%      Default |
|                               |                      |                  N/A |
+-------------------------------|----------------------|----------------------+

+-----------------------------------------------------------------------------+
| Processes:                                                                  |
|  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
|        ID   ID                                                   Usage      |
|=============================================================================|
|    0   N/A  N/A      1752      G   /usr/lib/xorg/Xorg                 57MiB |
|    0   N/A  N/A      2432      G   /usr/lib/xorg/Xorg                196MiB |
|    0   N/A  N/A      2629      G   /usr/bin/gnome-shell               70MiB |
+-----------------------------------------------------------------------------+
``````

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-20 Sat&gt;</span></span>  


#### Doesn't auto enable Bluetooth when system startup. {#doesn-t-auto-enable-bluetooth-when-system-startup-dot}

18.04\* users who don't naturally have a /etc/rc.local, you'll need to create one and make it executable. To make things slightly easier, you can just paste the following command into a terminal:  

``````shell
sudo install -b -m 755 /dev/stdin /etc/rc.local << EOF
#!/bin/sh
rfkill unblock bluetooth
exit 0
EOF
``````

-   Ref Website: <https://askubuntu.com/a/2568/1193335>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-18 Thu&gt;</span></span>  


#### System doesn't resume after suspend {#system-doesn-t-resume-after-suspend}

[ `V` ] means it's work for me  
[ `X` ] means it's not work for me  
<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-20 Sat&gt;</span></span>  

<!--list-separator-->

-  [ `X` ] Suspend and hibernate configuration in Debian Jessie

    1.  edit `/etc/systemd/logind.conf`
    2.  create the file `/etc/systemd/system/suspend-sedation.service`
    
    Ref: <https://wiki.debian.org/Hibernation>  
    Ref: <https://wiki.debian.org/SystemdSuspendSedation>  

<!--list-separator-->

-  [ `X` ] Hibernate with hibernate command

    ``````shell
    sudo apt-get install hibernate
    sudo hibernate
    ``````

<!--list-separator-->

-  [ `X` ] edit `/etc/systemd/logind.conf`

    Ref: <https://askubuntu.com/a/1245763/1193335>  

<!--list-separator-->

-  [ `X` ] edit `/etc/default/grub` file

    ``````shell
    GRUB_CMDLINE_LINUX="nouveau.modeset=0"
    ``````
    
    after that run:  
    
    ``````shell
    sudo update-grub
    sudo reboot
    ``````
    
    Ref: <https://askubuntu.com/a/1041395/1193335>  

<!--list-separator-->

-  [ `X` ] sudo apt-get install pm-utils

    I got a workaround for suspend working on Ubuntu 18.04 with a NVIDIA  
    GeForce GTX 1050 Mobile and proprietary nvidia drivers 390. I installed  
    pm-suspend via `sudo apt-get install pm-utils`. Then, I switch from  
    Gnome Shell to the terminal via Ctrl+Alt+f6. After the login, I do  
    `sudo pm-suspend`. After waking up from standby, I change back to Gnome  
    Shell via Ctrl+Alt+f1. Done!  
    
    Ref: <https://askubuntu.com/a/1081639/1193335>  

<!--list-separator-->

-  [ `V` ] add-apt-repository ppa:graphics-drivers/ppa

    ``````shell
    sudo add-apt-repository ppa:graphics-drivers/ppa
    sudo apt update
    sudo apt upgrade
    sudo reboot
    ``````
    
    Ref: <https://bugs.launchpad.net/ubuntu/+source/nvidia-graphics-drivers-460/+bug/1911055> #9  

<!--list-separator-->

-  [ `not test` ] edit `/etc/gdm3/custom.conf`

    If your desktop does not load after installing the corresponding driver, then do the following:  
    `sudo nano /etc/gdm3/custom.conf`  
    then remove the comment (# symbol) from the line that says  
    `# WaylandEnable=false`  
    and save. Then reboot. If this still does not work, then please disable Secure Boot since you might actually be using UEFI.  
    
    Ref: <https://askubuntu.com/a/61433/1193335> 1. The quick way  


#### Change the login screen resolution in Ubuntu 20.04 {#change-the-login-screen-resolution-in-ubuntu-20-dot-04}

<!--list-separator-->

-  [ `X` ] edit `/etc/default/grub` file

    Step:  
    
    1.  Open a terminal and enter:  
        
        ``````shell
        sudo vi /etc/default/grub
        ``````
    2.  Find the `#GRUB_GFXMODE=640x480`, Below that line, enter the following, substituting the 1920x1080 for a supported resolution:  
        
        ``````shell
        GRUB_GFXMODE=1920x1080
        GRUB_GFXPAYLOAD_LINUX=keep
        ``````
    
    Ref: <https://askubuntu.com/a/1041697/1193335>  

<!--list-separator-->

-  [ `V` ] edit `/etc/default/grub` file

    Just want to add that I found a way to change the login screen resolution. That part of my problem has been asked and answered, see [how to change gdm3 thread](https://askubuntu.com/questions/912052/how-do-i-change-gdm3-login-screen-resolution).  
    
    After setting up the monitor resolution and zoom level I wanted, I simply copy the settings to gdm3 .config directory, make any further changes you need and then reboot the PC.  
    
    ``````shell
    sudo cp -i ~/.config/monitors.xml /var/lib/gdm3/.config/
    less /var/lib/gdm3/.config/monitors.xml
    ``````
    
    You probably also need to do the following before rebooting. Select gdm3 when prompted.  
    
    ``````shell
    sudo dpkg-reconfigure gdm3
    ``````
    
    Ref: <https://askubuntu.com/a/1041697/1193335>  


#### <span class="org-todo todo TODO">TODO</span> Changing login background automatically {#changing-login-background-automatically}

Ref: <https://askubuntu.com/questions/1227070/how-do-i-change-login-screen-theme-or-background-in-ubuntu-20-04>  


#### Login Screen language doesn't Chinese {#login-screen-language-doesn-t-chinese}

Ref: [Ubuntu 用指令設定終端機顯示中文訊息](https://www.arthurtoday.com/2015/02/how-to-make-ubuntu-terminal-speak-your-language.html)  


#### 解決Linux系統的中文變成細明體或是標楷體的問題 {#解決linux系統的中文變成細明體或是標楷體的問題}

``````sh
sudo apt-get remove fonts-arphic-ukai fonts-arphic-uming
``````

Ref: [解決Linux系統的中文變成細明體或是標楷體的問題](https://magiclen.org/linux-font-remove-kai/)  


#### Fix time modification on your computer with dual boot (Windows 10 and Ubuntu 20.04) {#fix-time-modification-on-your-computer-with-dual-boot--windows-10-and-ubuntu-20-dot-04}

``````sh
timedatectl
timedatectl set-local-rtc 1 --adjust-system-clock
timedatectl
``````

Ref: [How to fix time modification on your computer with dual boot (Windows 10 and Ubuntu 18.04)](https://ourcodeworld.com/articles/read/1063/how-to-fix-time-modification-on-your-computer-with-dual-boot-windows-10-and-ubuntu-18-04)  


## Editor & IDE {#editor-and-ide}


### Emacs {#emacs}

An extensible, customizable, free/libre text editor — and more.  

``````shell
sudo snap install emacs --classic
``````

-   Official Website: <https://www.gnu.org/software/emacs/>
-   Snapcraft: <https://snapcraft.io/emacs>
-   GitHub: <https://github.com/emacs-mirror/emacs>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-19 Fri&gt;</span></span>  


#### Emacs GUI can't activation Fcitx input method {#emacs-gui-can-t-activation-fcitx-input-method}

<style>.org-center { margin-left: auto; margin-right: auto; text-align: center; }</style>

<div class="org-center">
  <div></div>

echo "export LC\_CTYPE=zh\_TW.UTF-8" >> ~/.xprofile  

</div>

-   Ref: [Arch Linux：環境設定與常用套件](https://blog.rex-tsou.com/2017/12/arch-linux%E7%92%B0%E5%A2%83%E8%A8%AD%E5%AE%9A%E8%88%87%E5%B8%B8%E7%94%A8%E5%A5%97%E4%BB%B6/)

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-21 Sun&gt;</span></span>  


### Intellij IDEA {#intellij-idea}

IntelliJ IDEA is an integrated development environment (IDE) written in Java for developing computer software. It is developed by JetBrains (formerly known as IntelliJ), and is available as an Apache 2 Licensed community edition, and in a proprietary commercial edition. Both can be used for commercial development.  

``````sh
sudo snap install intellij-idea-community --classic
``````

-   Official Website: <https://www.jetbrains.com/idea/>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-25 Thu&gt;</span></span>  


### Spacemacs {#spacemacs}

Spacemacs is a new way to experience Emacs -- a sophisticated and polished set-up focused on ergonomics, mnemonics and consistency.  

Just clone it, launch it, then press the space bar to explore the interactive list of carefully-chosen key bindings. You can also press the home buffer's [?] button for some great first key bindings to try.  

Spacemacs can be used naturally by both Emacs and Vim users -- you can even mix the two editing styles. Switching easily between input styles makes Spacemacs a great tool for pair-programming.  

Spacemacs is currently in beta, and contributions are very welcome.  

``````shell
git clone https://github.com/syl20bnr/spacemacs.git ~/.emacs.d &&\
git clone https://github.com/shdennlin/spacemacs-private.git ~/.spacemacs.d
``````

-   GitHub1: [syl20bnr/spacemacs](https://github.com/syl20bnr/spacemacs)
-   GitHub2: [shdennlin/spacemacs-private](https://github.com/shdennlin/spacemacs-private)
-   Ref: [spacemacs.org](https://www.spacemacs.org/)

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-19 Fri&gt;</span></span>  


### typora {#typora}

Typora gives you a seamless experience as both a reader and a writer. It removes the preview window, mode switcher, syntax symbols of markdown source code, and all other unnecessary distractions. Instead, it provides a real live preview feature to help you concentrate on the content itself.  

``````shell
# or run:
# sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys BA300B7755AFCFAE

wget -qO - https://typora.io/linux/public-key.asc | sudo apt-key add -

# add Typora's repository

sudo add-apt-repository 'deb https://typora.io/linux ./'

sudo apt-get update

# install typora

sudo apt-get install typora
``````

-   Official Website: <https://typora.io/>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-24 Wed&gt;</span></span>  


### Vim {#vim}

``````shell
sudo apt purge vim
sudo apt-get install vim-gtk3
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
``````

-   Ref: [shdennlin/dotfiles](https://github.com/shdennlin/dotfiles)


## Software Engineering {#software-engineering}


### Anaconda {#anaconda}

``````shell
## Install
sudo apt-get install -y libgl1-mesa-glx libegl1-mesa libxrandr2 libxrandr2 libxss1 libxcursor1 libxcomposite1 libasound2 libxi6 libxtst6
cd ~/Downloads
wget https://repo.anaconda.com/archive/Anaconda3-2020.11-Linux-x86_64.sh
sh ~/Downloads/Anaconda3-2020.11-Linux-x86_64.sh


## For Spacemacs
# for import sorting
pip install pyls-isort
# for mypy checking (python 3.4+ is needed)
pip install pyls-mypy
pip install pyls-black
# Syntax checking uses flake8 package: 
pip install flake8
# To be able to suppress unused imports easily
pip install autoflake
# To use dap-mode for debugging do: 
pip install "ptvsd>=4.2"
pip install importmagic epc

echo "export PYTHONPATH=/home/$(whoami)/anaconda3/bin/" >> ~/.bashrc


conda create -n tf-gpu tensorflow-gpu
conda activate tf-gpu
``````

-   Official Website: <https://docs.anaconda.com/>
-   Install tutorial: <https://docs.anaconda.com/anaconda/install/linux/>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-30 Tue&gt;</span></span>  


### Java {#java}

``````shell
# install open JRE
sudo apt install openjdk-8-jre
# change default version in Ubuntu
sudo update-alternatives --config java
# check java version
java -version
# set JAVA_HOME environment variable
echo "export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64/" >> ~/.bashrc
echo "export PATH=\$PATH:\$JAVA_HOME/bin" >> ~/.bashrc
echo $PATH | grep java
``````

-   Official Website: <https://www.oracle.com/java/>
-   Install tutorial: <https://www.oracle.com/java/technologies/javase-downloads.html>
-   Open JRE: <https://ubuntu.com/tutorials/install-jre>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-26 Fri&gt;</span></span>  


### JavaScirpt-Node Package Manager(NPM) {#javascirpt-node-package-manager--npm}

npm (originally short for Node Package Manager)[4] is a package manager for the JavaScript programming language.  

``````shell
sudo apt install -y npm
sudo npm i -g npm

sudo npm install -g chokidar
sudo npm install -g urix
sudo npm install -g resolve-url

sudo npm install -g vmd

sudo npm audit fix
``````

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-25 Thu&gt;</span></span>  


### KiCad {#kicad}

A Cross Platform and Open Source Electronics Design Automation Suite  

``````shell
sudo add-apt-repository --yes ppa:js-reynaud/kicad-4 ; &&\
sudo apt-get update ; &&\
sudo apt-get install -y kicad
``````

-   Official Website: <https://kicad.org/>
-   Install tutorial: <https://kicad.org/download/ubuntu/>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-25 Thu&gt;</span></span>  


### Latex {#latex}

``````shell
sudo apt-get install texlive-base &&\
sudo apt-get install texlive-latex-recommended &&\
sudo apt-get install texlive &&\
sudo apt-get install texlive-latex-extra &&\
sudo apt-get install texlive-xetex
``````

-   Ref: [How to install LaTex on Ubuntu 20.04 Focal Fossa Linux](https://linuxconfig.org/how-to-install-latex-on-ubuntu-20-04-focal-fossa-linux)


### MySQL {#mysql}

``````shell
sudo apt-get install mysql-server
sudo apt install mysql-client
sudo apt install libmysqlclient-dev
``````

check insall  

``````shell
sudo netstat -tap | grep mysql
``````

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-25 Thu&gt;</span></span>  


### phpMyAdmin {#phpmyadmin}

``````sh
sudo apt-get install phpmyadmin -y
``````

-   Official Website: <https://www.phpmyadmin.net/>
-   Documentation: <https://docs.phpmyadmin.net/en/latest/>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-04-01 Thu&gt;</span></span>  


### Nginx {#nginx}

Nginx (pronounced "engine X"), stylized as NGINX, nginx or NginX, is a web server that can also be used as a reverse proxy, load balancer, mail proxy and HTTP cache. The software was created by Igor Sysoev and publicly released in 2004. Nginx is free and open-source software, released under the terms of the 2-clause BSD license. A large fraction of web servers use NGINX, often as a load balancer.  

``````sh
sudo apt-get install -y nginx
sudo nginx -v
sudo nginx
curl -I 127.0.0.1
``````

-   GitHub: [https://github.com/nginx/nginx](https://github.com/nginx/nginx)
-   Repository: [https://hg.nginx.org/nginx](https://hg.nginx.org/nginx)
-   Official Website: [https://www.nginx.com/](https://www.nginx.com/)
-   Install tutorial: [https://docs.nginx.com/nginx/admin-guide/installing-nginx/installing-nginx-open-source/](https://docs.nginx.com/nginx/admin-guide/installing-nginx/installing-nginx-open-source/)

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-26 Fri&gt;</span></span>  


### Ruby-RVM {#ruby-rvm}

Ruby Version Manager (RVM)  

RVM is a command-line tool which allows you to easily install, manage, and work with multiple ruby environments from interpreters to sets of gems.  

Install Step:  

1.  To see `Install tutorial`
2.  after Install, type  
    
    ``````sh
    echo "[[ -s \"$HOME/.rvm/scripts/rvm\" ]] && . \"$HOME/.rvm/scripts/rvm\"" >> ~/.profile
    ``````
3.  reboot system

<!--listend-->

-   Official Website: <https://rvm.io/>
-   Install tutorial: <https://rvm.io/rvm/install>


### Tensorflow-gpu {#tensorflow-gpu}

``````shell
cd ~/Downloads
wget http://tw.download.nvidia.com/XFree86/Linux-x86_64/440.82/NVIDIA-Linux-x86_64-440.82.run
``````

-   Ref: [Installing TensorFlow 2 with GPU support on Ubuntu 20.04 LTS](https://illya13.github.io/RL/tutorial/2020/04/26/installing-tensorflow-on-ubuntu-20.html)


### PHP {#php}

``````sh
sudo apt install php
``````

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-04-01 Thu&gt;</span></span>  


### Redis {#redis}

Redis is an in-memory database that persists on disk. The data model is key-value, but many different kind of values are supported: Strings, Lists, Sets, Sorted Sets, Hashes, Streams, HyperLogLogs, Bitmaps.  

``````sh
sudo add-apt-repository ppa:redislabs/redis &&\
sudo apt-get update &&\
sudo apt-get install -y redis
``````

-   GitHub: <https://github.com/redis/redis>
-   Official Website: <https://redis.io/>
-   Install tutorial: <https://redis.io/download>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-26 Fri&gt; </span></span>   


### Jenkins {#jenkins}

``````sh
wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > \
    /etc/apt/sources.list.d/jenkins.list'
sudo apt-get update
sudo apt-get install jenkins
``````

-   Official Website: <https://www.jenkins.io/>
-   Install tutorial: <https://www.jenkins.io/download/>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-30 Tue&gt;</span></span>  


## Engineering Tool {#engineering-tool}


### Angry IP scanner {#angry-ip-scanner}

Angry IP Scanner - fast and friendly network scanner  
**Go to Download Page to Download `deb` file** and type below:  

``````shell
cd ~/Downloads
sudo apt install ipscan_3.7.6_all.deb # your version
``````

-   Official Website: <https://angryip.org/about/>
-   Download Page: <https://angryip.org/download/#linux>
-   GitHub: <https://github.com/angryip/ipscan/tree/3.7.2>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-19 Fri&gt;</span></span>  


### flatpak {#flatpak}

``````shell
sudo apt install -y flatpak
``````

-   Ref: [flatpak](https://zh.wikipedia.org/wiki/Flatpak)(wiki)


### Git {#git}

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.  

``````shell
sudo add-apt-repository ppa:git-core/ppa
sudo apt update
sudo apt-get -y install git
``````

-   Official Website: <https://git-scm.com/>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-20 Sat&gt;</span></span>  


### GitKraken {#gitkraken}

``````shell
wget https://release.gitkraken.com/linux/gitkraken-amd64.deb ~/Downloads &&\
sudo dpkg -i ~/Downloads/gitkraken-amd64.deb
``````

-   Ref: [GitKrakon](https://www.gitkraken.com/)


### HUGO {#hugo}

A Fast and Flexible Static Site Generator built with love by bep, spf13 and friends in Go.  

``````shell
# sudo snap install hugo  # version 0.80.0, or
# sudo apt  install hugo  # version 0.68.3-1
sudo snap install hugo
``````

-   Official Website: <https://gohugo.io/>
-   Install tutorial: <https://gohugo.io/getting-started/installing>
-   GitHub: <https://github.com/gohugoio/hugo>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-16 Tue&gt;</span></span>  


### Elastic Search {#elastic-search}

Elasticsearch is a search engine based on the Lucene library. It provides a distributed, multitenant-capable full-text search engine with an HTTP web interface and schema-free JSON documents. Elasticsearch is developed in Java and is dual-licensed under the source-available Server Side Public License and the Elastic license, while other parts fall under the proprietary (source-available) Elastic License. Official clients are available in Java, .NET (C#), PHP, Python, Apache Groovy, Ruby and many other languages. According to the DB-Engines ranking, Elasticsearch is the most popular enterprise search engine followed by Apache Solr, also based on Lucene.  

``````sh
# APT or YUM (RECOMMEND)(to see Install with Repositories)
wget -qO - https://packages.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -
echo "deb https://packages.elastic.co/elasticsearch/2.x/debian stable main" | sudo tee -a /etc/apt/sources.list.d/elasticsearch-2.x.list
sudo apt-get update && sudo apt-get install elasticsearch
whereis elasticsearch
sudo update-rc.d elasticsearch defaults 95 10
sudo /bin/systemctl daemon-reload
sudo /bin/systemctl enable elasticsearch.service

# install manually
cd ~/Downloads
curl -L -O https://download.elastic.co/elasticsearch/release/org/elasticsearch/distribution/tar/elasticsearch/2.4.6/elasticsearch-2.4.6.tar.gz
tar -xvf elasticsearch-2.4.6.tar.gz
cd elasticsearch-2.4.6/bin
./elasticsearch
./elasticsearch --cluster.name my_cluster_name --node.name my_node_name
``````

-   Official Website: <https://www.elastic.co/>
-   Install tutorial: <https://www.elastic.co/guide/en/elasticsearch/reference/index.html>
-   Install with Repositories: <https://www.elastic.co/guide/en/elasticsearch/reference/index.html>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-26 Fri&gt;</span></span>  


### Memcached {#memcached}

Memcached is a high performance multithreaded event-based key/value cache store intended to be used in a distributed system.  

``````sh
sudo apt-get install libevent-dev
sudo apt-get install memcached
``````

-   GitHub: <https://github.com/memcached/memcached>
-   Official Website: <https://memcached.org/>
-   Install tutorial: <https://github.com/memcached/memcached/wiki/Install>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-26 Fri&gt;</span></span>  


## Life Tool {#life-tool}


### BingWall - Bing wallpaper of the day {#bingwall-bing-wallpaper-of-the-day}

Bing wallpaper of the day application for Gnome desktop.  

``````shell
sudo snap install bing-wall
``````

-   Snapcraft: <https://snapcraft.io/bing-wall>
-   GitHub: <https://github.com/keshavbhatt/BingWall>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-16 Tue&gt;</span></span>  


### Bitwarden {#bitwarden}

``````sh
# desktop application
sudo snap install bitwarden

# command-line tool(CLI)
sudo npm install -g @bitwarden/cli
``````

-   GitHub: <https://github.com/bitwarden>
-   Official Website: <https://bitwarden.com/>
-   Install tutorial: <https://bitwarden.com/download/>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-27 Sat&gt;</span></span>  


### Crow Translate {#crow-translate}

A small translate tool like QTranslate.  

``````shell
sudo add-apt-repository ppa:jonmagon/crow-translate &&\
sudo apt update &&\
sudo apt install crow-translate
``````

-   Official Website: <https://crow-translate.github.io/>
-   GitHub: <https://github.com/crow-translate/crow-translate>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-19 Fri&gt;</span></span>  


### draw.io {#draw-dot-io}

``````shell
sudo snap install drawio
``````

-   GitHub: <https://github.com/jgraph/drawio-desktop>
-   Snapcraft: <https://snapcraft.io/drawio>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-23 Tue&gt;</span></span>  


### FreeCAD {#freecad}

``````shell
sudo apt install -y freecad
``````


### FSearch {#fsearch}

FSearch is a fast file search utility, inspired by Everything Search Engine. It's written in C and based on GTK+3.  

``````shell
sudo add-apt-repository ppa:christian-boxdoerfer/fsearch-daily &&\
sudo apt-get update &&\
sudo apt install fsearch-trunk
``````

-   GitHub: [cboxdoerfer/fsearch](https://github.com/cboxdoerfer/fsearch)


### linux-wifi-hotspot {#linux-wifi-hotspot}

Feature-rich wifi hotspot creator for Linux which provides both GUI and command-line interface. It is also able to create a hotspot using the same wifi card which is connected to an AP already ( Similar to Windows 10).  

``````shell
sudo add-apt-repository ppa:lakinduakash/lwh
sudo apt install linux-wifi-hotspot
``````

-   GitHub: <https://github.com/lakinduakash/linux-wifi-hotspot>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-19 Fri&gt;</span></span>  


### Logitech MX Master {#logitech-mx-master}

First:  

``````shell
sudo apt install -y cmake libevdev-dev libudev-dev libconfig++-dev &&\
mkdir -p ~/Downloads/logiops &&\
git clone https://github.com/PixlOne/logiops.git ~/Downloads/logiops/  &&\
cd ~/Downloads/logiops &&\
mkdir build &&\
cd build &&\
cmake .. &&\
make &&\
sudo make install &&\
sudo systemctl start logid
``````

Second:  

``````shell
mkdir -p ~/Downloads/logitech-mouse-config &&\
git clone https://github.com/shdennlin/logitech-mouse-config.git ~/Downloads/logitech-mouse-config/ &&\
cd ~/Downloads/logitech-mouse-config/ &&\
bash install.sh
``````

-   GitHub: [shdennlin/logitech-mouse-config](https://github.com/shdennlin/logitech-mouse-config)
-   Ref: See GitHub


### MusixMatch {#musixmatch}

``````shell
sudo snap install musixmatch
``````

-   GitHub:
-   Ref: [Install Musixmatch on your Linux distribution](https://snapcraft.io/musixmatch)


### nomacs {#nomacs}

nomacs is a free, open source image viewer, which supports multiple platforms. You can use it for viewing all common image formats including RAW and psd images.  

``````shell
sudo apt install nomacs &&\
sudo apt-get install nomacs-l10n
``````

-   Ref: [nomacs.org](https://nomacs.org/%5C)


### Okular {#okular}

Okular is a universal document viewer developed by KDE. Okular works on multiple platforms, including but not limited to Linux, Windows, macOS, \*BSD, etc.  

``````shell
sudo apt-get install okular
``````

-   Ref: [okular.kde.org](https://okular.kde.org/)


### Open Broadcaster Software Studio (OBS) {#open-broadcaster-software-studio--obs}

Free and open source software for video recording and live streaming.  

``````shell
sudo add-apt-repository ppa:obsproject/obs-studio ;\
sudo apt update ;\
sudo apt install -y obs-studio
``````

-   Ref1: [obsproject.com](https://obsproject.com/)
-   Ref2: [9 Best Screen Recorders For Linux](https://itsfoss.com/best-linux-screen-recorders/)


### Rclone {#rclone}

``````sh
curl https://rclone.org/install.sh | sudo bash
rclone config

# Mount Google drive Locally
# https://www.youtube.com/watch?v=f8K-V3HHDA0
rclone mount --daemon shdennlin: /home/shdennlin/gdrive-shdennlin/
df -h
``````

-   GitHub: <https://github.com/rclone/rclone>
-   Official Website: <https://rclone.org/>
-   Install tutorial: <https://rclone.org/install/>
-   Drive Install tutorial: <https://rclone.org/drive/>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-27 Sat&gt;</span></span>  


### Spotify {#spotify}

``````shell
sudo snap install spotify
``````

-   Official Website: <https://www.spotify.com/>
-   Snapcraft: <https://snapcraft.io/spotify>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-19 Fri&gt; </span></span>   


## Terminal Tool {#terminal-tool}


### aria2 {#aria2}

aria2 is a lightweight multi-protocol & multi-source command-line download utility. It supports HTTP/HTTPS, FTP, SFTP, BitTorrent and Metalink. aria2 can be manipulated via built-in JSON-RPC and XML-RPC interfaces.  

``````shell
sudo apt-get install -y aria2
``````

-   GitHub: <https://github.com/aria2/aria2>
-   Official Website: <https://aria2.github.io/>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-04-17 Sat&gt;</span></span>  


### autojump {#autojump}

a faster way to navigate your filesystem  

``````shell
sudo apt install autojump
``````

-   GitHub: <https://github.com/wting/autojump>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-04-17 Sat&gt;</span></span>  


### exa & bat {#exa-and-bat}

**exa**  
exa is a modern replacement for ls.  

``````shell
# ubuntu 20.10 and later
sudo apt install exa
# ubuntu 20.10 before
curl https://sh.rustup.rs -sSf | sh
cargo install exa
``````

-   GitHub: <https://github.com/ogham/exa>
-   Official Website: <https://the.exa.website/>
-   Install tutorial: <https://the.exa.website/install>

**bat**  
A code searching tool similar to ack, with a focus on speed.  

``````shell
sudo apt install -y bat
``````

-   GitHub: <https://github.com/sharkdp/bat>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-04-17 Sat&gt;</span></span>  


### fd & ag {#fd-and-ag}

**fd**  
fd is a program to find entries in your filesytem. It is a simple, fast and user-friendly alternative to find. While it does not aim to support all of find's powerful functionality, it provides sensible (opinionated) defaults for a majority of use cases.  

``````shell
sudo apt install fd-find
``````

-   GitHub: <https://github.com/sharkdp/fd>

**ag**  
A code searching tool similar to ack, with a focus on speed.  

``````shell
sudo apt-get install -y silversearcher-ag
``````

-   GitHub: <https://github.com/ggreer/the%5Fsilver%5Fsearcher>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-04-17 Sat&gt;</span></span>  


### fzf {#fzf}

fzf is a general-purpose command-line fuzzy finder.  

``````shell
sudo apt-get install fzf
``````

-   GitHub: <https://github.com/junegunn/fzf>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-04-17 Sat&gt;</span></span>  


### gdrive {#gdrive}

``````shell
cd ~/Downloads &&\
wget -O drive https://drive.google.com/uc?id=0B3X9GlR6Embnb095MGxEYmJhY2c &&\
sudo install drive /usr/local/bin/drive
``````

-   GitHub: [prasmussen/gdrive](https://github.com/prasmussen/gdrive)
-   Ref: [如何在終端機介面使用 Google Drive (gdrive cmd)](https://hiraku.tw/2020/01/5894/)


### jq {#jq}

Command-line JSON processor  

``````shell
sudo apt-get install -y jq
``````

-   GitHub: <https://github.com/stedolan/jq>
-   Official Website: <https://stedolan.github.io/jq/>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-04-17 Sat&gt;</span></span>  


### Linux Advanced Power Management (TLP) {#linux-advanced-power-management--tlp}

TLP is a feature-rich command line utility for Linux, saving laptop battery power without the need to delve deeper into technical details.  

TLP’s default settings are already optimized for battery life and implement Powertop’s recommendations out of the box. So you may just install and forget it.  

Nevertheless TLP is highly customizable to fulfil your specific requirements.  

``````shell
sudo add-apt-repository ppa:linrunner/tlp &&\
sudo apt update &&\
sudo apt install tlp tlp-rdw &&\
sudo apt-get install smartmontools &&\
sudo systemctl start tlp &&\
sudo tlp-stat | less
``````

-   Ref: [linux tlp tutorial](https://github.com/twtrubiks/linux-note/tree/master/linux-tlp-tutorial)
-   Ref: [TLP - Optimize Linux Laptop Battery Life](https://linrunner.de/tlp/)


### lm Sensors {#lm-sensors}

``````shell
sudo apt install -y lm-sensors

sudo sensors-detect

sensors
``````

-   Ref: [How to Install lm Sensors on Linux](https://linoxide.com/install-lm-sensors-linux/)

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-18 Thu&gt;</span></span>  


### locate {#locate}

``````shell
sudo apt install -y mlocate
``````

-   Ref: [搜尋指令 which, whereis, locate, find的差別](http://blog.faq-book.com/?p=1013)

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-19 Fri&gt;</span></span>  


### mosh {#mosh}

Mosh is a remote terminal application that supports intermittent connectivity, allows roaming, and provides speculative local echo and line editing of user keystrokes.  

``````shell
sudo apt-get install mosh
``````

-   GitHub: <https://github.com/mobile-shell/mosh>
-   Official Website: <https://mosh.org/>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-04-17 Sat&gt;</span></span>  


### NCdU {#ncdu}

Ncdu is a disk usage analyzer with an ncurses interface. It is designed to find space hogs on a remote server where you don't have an entire graphical setup available, but it is a useful tool even on regular desktop systems. Ncdu aims to be fast, simple and easy to use, and should be able to run in any minimal POSIX-like environment with ncurses installed.  

``````sh
sudo apt install ncdu
``````

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-04-17 Sat&gt;</span></span>  


### rar, zip {#rar-zip}

``````shell
apt-get install -y unrar &&\
sudo apt install -y p7zip-full
``````


### screenfetch {#screenfetch}

screenFetch is a "Bash Screenshot Information Tool". This handy Bash script can be used to generate one of those nifty terminal theme information + ASCII distribution logos you see in everyone's screenshots nowadays. It will auto-detect your distribution and display an ASCII version of that distribution's logo and some valuable information to the right. There are options to specify no ASCII art, colors, taking a screenshot upon displaying info, and even customizing the screenshot command! This script is very easy to add to and can easily be extended.  

``````shell
sudo apt install screenfetch
``````

-   GitHub: <https://github.com/KittyKatt/screenFetch>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-25 Thu&gt;</span></span>  


### Snap {#snap}

``````sh
sudo apt install snapd
``````

-   Ref: <https://codeburst.io/how-to-install-and-use-snap-on-ubuntu-18-04-9fcb6e3b34f9>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-28 Sun&gt;</span></span>  


### Terminator {#terminator}

Originally created and developed for a long time by Chris Jones, the goal of this project is to produce a useful tool for arranging terminals. It is inspired by programs such as gnome-multi-term, quadkonsole, etc. in that the main focus is arranging terminals in grids (tabs is the most common default method, which Terminator also supports).  

Much of the behaviour of Terminator is based on GNOME Terminal, and we are adding more features from that as time goes by, but we also want to extend out in different directions with useful features for sysadmins and other users. If you have any suggestions, please file wishlist bugs! (see below for the address)  

``````shell
sudo apt install -y terminator
``````

-   Official Website: <https://gnometerminator.blogspot.com/>
-   Install tutorial: <https://gnometerminator.blogspot.com/p/introduction.html>
-   My configuration: <https://github.com/shdennlin/dotfiles>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-16 Tue&gt;</span></span>  


### top-bpytop {#top-bpytop}

Resource monitor that shows usage and stats for processor, memory, disks, network and processes. Python port of bashtop.  

``````shell
cd ~/Downloads &&\
git clone https://github.com/aristocratos/bpytop.git &&\
cd bpytop &&\
sudo make install
``````

-   GitHub: <https://github.com/aristocratos/bpytop>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-19 Fri&gt;</span></span>  


### top-NVTOP {#top-nvtop}

Nvtop stands for NVidia TOP, a (h)top like task monitor for NVIDIA GPUs. It can handle multiple GPUs and print information about them in a htop familiar way.  

``````shell
sudo apt install cmake libncurses5-dev libncursesw5-dev
sudo apt install -y nvtop
``````

-   GitHub: <https://github.com/Syllo/nvtop>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-18 Thu&gt;</span></span>  


### xclip {#xclip}

xclip is a command line interface to the X11 clipboard. It allows you to put the output of a command directly into the clipboard so that you don't have to copy&paste from the terminal manually (which can be a tedious task especially if the output is very long). It also allows you to put the contents of a file directly into the clipboard.  

``````shell
sudo apt-get install -y xclip
``````

-   Ref: [Command-Line Copy&Paste With xclip (Debian/Ubuntu)](https://www.howtoforge.com/command-line-copy-and-paste-with-xclip-debian-ubuntu)


### ImageMagick {#imagemagick}

ImageMagick is a free and open-source cross-platform software suite for displaying, creating, converting, modifying, and editing raster images. Created in 1987 by John Cristy, it can read and write over 200 image file formats. It and its components are widely used in open-source applications.  

``````sh
cd ~/Downloads &&\
git clone --depth 1 https://github.com/ImageMagick/ImageMagick.git ImageMagick-7.0.11 &&\
cd ImageMagick-7.0.11 &&\
./configure &&\
make

./configure --with-modules
sudo make install
sudo ldconfig /usr/local/lib
/usr/local/bin/convert logo: logo.gif
magick identify -version
``````

-   GitHub: <https://github.com/ImageMagick/ImageMagick>
-   Official Website: <https://imagemagick.org/index.php>
-   Install tutorial: <https://imagemagick.org/script/install-source.php>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-26 Fri&gt;  </span></span>    


### lighttpd {#lighttpd}

``````nil
sudo apt install lighttpd
``````


### ZSH {#zsh}

``````sh
# =============== install zsh ===============
sudo apt install -y zsh

# set zsh as default in user
chsh -s $(which zsh)
# logout GUI if you use GUI desktop
# login
echo $SHELL

# set zsh as default in root
sudo su
chsh -s $(which zsh) root
echo $SHELL

# =============== install extension ===============
# install ohmyzsh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# install theme
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

# install icon ====> to see font to install

# alias
echo "source $HOME/.aliases" >> ~/.zshrc
# ====> install .aliases from my dot file

# =============== install extension for root ===============
sudo ln -s $HOME/.oh-my-zsh           /root/.oh-my-zsh
sudo ln -s $HOME/.zshrc               /root/.zshrc
sudo ln -s $HOME/.p10k.zsh            /root/.p10k.zsh
``````

-   Official Website: <https://www.zsh.org/>
-   Oh My Zsh Official Website: <https://ohmyz.sh/>
-   Oh My Zsh GitHub: <https://github.com/ohmyzsh/ohmyzsh>
-   powerlevel10k GitHub: <https://github.com/romkatv/powerlevel10k>
-   My zsh configuration: <https://github.com/shdennlin/dotfiles/blob/main/.zshrc>

-   My Plugins by manual install  
    1.  [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)  
        `git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`
    2.  [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)  
        `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`
    3.  [autojump](https://github.com/wting/autojump)  
        `sudo apt install autojump`
    4.  [zsh-completions](https://github.com/zsh-users/zsh-completions)  
        `git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:=~/.oh-my-zsh/custom}/plugins/zsh-completions`
    5.  [fzf](https://github.com/junegunn/fzf)  
        `sudo apt-get install fzf`


## Communication {#communication}


### Discord {#discord}

``````shell
sudo snap install discord
``````

-   Official Website: <https://discord.com/>
-   Snapcraft: <https://snapcraft.io/discord>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-19 Fri&gt;  </span></span>    


### LINE {#line}

-   Ref: [如何在 Ubuntu 20.04 中安裝 LINE 通訊軟體](https://tedliou.com/archives/howto-install-line-on-ubuntu-20-04/)

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-16 Tue&gt;</span></span>  


### Telegram Desktop {#telegram-desktop}

``````sh
sudo snap install telegram-desktop
``````

-   Official Website: <https://telegram.org/>
-   Snapcraft: <https://snapcraft.io/telegram-desktop>

<span class="timestamp-wrapper"><span class="timestamp">&lt;2021-03-29 Mon&gt;</span></span>
