# Vim Help

- [Vim Help](#vim-help)
  - [Basics](#basics)
    - [Exiting vim](#exiting-vim)
    - [Modes](#modes)
      - [Insert](#insert)
        - [Replace](#replace)
      - [Normal](#normal)
      - [Visual](#visual)
  - [Navigation](#navigation)
    - [Repeat](#repeat)
  - [Searching](#searching)
  - [Find \& Replace](#find--replace)
  - [Selection](#selection)
  - [Copy \& Paste](#copy--paste)
  - [Indentation](#indentation)
  - [Configuration](#configuration)
  - [Tutorials](#tutorials)
  - [Plugins](#plugins)

## Basics

### Exiting vim

First press/spam Escape to go to normal mode!

- `:q` to quit without changes
- `:q!` to quit, discarding any changes
- `:wq` to write any changes and quit
- `:x` practically the same as `wq`, however this only actually writes when changes have been made (and it's shorter ;))

### Modes

- Insert, where you write!
- Normal, where you can exit, thank Bob
- Visual, to select, copy/paste, delete

#### Insert

The most used method to go into insert mode is by simply pressing `i`, for insert.

This will insert the cursor at the position of the cursor.

However, what you will most likely want 9/10 times is _append_ with `a`, which will insert the cursor _after_ the current position.

You can also insert at the beginning of the line with `I`, or at the end of the line with `A`.

Makes sense right?

Insert mode also has some shortcuts. You will probably use `Ctrl+w` to delete the previous word most often.

PS: Did you know `Ctrl+w` has the same effect in most terminals?

##### Replace

With `r` you can replace the character under the cursor. Example `rG`

With `R` you will enter replace mode (insert but overwriting existing text)

#### Normal

Esape to normal mode, never get stuck again in vim.

This is where you _navigate_, search, make small changes/deletions.

#### Visual

Visual mode has several sub-modes, which you can all enter from normal mode (Escape!)

- `v` - Regular visual mode, to work similarly to how you would work in edit mode
- `Shift+v` - Visual line mode, to work with entire lines
- `Ctrl+v` - Visual block mode, to work with, well, _blocks_ of text

## Navigation

H J K L!

- H = Left
- J = Down
- K = Up
- L = Right

Arrow keys work too and function the same...

Use `0` to go the start of a line, and `$` to go the end.

Use `w` to jump to the next word. `W` to jump a word-with-punctuation.and_stuff

Adversely, `b` and `B` to go back.

### Repeat

**You can repeat actions by prepending with a number!**

Examples:

- `5j` will go down 5 lines
- `3W` to jump three words-with-punctuation to the right

## Searching

In normal mode, press `/` to search.

Some symbols have to be escaped...

`n` to go to the next result

`N` to go to the previous!

## Find & Replace

Find and replace all instances:

`:%s/potato/tomato/g`

Explanation:

- `s` stands for substitute
- `%` is a shortcut for using the entire document
- `g` means global; this is required to change _all_ occurrences in a line

Remember `:%s` and don't forget the `g`!

## Selection

In any of the visual modes, just browse around!

Remember you can repeat commands!

`shift+v`, `3k` to select the current line and the 3 lines above it

You can also select from the cursor to a search result:

`v`, `/my-word`

And then execute commands on it:

- `:s/foo/bar/g` will replace all occurrences of foo with bar _in the selection_
- `>` to indent
- `~` to switch case

## Copy & Paste

With a selection, press `y` to yank (aka copy), or `d` to delete!

Then you can paste:

- after the cursor with `p`
- before the cursor with `P`

Remember you can combine this with navigation!

## Indentation

Depends on your `tabstop` settings!

In normal mode:

Indentation, press `>>` or `<<` to indent the current line.

Example: `>5j` to indent the current line and the 5 lines below it.

## Configuration

You can configure vim with a `.vimrc` file in your `$HOME` (`cd ~` should work on every system, including Windows with PowerShell)

Recommended:

```vim
" This is a comment
syntax on

set encoding=UTF-8

set tabstop=8       " This will _display_ actual tabs as 8-wide (default on most systems)
set softtabstop=4
set shiftwidth=4    " This will insert 4 spaces when you press tab.
set expandtab       " This will automatically convert tabs to spaces!
```

Other options:

- `set number` to see line numbers
- `set nonumber` to disable
- `set relativenumber` to show how far away from other lines your cursor is, super convenient for navigation!
- `set norelativenumber` to disable as well

Note that you can tab-complete these options. :)

## Tutorials

- [Vim Cheatsheet at vim.rtorr.com](https://vim.rtorr.com/)
- Try vimtutor! Just run `vimtutor` (NOT in vim), or try `:help vimtutor` (IN vim) for instructions on getting started.
- Also try the [interactive vim tutorial on openvim.com](https://www.openvim.com/)

## Plugins

[Vim Awesome](https://vimawesome.com/) is an _awesome_ site with a list of plug-ins.
