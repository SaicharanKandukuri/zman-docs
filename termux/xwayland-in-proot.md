---
description: 'Xwayland to make thing smooth in termux proot [no-root]'
---

# Xwayland In proot

{% hint style="danger" %}
Termux:Xwayland app for termux is a project left by termux before release. and a fork of it is under development. as lot of it is old and less polished you may observe a lot of bugs and may experience app crashes  
active maintainer: [https://github.com/suhan-paradkar](https://github.com/suhan-paradkar)

\[ Upadate \]: termux:x11main branch is back under maintainanece 
{% endhint %}

## Setting up apps & dependencies

### Setting up termux

Official f-droid termux may not work for this so get termux from [https://github.com/termux/termux-app/actions](https://github.com/termux/termux-app/actions)

after install do some updates and installations  
Just copy the code below in termux and done!

```bash
pkg install x11-repo wget -y
wget https://github.com/suhan-paradkar/xwayland4tewmux/releases/download/xwayland/libwayland-protocols_1.17-4_$(dpkg --print-architecture).deb
wget https://github.com/suhan-paradkar/xwayland4tewmux/releases/download/xwayland/libwayland_1.19.0_$(dpkg --print-architecture).deb
wget https://github.com/suhan-paradkar/xwayland4tewmux/releases/download/xwayland/xwayland_1.20.5-6_$(dpkg --print-architecture).deb
pkg in ./libwayland-protocols_1.17-4_$(dpkg --print-architecture).deb ./libwayland_1.19.0_$(dpkg --print-architecture).deb ./xwayland_1.20.5-6_$(dpkg --print-architecture).deb
```

{% hint style="success" %}
Setting termux is done ✌️
{% endhint %}

### Setting up Termux:Xwayalnd app

for now, this app is available here [https://github.com/termux/termux-x11/actions](https://github.com/termux/termux-x11/actions)  
so download and install it

## Using Termux:Xwayland to run `proot-distro` Linux

{% hint style="info" %}
assuming you installed ubuntu with proot-distro with xfce4 installed
{% endhint %}

> Here starts setp by step process

Open termux app the minimize it and open Termux:Xwayland app  
then open termux and use 

```bash
export XDG_RUNTIME_DIR=$TMPDIR
Xwayland :0 
```

this starts connection at port :0  
Open a new session then start your prooted Linux

```bash
proot-distro login hippo --shared-tmp
# you can replace hippo
# you can use hippo --shared-tmp
```

export DISPLAY value to :0

```bash
export DISPLAY=:0
```

then invoke your de start script. for xfce4 it is startxfce4 and others may differ

```bash
startxfce4
```

{% hint style="success" %}
That's all now if you open minimized Xwayland:Termux app you see xfce4 running
{% endhint %}

## Show some love 💖⭐

even it's a fork [@suhan-paradkar ](https://github.com/suhan-paradkar)managed to make a private reboot and make it work. it would be great if you show some love by staring his GitHub repo  
if you are a Wayland or linux expert make sure to help this tiny platform where people try to do these kind of  uncommon things

## Further sources

{% embed url="https://github.com/suhan-paradkar/termux-wayland/wiki/Launching-GUI-applications" caption="suhan-paradkar guide on starting wayland" %}

{% embed url="https://github.com/termux/termux-x11" caption="termux:x11 Github repo" %}

{% embed url="https://at.projects.genivi.org/wiki/display/DIRO/Wayland+Application+on+Android" %}



  


