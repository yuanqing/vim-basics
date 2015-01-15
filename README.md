# Vim Basics

> Just the basics to get you up and running with Vim.

## Workflow

A barebones workflow is as follows:

1. Launch Vim via the terminal:

  ```bash
  $ vim Main.java
  ```

  You are now in Vim&rsquo;s **Command** mode (also known as **Normal** mode).

2. To start typing into the file, you need to switch to Vim&rsquo;s **Insert** mode. Press `i` to do so. Now, whatever you type will appear as you would expect in a text editor.

3. As soon as you are done typing, press `<Esc>` to switch back to **Command** mode. (The `<Esc>` key is your friend; hitting `<Esc>` will always bring you back to **Command** mode.)

3. And, well, that&rsquo;s it, really! Type `:w` to save the file, and `:q!` to quit Vim.

## Commands

Virtually all operations in Vim happen in **Command** mode. The key commands you must know are:

- `<Ctrl>` + `u` and `<Ctrl>` + `d` to page up and down the file (faster than using the <code>&uarr;</code> and <code>&darr;</code> arrow keys)
- `W` and `b` to move the cursor across words (faster than using the <code>&larr;</code> and <code>&rarr;</code> arrow keys)
- `0` and `$` to move the cursor to the start and end of the current line
- `yy` to copy the current line, and `p` to paste
- `dd` to delete the current line
- `u` to undo, and `<Ctrl>` + `r` to redo
- `gg=G` to auto-indent the file
- `:w` to save the file, `:wq!` to save and quit, and `:q!` to quit without saving

More commands are listed below.

### Moving around the file

Action | Key
:------|:----
Page up | `<Ctrl>` + `u`
Page down | `<Ctrl>` + `d`
Move the cursor to the next word | `W`
Move the cursor to the previous word | `b`
Move the cursor to the start of the current line | `0`
Move the cursor to the end of the current line | `$`
Move the cursor to a particular line (eg. line number 9) | `9G`

### Delete

Action | Key
:------|:----
Delete the current line | `dd`
Delete the character under the cursor | `x`

### Copy and paste

Action | Key
:------|:----
Copy the current line | `yy`
Copy a particular number of lines, starting from the current line (eg. 3 lines) | `3yy`
Paste | `p`

### Undo/redo

Action | Key
:------|:----
Undo | `u`
Redo | `<Ctrl>` + `r`

### Save and quit

Action | Key
:------|:----
Save the file | `:w`
Save the file then quit | `:wq!`
Quit without saving the file | `:q!`

### Find and replace

Action | Key
:------|:----
Search the file for a keyword (eg. &ldquo;foo&rdquo;) | `/foo`
Move to the next match | `n`
Move to the previous match | `N`
Replace all instances of a keyword (eg. replace &ldquo;foo&rdquo; with &ldquo;bar&rdquo;) | `%s/foo/bar/g`

### Text formatting

Action | Key
:------|:----
Auto-indent the file | `gg=G`
Enable smart indenting | `:set smartindent`
Insert spaces on pressing `<Tab>` | `:set expandtab`
Set the number of spaces to insert on pressing `<Tab>` (eg. 2 spaces) | `:set tabstop=2`

### Display settings

Action | Key
:------|:----
Turn on syntax highlighting | `:syntax on`
Display line numbers | `:set number`

## Settings

Various settings (eg. syntax highlighting) can be persisted by putting them in a file called `.vimrc` in your home directory.

Your `~/.vimrc` might be as follows:

```viml
syntax on

set number
set smartindent
set expandtab
set tabstop=2
```
