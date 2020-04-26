# Rusk's build of st - the simple (suckless) terminal

The [suckless terminal (st)](https://st.suckless.org/) with some additional features that make it literally the best terminal emulator ever:

## (Somewhat) unique features (using dmenu) (stolen from [Luke's build of st](https://www.github.com/lukesmithxyz/st))

+ **follow urls** by pressing `alt-l`
+ **copy urls** in the same way with `alt-y`
+ **copy the output of commands** with `alt-o`

## Other features

+ [**VimBrowse**](http://st.suckless.org/patches/vim_browse/) - by pressing `alt+shift+c` you enter into `normalmode` where using vim keys, you can scroll through your history and do vim commands (yi{ for example)

## Bindings for

+ **scrollback** with `alt-↑/↓` or `alt-pageup/down` or `shift` while scrolling the mouse
+ OR **vim-bindings**: scroll up/down in history with `alt-k` and `alt-j`. Faster with `alt-u`/`alt-d`.
+ **zoom/change font size**: same bindings as above, but holding down shift as well. `alt-home` returns to default
+ **copy text** with `alt-c`, **paste** is `alt-v` or `shift-insert`

## Pretty stuff

+ Default [dracula](https://dracula) colors.
+ AlphaFocusHighlight, two difference alpha values, one for when the terminal is focused, one when the terminal is not.
+ Default font is system "mono" at 14pt, meaning the font will match your system font.

## Other st patches

+ Vertcenter
+ Scrollback (via vimbrowse)
+ Font2
+ Anysize

## Installation

```
git clone https://github.com/lordrusk/st
cd st
sudo make install
```

Obviously, `make` is required to build. `fontconfig` is required for the default build, since it asks `fontconfig` for your system monospace font.  It might be obvious, but `libX11` and `libXft` are required as well. Chances are, you have all of this installed already.

## Notes on Emojis and Special Characters

If st crashes when viewing emojis, install [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/) from the AUR.

Note that some special characters may appear truncated if too wide. You might want to manually set your prefered emoji/special character font to a lower size in the `config.h` file to avoid this. By default, JoyPixels is used at a smaller size than the usual text.
