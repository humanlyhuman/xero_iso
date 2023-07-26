# XeroLinux ISO Repo

This is the **Flagship** version of **XeroLinux**. It uses the **KDE Plasma** Desktop environment [Click Here](https://forum.xerolinux.xyz/thread-4.html) for full release info.

You can either build it yourselves following the guide below, that way you always have the latest version available as of build time, if you can't, or prefer not to, you can download the pre-built ISO from the [Official Site](https://xerolinux.xyz).

<p align="center">
    <img width="300" src="https://i.imgur.com/QWqMIsr.png" alt="logo">
</p>

<h1 align="center">Must be on an *Arch* based Distro to build ISO.</h1>

<h3 align="center">||| Note |||<br />
Not all *Arch* based Distros are supported.<br />
Script was tested on <a href="https://archlinux.org">Arch</a>/<a href="https://xerolinux.xyz">XeroLinux</a>/<a href="https://https://arcolinux.com/">ArcoLinux</a> & <a href="https://endeavouros.com/">EndeavourOS</a>
</h3>

![XeroKDE](https://i.imgur.com/ujPgkvC.png)

<h1 align="center">How to build XeroKDE</h1>

## Note before building

If you already are on any version of **XeroLinux**, you do not need to do all this, just use our tool, which has a script that will do it for you. Just launch it, go to **Post-Instal System Config** and click on the **ISO Builder** button, select option *1* **XeroLinux KDE Plasma** and watch it do its magic. Keep a close eye on it while it builds, because you will be prompted for root password, please type it so it can clean up the build environment. Finally your ISO is ready in `~/Xero-Out/` Have fun ! Otherwise follow the guide below...

### Distrobox Option

In case you are on somthing other than **Arch**, or don't want to install Arch to build, you always have **Distrobox** as an option.

Follow the [(Official Guide)](https://distrobox.privatedns.org/#installation) to install it on your specific system, then follow steps below to get the **XeroBuilder** **Arch** container up and running.

Afterwards follow steps 1 & 2 to build the ISO...

- Create The Container :
```
distrobox create -i quay.io/toolbx-images/archlinux-toolbox -n "xerobuilder"
```

- Enter the Container :
```
distrobox enter xerobuilder
```

- Install necessary packages :
```
sudo pacman -Syyu && sudo pacman -S --noconirm neofetch git archiso base base-devel
```

That's it. Now follow below steps to build XeroLinux...

### Step 1 - Clone Build Repo :

Grab the build environment. Just note that you will need Git installed in order to do that.

**Grab Build Env.**
```
cd ~ && git clone https://github.com/xerolinux/xero_iso.git
```

### Step 2 - Building the XeroKDE ISO :

Now that we have build environment on our system, it's time to build it.

**Build ISO :**
```
cd ~/xero_iso/ && ./build.sh
```

Build will take some time depending on your machine's specs, once done you will be prompted for root password, please type it so it can clean up the build environment. Finally your ISO is ready in `~/Xero-Out/` Have fun !

### Support

A lot of hard work, and sleepless nights went into the creation of this awesome Ditro/Spin & build script, with the current situation in **Lebanon** not being so great, I am limited on time & reources, with no other means of income to cover server fees for hosting the sites and repos, I solely rely on your generous contributions. Any amount will go a long way making sure the project continues to thrive. So if you can, please show the project some love, on [**Ko-Fi**](https://ko-fi.com/xerolinux), [**FundRazr**](https://fundrazr.com/xerolinux) or by becoming a [**Github Sponsor**](https://github.com/sponsors/xerolinux).

### Support the team...

If you feel like being extra awesome, please show [**TeddyBearKilla**](https://ko-fi.com/teddybearkilla) and [**Ripl3yPlays**](https://ko-fi.com/ripleyplays) the same love you would show the project, by buying them a **Coffee** or two, they deserve it, thanks...

*May You Live Long & Prosper*...

I hope this helps.. In case of other issues kindly find me on [**Discord**](https://discord.gg/Xg6T78ahtK)

Happy building
