+++
title = "Install GUI in WSL2 using VcXsrv"
author = ["Shawn Dennis Lin"]
date = 2020-12-02T00:00:00+08:00
lastmod = 2020-12-02T11:21:58+08:00
tags = ["wsl", "vcxsrv", "gui"]
categories = ["linux"]
draft = false
hero = "/posts/linux/install_gui_in_wsl2_using_vcxsrv/images/hero.svg"
[menu.sidebar]
  parent = "linux"
  weight = "auto"
  identifier = "install_gui_in_wsl2_using_vcxsrv"
  name = "Install GUI in WSL2 using VcXsrv"
+++

Introduction how to install GUI desktop in WSL2 with VcSxrv in winsows 10.  

<!--more-->


## Install Step {#install-step}


### Install WSL {#install-wsl}

First check if you Windows 10 Version supports WSL 2 or not checkout the [Link](https://docs.microsoft.com/en-us/windows/wsl/install-win10) and Install.  


### Download VcSxrv {#download-vcsxrv}

Download X server connected tool, I use [VcXsrv](https://sourceforge.net/projects/vcxsrv/).  


### Update Ubuntu 20.04 to the latest version {#update-ubuntu-20-dot-04-to-the-latest-version}

```shell
$ sudo apt-get update
$ sudo apt-get upgrade
```


### x-server VcXsrv configuration {#x-server-vcxsrv-configuration}

Open the Ubuntu 20.04 LTS terminal and type below to install XFCE4 Desktop:  

```shell
$ sudo apt-get install x11-apps
$ sudo apt-get install xfce4
```

When you install xfce4, you maybe need to select the Default Display Manager link this:  
![](/ox-hugo/change-the-default-display-manager.png)  
If you don't how to select, you can reference [What is LightDM and GDM](https://unix.stackexchange.com/questions/131496/what-is-lightdm-and-gdm/131497#131497?newreg=7caa2cd48b7b447f8b612ca8a7a13c5a).  

After the installation finished, open .bashrc add some configuration.  

```shell
$ cd ~
$ vi .bashrc
```

Go to the last line and write this  

```bash
export DISPLAY=:0.0
```

and Exit your WSL and run it again.  

Now after we got everything we need, let's start the session  

```shell
$ startxfce4
```

and go back you windows to open VcXsrv main program(XLaunch) you can use you GUI in WSL  
![](/ox-hugo/vcxsrv-init-screen.jpg)  

Congratulations!! Now you can use your WSL using Graphical User Interface.  


## Reference {#reference}

-   [What's the easiest way to run GUI apps on Windows Subsystem for Linux as of 2018?](https://askubuntu.com/questions/993225/whats-the-easiest-way-to-run-gui-apps-on-windows-subsystem-for-linux-as-of-2018)
-   [Window10 建置Ubuntu(WSL2)與GUI桌面配置筆記](https://s123600g.medium.com/window10-%E5%BB%BA%E7%BD%AEubuntu-wsl2-%E8%88%87gui%E6%A1%8C%E9%9D%A2%E9%85%8D%E7%BD%AE%E7%AD%86%E8%A8%98-58796915ed4d)
-   [Installing WSL with GUI using VcXsrv](https://medium.com/@dhanar.santika/installing-wsl-with-gui-using-vcxsrv-6f307e96fac0)
-   [How to Change the Default Display Manager in Ubuntu 20.04](http://ubuntuhandbook.org/index.php/2020/07/change-default-display-manager-ubuntu-20-04/)
-   [What is LightDM and GDM](https://unix.stackexchange.com/questions/131496/what-is-lightdm-and-gdm/131497#131497)
