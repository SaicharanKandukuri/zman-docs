---
description: 'Xwayland to make thing smooth in termux proot [no-root]'
---

# Xwayland In proot

{% hint style="danger" %}
Xwayland for termux is a project left by termux before release. and a fork is under development. so you may observe a lot of bugs and may experience app crashes  
active maintainer: [https://github.com/suhan-paradkar](https://github.com/suhan-paradkar)
{% endhint %}

## Setting Up apps & dependencies

### Setting up termux

Official f-droid termux may not work for this so get termux from [https://github.com/termux/termux-app/actions](https://github.com/termux/termux-app/actions)

after install do some updates and installations  
Just copy code below in termux and done!

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

for now, this app is available here [https://github.com/suhan-paradkar/termux-wayland/releases](https://github.com/suhan-paradkar/termux-wayland/releases)  
so download and install it

## Using Xwaland to run `proot-distro` linux

{% hint style="info" %}
assuming you installed ubuntu with proot-distro with xfce4 installed
{% endhint %}



