---
layout: page
title: Set random unsplash image as wallpaper
image: /image/a1.png
description: Unsplash images are awesome. They deserve to be your wallpaper.
---

[Lorem picsum](https://picsum.photos) is a great website to get a random image from [Unsplash](https://unsplash.com). It even lets you choose a size. Which begs to be used as the source of wallpapers.

**Ubuntu** (gnome)
```sh
wget https://picsum.photos/1366/768/\?random -O ~/wallpaper.jpg && gsettings set org.gnome.desktop.background picture-uri ~/wallpaper.jpg
```

We're using `wget` to download an image of size 1366x768 at `~/wallpaper.jpg` and then setting it via `gsettings` which is the gnome-way.

To change your wallpaper every hour, add this to `crontab`
```sh
0 * * * * wget https://picsum.photos/1366/768/\?random -O ~/wallpaper.jpg && gsettings set org.gnome.desktop.background picture-uri ~/wallpaper.jpg
```

