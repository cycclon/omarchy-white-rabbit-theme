# Contributing

Thanks for considering it. This is a personal theme shared in case it's
useful to someone else, not a project with a team behind it -- so the
process is deliberately small.

## The short version

1. Fork the repo.
2. Make your change on a branch.
3. Open a pull request describing what changed and why.
4. It gets reviewed and merged, asked for changes, or closed with an
   explanation. Every PR is read; not every PR is merged.

Forking, cloning, and running your own modified copy needs no permission --
the license already grants that. Getting a change merged back into this
repo is the one thing that goes through review.

## What belongs here

Only theme files: the palette, backgrounds, previews, the app theme files
Omarchy reads, and the `.example` reference configs. Nothing that runs --
no scripts, plugins or build tools -- so the theme can be listed in
Omarchy's gallery. The plugins, window frames, cursors and installer live in
[White Rabbit extras](https://github.com/cycclon/omarchy-white-rabbit-extras);
send changes to those there.

## Before opening a PR

- **Include a screenshot.** Almost everything here is visual; a before and
  after makes a color or background change easy to judge.
- **Keep backgrounds light.** WebP, sized for 2560×1440 and up, re-encoded
  with `magick input.png -strip -resize '3840>' -quality 82 output.webp`.
- **Keep `hyprland.lua.example` in step with the extras.** Its plugin and
  cursor settings document what the extras installer sets up.
