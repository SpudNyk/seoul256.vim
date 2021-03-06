```
"  _____             _ ___ ___ ___      "
" |   __|___ ___ _ _| |_  |  _|  _|     "
" |__   | -_| . | | | |  _|_  | . |     "
" |_____|___|___|___|_|___|___|___|.vim "
```

seoul256.vim ![travis-ci](https://travis-ci.org/junegunn/seoul256.vim.svg?branch=master)
------------

*seoul256.vim* is a low-contrast Vim color scheme based on [Seoul Colors](http://www.seoul.go.kr/v2012/seoul/symbol/color.html).
Works on 256-color terminal or on GVim.

### seoul256

![seoul256](https://raw.github.com/junegunn/i/master/seoul256.png)

### seoul256 (light version)

![seoul256-light](https://raw.github.com/junegunn/i/master/seoul256-light.png)

Installation
------------

Use your favorite plugin manager.

- [vim-plug](https://github.com/junegunn/vim-plug)
  1. Add `Plug 'junegunn/seoul256.vim'` to .vimrc
  2. Run `:PlugInstall`

Color schemes
-------------

```vim
" Unified color scheme (default: dark)
colo seoul256

" Light color scheme
colo seoul256-light

" Switch
set background=dark
set background=light
```

Change background color
-----------------------

![seoul256-bg](https://raw.github.com/junegunn/i/master/seoul256-bg.png)

```vim
" seoul256 (dark):
"   Range:   233 (darkest) ~ 239 (lightest)
"   Default: 237
let g:seoul256_background = 236
colo seoul256

" seoul256 (light):
"   Range:   252 (darkest) ~ 256 (lightest)
"   Default: 253
let g:seoul256_background = 256
colo seoul256
```

If `g:seoul256_background` is set, seoul256 will choose the right version based
on the value and `set background=dark/light` will not switch versions.

If you'd like to switch versions with custom background colors, set
`g:seoul256_background` to be a dark value, and additionally define
`g:seoul256_light_background` for seoul256-light.

```vim
let g:seoul256_background = 233
let g:seoul256_light_background = 256

colo seoul256
colo seoul256-light
```

Current background color
------------------------

When loaded, soul256.vim will set up two global variables so that you can use
them to customize other plugins:

- `g:seoul256_current_fg` - Current foreground color in ANSI code
- `g:seoul256_current_bg` - Current background color in ANSI code

iTerm2 color scheme
-------------------

- [Official iTerm2 color scheme](iterm2/seoul256.itermcolors)
- [seoul256-iTerm2](https://github.com/mikker/seoul256-iTerm2) by
[Mikkel Malmberg](https://github.com/mikker).

Author
------

Junegunn Choi

License
-------

MIT
