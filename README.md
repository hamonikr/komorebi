
# Komorebi
 
 리눅스 데스크톱에서 애니메이션 배경화면을 사용할 수 있게 해주는 프로그램입니다.

 Animated Wallpapers for Linux

 * upstream : https://github.com/cheesecakeufo/komorebi.git

![app](https://raw.githubusercontent.com/cheesecakeufo/komorebi/master/screenshots/collage.jpg)


# Usage
프로그램 설치 후 `프로그램 메뉴 > komorebi` 를 실행

# Install

## HamoniKR
```
sudo apt update
sudo apt install komorebi
```

## Other Ubuntu based distro
```
# add hamonikr apt repo
wget -qO- https://pkg.hamonikr.org/add-hamonikr.apt | sudo -E bash -

# install
sudo apt install komorebi
```

## Install from source
```
sudo add-apt-repository ppa:gnome3-team/gnome3 -y
sudo add-apt-repository ppa:vala-team -y
sudo add-apt-repository ppa:gnome3-team/gnome3-staging -y

sudo apt install cmake valac libgtk-3-dev libgee-0.8-dev libclutter-gtk-1.0-dev libclutter-1.0-dev libwebkit2gtk-4.0-dev libclutter-gst-3.0-dev

git clone https://github.com/hamonikr/komorebi.git
cd komorebi
mkdir build && cd build
cmake .. && sudo make install && ./komorebi
```


## Change Wallpaper & Desktop Preferences
To change desktop preferences or your wallpaper, right click anywhere on the desktop to show the menu.

![s1](https://raw.githubusercontent.com/cheesecakeufo/komorebi/master/screenshots/preferences.jpg)

## How do I create my own wallpaper?

Komorebi provides a simple tool to create your own wallpapers! Simply, open your apps and search for 'Wallpaper Creator'

![s1](https://raw.githubusercontent.com/cheesecakeufo/komorebi/master/screenshots/wallpaper_creator.jpg)

You can use either an image, a video, or a web page as a wallpaper and you have many different options to customize your very own wallpaper!

## Uninstall

### If you installed a packaged version of Komorebi

1. Open Terminal
2. `sudo apt remove komorebi`

### If you manually installed Komorebi

1. Open Terminal
2. `cd komorebi/build`
3. `sudo make uninstall`

## Questions? Issues?

### Komorebi is slow. What can I do about it?

Komorebi includes support for video wallpapers that might slow your computer down. You can disable support for video wallpapers in 'Desktop Preferences' → uncheck 'Enable Video Wallpapers'.

_note: you need to quit and re-open Komorebi after changing this option_


### After uninstalling, my desktop isn't working right (blank or no icons)

The latest Komorebi should already have a fix for this issue. If you've already uninstalled Komorebi and would like to fix the issue, simply run this (in the Terminal):
`curl -s https://raw.githubusercontent.com/cheesecakeufo/komorebi/master/data/Other/postrm | bash -s`

If your issue has not already been reported, please report it *[`here`](https://github.com/cheesecakeufo/komorebi/issues/new)* and I'll try my best to fix them.

### Why does Komorebi install files in a macOS-like structure?

Komorebi was originally intended to run on an unreleased OS project. Since many people already use Komorebi, an update could potentially break Komorebi and custom-made wallpapers.

It is possible to change the file structure with code changes and a `postinst` script but I'd rather keep it as is for now or if you have the time to make one, feel free to do so and submit a PR!
