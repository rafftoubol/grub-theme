# Grub-Theme

**Grub-Theme Serves as a repository of each grub theme I create and my configurations,
if you like a theme please use it and leave a star**

### Grub Theme taxonomy

```
theme-name/
├── theme.txt          # Main configuration file
├── background.png     # Background image
├── boot_menu_*.png    # Menu item images
├── progress_*.png     # Progress bar images
└── fonts/            # Custom fonts (optional)
    └── font.pf2
```

_Please see the themes in this repo for a guide on what should go in the theme.txt,
and so on to create your own_

## Installation

1. Clone the repo & move to the right location
   > [!INFO]
   > if you prefer to sym-link just do that, I wont put the steps here because I do not prefer it

```Bash
Git clone github.org/rafftoubol/grub-theme/{theme-name}
cd ..
cp or mv {theme-name} /boot/grub/themes/

```

> [!TIP]
> If you dont have the destination directory (/themes/) just create it

---

2. edit _*/etc/default/grub*_

```Bash
GRUB_THEME="/boot/grub/themes/{theme-name}/theme.txt"
GRUB_GFXMODE="3200x2000" ###Or Whatever your resolution is
```

> [!TIP]
> If you change the resolution above in theme.txt modify the boot_menu left,top,width,height positions
> to suit your screen size so the background and menu items are placed correctly 3.

---

3.

```Bash
sudo update grub
```
