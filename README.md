# White Rabbit

A green-phosphor [Omarchy](https://omarchy.org/) theme: dimmed phosphor green
on near-black, a desaturated cyan accent, and digital-rain backgrounds —
Kid's Story terminal, not a movie poster.

![preview](preview.png)

| The HUD menu | The digital-rain screensaver |
|---|---|
| ![menu](preview-menu.png) | ![screensaver](preview-rain.png) |

The HUD window frames, the menu, the screensaver, the CRT and glow overlays
and the cursors in these screenshots come from
[White Rabbit extras](https://github.com/cycclon/omarchy-white-rabbit-extras),
a separate repository. This one is only the theme, and it works on its own.

## What's in it

- **Palette** (`colors.toml`) — dimmed phosphor green text, a cyan accent,
  and green-shifted ANSI colors so terminal output stays on-theme.
- **Shell chrome** (`shell.*.toml`) — bar, menu, launcher, lock screen,
  notifications, popups, tooltips and controls, all from the same palette.
- **GTK styling** (`gtk.css`, `gtk4.css`) and the Yaru icon theme
  (`icons.theme`). GTK 4 context menus get the HUD frame: chamfered cyan
  outline, green text, and a 75% fill that Hyprland frosts.
- **Four backgrounds** (`backgrounds/`) — two digital-rain renders, a dense
  "code wall," and the Arch Linux logo formed out of the rain, sized for
  2560×1440 and up.
- **Reference configs** — `hyprland.lua.example` and `foot.ini.example`.
  Omarchy doesn't load these from a git-cloned theme; they document the full
  setup, and the extras installer puts them in place.

## Install

```sh
omarchy theme install https://github.com/cycclon/omarchy-white-rabbit-theme
```

That gives you the palette, the GTK and shell colors, and the backgrounds,
with Omarchy's standard window borders.

For the full look in the screenshots, install
[White Rabbit extras](https://github.com/cycclon/omarchy-white-rabbit-extras)
instead: its installer sets up this theme too, together with the Hyprland
config above, the window frames, the overlays, the screensaver, the menu and
the cursors. It runs code on your machine, so read its README first.

### Requirements

- **Omarchy.**
- **`yaru-icon-theme`** — named by `icons.theme`. Purely cosmetic; without it
  GTK apps keep whatever icon theme you already had.

## Configuration

`~/.config/omarchy/themes/white-rabbit/colors.toml` is a standard Omarchy
palette file — the usual `foreground` / `background` / `accent` / ANSI
16-color keys. Each shell surface has its own override file read
independently:

| File                       | Surface                                 |
|----------------------------|-----------------------------------------|
| `shell.bar.toml`           | top bar                                 |
| `shell.menu.toml`          | Omarchy menu (Super key)                |
| `shell.launcher.toml`      | app launcher                            |
| `shell.lock.toml`          | lock screen                             |
| `shell.notifications.toml` | notification cards                      |
| `shell.popups.toml`        | generic popups                          |
| `shell.tooltip.toml`       | tooltips                                |
| `shell.controls.toml`      | hover/focus/selected states on controls |

Edit any of these under the installed theme directory and re-run
`omarchy theme set white-rabbit` to apply.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Changes to the plugins, window
frames, cursors or installer go to
[White Rabbit extras](https://github.com/cycclon/omarchy-white-rabbit-extras).

## License

MIT — see [LICENSE](LICENSE). Contributions are accepted under the same
license.
