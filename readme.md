# Corne 3x5 Miryoku
Corne 3x5 keyboard with Miryoku key mappings (using Colemak DH keyboard layout).

![Miryoku](https://raw.githubusercontent.com/manna-harbour/miryoku/master/data/cover/miryoku-kle-cover.png)


## How To Use

### Install QMK
```
brew install qmk/qmk/qmk
```

### Setup and Clone QMK Firmware
```
qmk setup
```

### Go to Miryoku folder
```
cd ~/qmk_firmware/users/manna-harbour_miryoku
```

### Add this code in the `config.h` file
```
// Shared OLED and WPM
#define SPLIT_OLED_ENABLE
#define SPLIT_WPM_ENABLE

// Disabled Oneshot modifier
#define NO_ACTION_ONESHOT
```

### Add this code in the `rules.mk` file
```
OLED_ENABLE = yes
OLED_DRIVER = SSD1306

WPM_ENABLE = yes
```

### Add this code in the `manna-harbour_miryoku.c` file
```
#include "keymap.c"
```

### Copy `keymap.c` file in Miryoku folder

### Flashing
```
qmk flash -c -kb crkbd -km manna-harbour_miryoku -e MIRYOKU_CLIPBOARD=MAC
```
