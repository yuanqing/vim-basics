# Vim Basics

> Just the basics to get you up and running with Vim.

## Quick start

1. Launch Vim via the terminal:

  ```bash
  vim Main.java
  ```

  You are now in Vim&rsquo;s ***Command*** mode, also known as ***Normal*** mode.

  (You should see the contents of `Main.java` if the file already exists. Otherwise you will see an empty text editor window.)

2. To start typing into the file, you need to switch to Vim&rsquo;s ***Insert*** mode. Press `i` to do so. You should see `-- INSERT --` at the bottom-left hand corner of the window. Now whatever you type will appear as you would expect with any other text editor.

3. As soon as you&rsquo;re done typing, press `<Esc>` to go back to ***Command*** mode. (The `<Esc>` key is your friend! Hitting `<Esc>` will bring you back to ***Command*** mode.)

4. And&hellip; that&rsquo;s about it, really! Now type `:w` and `<Enter>` to save the file, followed by `:q!` and `<Enter>` to quit Vim.

## Commands

Virtually all operations in Vim occur while in ***Command*** mode. Listed here are the most crucial commands that you should/must know.

### Switching between ***Command*** and ***Insert*** mode

Action | Keys
:------|:-----
Switch to ***Command*** mode | `<Esc>`
Switch to ***Insert*** mode | `i`
Switch to ***Insert*** mode, moving the cursor to the end of the current line | `A`
Switch to ***Insert*** mode, adding a new line under the current line, and moving the cursor to the new line | `o`

### Moving the cursor around the file

Action | Keys
:------|:-----
Page up | `<Ctrl>` + `u`
Page down | `<Ctrl>` + `d`
Move the cursor to the next word | `W`
Move the cursor to the previous word | `b`
Move the cursor to the start of the current line | `0`
Move the cursor to the end of the current line | `$`
Move the cursor to a particular line of the file (eg. line number 9) | `9G` or `:9`

Of course, you can also move the cursor via any of the arrow keys, but it is a lot faster to use the above commands.

### Delete/cut

Action | Keys
:------|:-----
Delete the line under the cursor | `dd`
Delete the word under the cursor | `dw`
Delete the character under the cursor | `x`

Because whatever you delete is copied into Vim&rsquo;s buffer, these 3 commands are akin to performing a cut.

### Copy and paste

Action | Keys
:------|:-----
Copy the current line | `yy`
Copy a particular number of lines, starting from the current line (eg. 3 lines) | `3yy`
Paste | `p`

You can also copy via a text selection, which is more precise but a bit more involved:

1. While in ***Command*** mode, press `v` to switch to ***Visual*** mode. You should see `-- VISUAL --` at the bottom-left hand corner of the window.
2. [Move the cursor](#moving-the-cursor-around-the-file) to adjust the text selection.
3. When you have selected the text that you want to copy, press `y`. This will bring you back to *Command* mode, and the selected text will have been copied into Vim&rsquo;s buffer.

### Undo and redo

Action | Keys
:------|:-----
Undo | `u`
Redo | `<Ctrl>` + `r`

### Fixing code indentation

Action | Keys
:------|:-----
Fix the code indentation of the file | `gg=G`

### Save and quit

Action | Keys
:------|:-----
Save the file | `:w` then `<Enter>`
Save the file then quit | `:wq!` then `<Enter>`
Quit without saving the file | `:q!` then `<Enter>`

## Display settings

These are some commands to customise the display:

Action | Keys
:------|:-----
Enable syntax highlighting | `:syntax on` then `<Enter>`
Enable line numbers | `:set number` then `<Enter>`

Vim will look for a settings file called `.vimrc` in your home directory. You can avoid having to type the above settings again and again by simply putting the following in your `~/.vimrc`:

```viml
syntax on
set number
```

## Advanced stuff

- [Vim commands cheatsheet](http://www.fprintf.net/vimCheatSheet.html)
