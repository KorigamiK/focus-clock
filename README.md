# Focus Clock

Bigass clock that sits on top of all windows to help you focus.

![Screenshot](./.github/screenshot.png)

## Building

Requires Gtkmm4, gtk4-layer-shell, CMake, pkg-config.

```
mkdir build
cd build
cmake ..
make
```

You might also wanna add the following or Hyprland window rules to your wm or similar:

```
windowrule = noblur, focusclock
windowrule = noborder, focusclock
windowrule = pin, focusclock
windowrule = noshadow, focusclock
bind = $mainMod ALT, M, exec, killall -SIGTERM focusclock || focusclock -br -B 70 
```

## Usage

You can configure the position of the clock using the following command-line options:

```sh
Usage:
  focusclock [OPTION?]

Help Options:
  -h, --help              Show help options

Application Options:
  -t, --anchor-top        Anchor to the top edge
  -b, --anchor-bottom     Anchor to the bottom edge
  -l, --anchor-left       Anchor to the left edge
  -r, --anchor-right      Anchor to the right edge
  -T, --margin-top        Margin from the top edge
  -B, --margin-bottom     Margin from the bottom edge
  -L, --margin-left       Margin from the left edge
  -R, --margin-right      Margin from the right edge
```

# References

- https://github.com/nwg-piotr/nwg-wrapper/
- https://github.com/wmww/gtk4-layer-shell/
- https://www.gtk.org/docs/language-bindings/cpp

## License

GNU GPL3+
