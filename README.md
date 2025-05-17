# dansusman's zmk-config

This is my personal configuration for keyboards with ZMK firmware support. I'm
currently using a 42-key 3x6 Corne with Magic Sturdy base layer, heavily
inspired by the following GOATs.

- [getreuer](https://getreuer.info): Incredibly educational blog posts on all
things split keyboard
- [urob](https://github.com/urob/zmk-config): Wildly innovative ZMK setup with
custom macros for fancy things

## Layout 

![Dan's keymap, illustrated](./draw/keymap.svg)

I'm trying out Pascal Getreuer's
[flavor](https://getreuer.info/posts/keyboards/alt-layouts/index.html#magic-sturdy)
of Magic Sturdy right now, blending with some of ikcelaks's
[flavor](https://github.com/Ikcelaks/keyboard_layouts/blob/main/magic_sturdy/magic_sturdy.md)

This repo, at time of writing, is nearly a direct port of getreuer's QMK config.

## Usage

1. Build a ZMK board
2. Use GitHub Action to generate firmware
    - I found out after 53 commits that I could've (should've?) been doing this
    locally via [`act`](https://github.com/nektos/act)
    - Instead of pushing to remote, letting GitHub run the jobs and spit out
    the firmware, it's probably easier/faster/fewer public failures to just run
    them locally. You'll be using your own resources of course, but computers
    are fast nowadays.
3. Download firmware files
4. Plug in left half of board and hit reset button
5. Board will show up in file system as a valid destination
6. Copy left side firmware files to board; it will auto eject itself
7. Repeat for right half as needed

