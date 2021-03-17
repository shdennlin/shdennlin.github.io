+++
title = "Linux Install Application"
author = ["Shawn Dennis Lin"]
date = 2020-11-19T00:00:00+08:00
lastmod = 2021-01-13T03:55:22+08:00
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

These are the applications I installed in linux. If you have any questions about these apps, you can contact me.  

<!--more-->


## My Install Application in Linux {#my-install-application-in-linux}


### ag {#ag}

A code searching tool similar to ack, with a focus on speed.  

```shell
sudo apt-get install -y silversearcher-ag
```

-   GitHub: [ggreer/the\_silver\_searcher](https://github.com/ggreer/the%5Fsilver%5Fsearcher)


### Anaconda {#anaconda}

```shell
cd ~/Downloads
wget https://repo.anaconda.com/archive/Anaconda3-2020.02-Linux-x86_64.sh
bash ~/Dwonloads/Anaconda3-2020.02-Linux-x86_64.sh
conda create -n tf-gpu tensorflow-gpu
conda activate tf-gpu
```


### Angry IP scanner {#angry-ip-scanner}

-   GitHub: [angryip/ipscan](https://github.com/angryip/ipscan/tree/3.7.2)
-   Ref: [Angry IP Scanner](https://angryip.org/about/)


### BingWall - Bing wallpaper of the day {#bingwall-bing-wallpaper-of-the-day}

```shell
sudo snap install bing-wall
```

-   Ref: [BingWall - Bing wallpaper of the day](https://snapcraft.io/bing-wall)


### boot-repair {#boot-repair}

```shell
sudo add-apt-repository ppa:yannubuntu/boot-repair &&\
sudo apt-get update &&\
sudo apt-get install -y boot-repair && boot-repair
```

-   Ref: [Boot-Repair](https://help.ubuntu.com/community/Boot-Repair)


### bpytop {#bpytop}

Resource monitor that shows usage and stats for processor, memory, disks, network and processes. Python port of bashtop.  

```shell
cd ~/Downloads &&\
git clone https://github.com/aristocratos/bpytop.git &&\
cd bpytop &&\
sudo make install
```

-   GitHub: [aristocratos/bpytop](https://github.com/aristocratos/bpytop)


### Crow Translate {#crow-translate}

A small translate tool like QTranslate.  

```shell
cd ~/Downloads &&\
git clone https://aur.archlinux.org/crow-translate.git
cd crow-translate
makepkg -si
```

-   GitHub: [crow-translate/crow-translate](https://github.com/crow-translate/crow-translate)
-   Ref: [Crow Translate](https://crow-translate.github.io/)


### Discord {#discord}

```shell
cd ~/Downloads &&\
wget -O discord.deb "https://discordapp.com/api/download?platform=linux&format=deb" &&\
sudo dpkg -i discord.deb
```

-   Ref: [Discord](https://discord.com/)


### dotfiles {#dotfiles}

```shell
mkdir ~/.dotfiles &&\
git clone https://github.com/shdennlin/dotfiles.git ~/.dotfiles/. &&\
cd ~/.dotfiles &&\
bash install.sh &&\
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```

-   GitHub: [shdennlin/dotfiles](https://github.com/shdennlin/dotfiles)


### extra-cmake-modules {#extra-cmake-modules}

```shell
cd ~/Downloads &&\
git clone https://github.com/KDE/extra-cmake-modules.git &&\
cd extra-cmake-modules &&\
mkdir build &&\
cd build &&\
cmake ..  &&\
make &&\
sudo make install
```

-   GitHub: [KDE/extra-cmake-modules](https://github.com/KDE/extra-cmake-modules)


### fcitx & boshiamy {#fcitx-and-boshiamy}

```shell
sudo apt-get install -y fcitx fcitx-table-boshiamy fcitx-chewing
```

-   Ref: [Linux Ubuntu 嘸蝦米輸入法的FCITX安裝](https://thorasgard520.blogspot.com/2019/04/linux-ubuntu-fcitx.html)


### flatpak {#flatpak}

```shell
sudo apt install -y flatpak
```

-   Ref: [flatpak](https://zh.wikipedia.org/wiki/Flatpak)(wiki)


### font {#font}

```shell
cd ~/Downloads &&\
git clone https://github.com/shdennlin/linux-configuration.git &&\
cd ~/Downloads/linux-configuration/fonts &&\
bash install.sh
```

-   GitHub: [shdennlin/linux-configuration](https://github.com/shdennlin/linux-configuration)


### FreeCAD {#freecad}

```shell
sudo apt install -y freecad
```


### FSearch {#fsearch}

```shell
sudo add-apt-repository ppa:christian-boxdoerfer/fsearch-daily &&\
sudo apt-get update &&\
sudo apt install fsearch-trunk
```

-   GitHub: [cboxdoerfer/fsearch](https://github.com/cboxdoerfer/fsearch)


### gdrive {#gdrive}

```shell
cd ~/Downloads &&\
wget -O drive https://drive.google.com/uc?id=0B3X9GlR6Embnb095MGxEYmJhY2c &&\
sudo install drive /usr/local/bin/drive
```

-   GitHub: [prasmussen/gdrive](https://github.com/prasmussen/gdrive)
-   Ref: [如何在終端機介面使用 Google Drive (gdrive cmd)](https://hiraku.tw/2020/01/5894/)


### Git {#git}

```shell
sudo apt-get -y install git
```


### GitKraken {#gitkraken}

```shell
wget https://release.gitkraken.com/linux/gitkraken-amd64.deb ~/Downloads &&\
sudo dpkg -i ~/Downloads/gitkraken-amd64.deb
```

-   Ref: [GitKrakon](https://www.gitkraken.com/)


### GNOME {#gnome}

```shell
sudo apt install -y gnome-tweaks gnome-shell-extensions &&\
sudo apt install -y chrome-gnome-shell &&\
sudo apt purge gnome-shell-extenion-appindicator 

sudo apt install gnome-shell-extension-pixelsaver &&\
sudo apt install gnome-shell-extension-remove-dropdown-arrows &&\
sudo apt install gnome-shell-extension-system-monitor &&\
sudo apt install gnome-shell-extension-prefs &&\
sudo apt-get install gnome-shell-pomodoro
```

-   Ref: [針對Gnome 3的Linux桌面進行美化](https://www.itread01.com/content/1544311459.html)


### Java {#java}

Preparation: Download jre-8u251-linux-x64.tar.gz  
Download location: [Java Downloads for Linux](https://java.com/en/download/linux%5Fmanual.jsp)   

```shell
cd /usr &&\
sudo mkdir java &&\
cd java &&\
sudo mv ~/Downloads/jre-8u251-linux-x64.tar.gz . &&\
sudo tar zxvf jre-8u251-linux-x64.tar.gz &&\
sudo rm -rf jre-8u251-linux-x64.tar.gz
```

-   Preparation: Download jre-8u251-linux-x64.tar.gz
-   Ref: [Java Downloads for Linux](https://java.com/en/download/linux%5Fmanual.jsp)


### KiCad {#kicad}

```shell
sudo add-apt-repository --yes ppa:js-reynaud/kicad-4 ; &&\
sudo apt-get update ; &&\
sudo apt-get install -y kicad
```

-   Ref: [KiCad Install on Ubuntu](https://kicad.org/download/ubuntu/)


### Latex {#latex}

```shell
sudo apt-get install texlive-base &&\
sudo apt-get install texlive-latex-recommended &&\
sudo apt-get install texlive &&\
sudo apt-get install texlive-latex-extra &&\
sudo apt-get install texlive-xetex
```

-   Ref: [How to install LaTex on Ubuntu 20.04 Focal Fossa Linux](https://linuxconfig.org/how-to-install-latex-on-ubuntu-20-04-focal-fossa-linux)


### Linux Advanced Power Management (TLP) {#linux-advanced-power-management--tlp}

TLP is a feature-rich command line utility for Linux, saving laptop battery power without the need to delve deeper into technical details.  

TLP’s default settings are already optimized for battery life and implement Powertop’s recommendations out of the box. So you may just install and forget it.  

Nevertheless TLP is highly customizable to fulfil your specific requirements.  

```shell
sudo add-apt-repository ppa:linrunner/tlp &&\
sudo apt update &&\
sudo apt install tlp tlp-rdw &&\
sudo apt-get install smartmontools &&\
sudo systemctl start tlp &&\
sudo tlp-stat | less
```

-   Ref: [linux tlp tutorial](https://github.com/twtrubiks/linux-note/tree/master/linux-tlp-tutorial)
-   Ref: [TLP - Optimize Linux Laptop Battery Life](https://linrunner.de/tlp/)


### linux-wifi-hotspot {#linux-wifi-hotspot}

```shell
git clone https://github.com/lakinduakash/linux-wifi-hotspot
cd linux-wifi-hotspot

#build binaries
make

#install
sudo make install
```

-   GitHub: [lakinduakash/linux-wifi-hotspot](https://github.com/lakinduakash/linux-wifi-hotspot)


### Logitech MX Master {#logitech-mx-master}

First:  

```shell
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
```

Second:  

```shell
mkdir -p ~/Downloads/logitech-mouse-config &&\
git clone https://github.com/shdennlin/logitech-mouse-config.git ~/Downloads/logitech-mouse-config/ &&\
cd ~/Downloads/logitech-mouse-config/ &&\
bash install.sh
```

-   GitHub: [shdennlin/logitech-mouse-config](https://github.com/shdennlin/logitech-mouse-config)
-   Ref: See GitHub


### MusixMatch {#musixmatch}

```shell
sudo snap install musixmatch
```

-   GitHub:
-   Ref: [Install Musixmatch on your Linux distribution](https://snapcraft.io/musixmatch)


### nomacs {#nomacs}

nomacs is a free, open source image viewer, which supports multiple platforms. You can use it for viewing all common image formats including RAW and psd images.  

```shell
sudo apt install nomacs &&\
sudo apt-get install nomacs-l10n
```

-   Ref: [nomacs.org](https://nomacs.org/%5C)


### nvtop {#nvtop}

Nvtop stands for NVidia TOP, a (h)top like task monitor for NVIDIA GPUs. It can handle multiple GPUs and print information about them in a htop familiar way.  

```shell
sudo apt install -y nvtop
```

-   GitHub: [Syllo/nvtop](https://github.com/Syllo/nvtop)


### Okular {#okular}

Okular is a universal document viewer developed by KDE. Okular works on multiple platforms, including but not limited to Linux, Windows, macOS, \*BSD, etc.  

```shell
sudo apt-get install okular
```

-   Ref: [okular.kde.org](https://okular.kde.org/)


### Open Broadcaster Software Studio (OBS) {#open-broadcaster-software-studio--obs}

Free and open source software for video recording and live streaming.  

```shell
sudo add-apt-repository ppa:obsproject/obs-studio ;\
sudo apt update ;\
sudo apt install -y obs-studio
```

-   Ref1: [obsproject.com](https://obsproject.com/)
-   Ref2: [9 Best Screen Recorders For Linux](https://itsfoss.com/best-linux-screen-recorders/)


### rar, zip {#rar-zip}

```shell
apt-get install -y unrar &&\
sudo apt install -y p7zip-full
```


### screenfetch {#screenfetch}

screenFetch is a "Bash Screenshot Information Tool". This handy Bash script can be used to generate one of those nifty terminal theme information + ASCII distribution logos you see in everyone's screenshots nowadays. It will auto-detect your distribution and display an ASCII version of that distribution's logo and some valuable information to the right. There are options to specify no ASCII art, colors, taking a screenshot upon displaying info, and even customizing the screenshot command! This script is very easy to add to and can easily be extended.  

```shell
apt install screenfetch
```

-   GitHub:  [KittyKatt/screenFetch](https://github.com/KittyKatt/screenFetch)


### spacemacs {#spacemacs}

Spacemacs is a new way to experience Emacs -- a sophisticated and polished set-up focused on ergonomics, mnemonics and consistency.  

Just clone it, launch it, then press the space bar to explore the interactive list of carefully-chosen key bindings. You can also press the home buffer's [?] button for some great first key bindings to try.  

Spacemacs can be used naturally by both Emacs and Vim users -- you can even mix the two editing styles. Switching easily between input styles makes Spacemacs a great tool for pair-programming.  

Spacemacs is currently in beta, and contributions are very welcome.  

```shell
git clone -b develop https://github.com/syl20bnr/spacemacs.git ~/.emacs.d &&\
git clone https://github.com/bitjockey42/spacemacs-jekyll.git ~/.emacs.d/private/jekyll &&\
git clone https://github.com/shdennlin/spacemacs-private.git ~/.spacemacs.d
```

-   GitHub1: [syl20bnr/spacemacs](https://github.com/syl20bnr/spacemacs)
-   GitHub2: [shdennlin/spacemacs-private](https://github.com/shdennlin/spacemacs-private)
-   Ref: [spacemacs.org](https://www.spacemacs.org/)


### Spotify {#spotify}

```shell
sudo apt install -y snapd &&\
sudo snap install spotify
```


### Tensorflow-gpu {#tensorflow-gpu}

```shell
cd ~/Downloads
wget http://tw.download.nvidia.com/XFree86/Linux-x86_64/440.82/NVIDIA-Linux-x86_64-440.82.run
```

-   Ref: [Installing TensorFlow 2 with GPU support on Ubuntu 20.04 LTS](https://illya13.github.io/RL/tutorial/2020/04/26/installing-tensorflow-on-ubuntu-20.html)


### Terminator {#terminator}

Originally created and developed for a long time by Chris Jones, the goal of this project is to produce a useful tool for arranging terminals. It is inspired by programs such as gnome-multi-term, quadkonsole, etc. in that the main focus is arranging terminals in grids (tabs is the most common default method, which Terminator also supports).  

Much of the behaviour of Terminator is based on GNOME Terminal, and we are adding more features from that as time goes by, but we also want to extend out in different directions with useful features for sysadmins and other users. If you have any suggestions, please file wishlist bugs! (see below for the address)  

```shell
sudo apt install terminator
```

-   Ref: [Introduction-Terminator](https://gnometerminator.blogspot.com/p/introduction.html)


### update & upgrade {#update-and-upgrade}

```shell
sudo apt-get update && sudo apt-get -y upgrade
```

or  

```shell
sudo apt-get update && sudo apt-get -y dist-upgrade
```

-   Ref: [APT upgrade 和 dist-upgrade 的差別](https://blog.longwin.com.tw/2008/03/debian%5Fubuntu%5Fapt%5Fdist%5Fupgrade%5Fdifference%5F2008/)


### Vim {#vim}

```shell
sudo apt-get install vim
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```

-   Ref: [shdennlin/dotfiles](https://github.com/shdennlin/dotfiles)


### Wine {#wine}

Wine (originally an acronym for "Wine Is Not an Emulator") is a compatibility layer capable of running Windows applications on several POSIX-compliant operating systems, such as Linux, macOS, & BSD. Instead of simulating internal Windows logic like a virtual machine or emulator, Wine translates Windows API calls into POSIX calls on-the-fly, eliminating the performance and memory penalties of other methods and allowing you to cleanly integrate Windows applications into your desktop.  

-   Ref: [Supported Wine](https://wiki.winehq.org/Download)
-   Ref: [winehq.org](https://wiki.winehq.org)


### xclip {#xclip}

xclip is a command line interface to the X11 clipboard. It allows you to put the output of a command directly into the clipboard so that you don't have to copy&paste from the terminal manually (which can be a tedious task especially if the output is very long). It also allows you to put the contents of a file directly into the clipboard.  

```shell
sudo apt-get install -y xclip
```

-   Ref: [Command-Line Copy&Paste With xclip (Debian/Ubuntu)](https://www.howtoforge.com/command-line-copy-and-paste-with-xclip-debian-ubuntu)
