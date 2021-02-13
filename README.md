# how I learned Vim

## introduction

In this document, I'll share with you how I learned Vim, listing common commands and tips to help get you started.

Vim is a text editor that runs in the terminal. You can't use a mouse with Vim. All navigation and operations are performed with keyboard shortcuts. It's used by programmers because of how quickly practiced users can navigate files and how customizable it is, especially in the keyboard shortcut area. You should know the basics of using a command prompt before following this document.

(FYI, I use NeoVim, but that shouldn't change any of the instructions/commands below.)

## launch / exit Vim
- type "vim" into your terminal of choice
- to open a file type "vim [path to file]"
- to exit Vim, type ":q" and hit enter
- to save changes: ":w"
- if you want to save and quit: ":wq"
- if you want to discard changes: ":q!"

## modes

- normal - When you launch Vim, you'll be in normal mode, which is when you can use all the fancy key-bindings (keyboard shortcuts) that make Vim so special. You can tell you're in normal mode because the cursor will be fat.
- insert - To actually type text, hit "i" or "a" and then start typing. (Try and figure out the difference between i and a.) Use escape to get back into normal mode.
- visual - Visual mode happens when you hit "v" in normal mode. You can use the arrow keys (or h, j, k, l) to select text. You'll need this for copying/pasting and bulk deleting, etc.
- command - When you hit ":" in normal mode you can type commands, like "w" to save or "q" to quit or "term" to open up a terminal window.

## commands

Now it's time to learn some handy commands that you can use in normal mode. Getting good at these things is what makes Vim folks to fast at writing code. These are basic commands, roughly in the order I learned them.

| command/s           | description                                               |
| ------------------- | --------------------------------------------------------- |
| h, j, k, l          | move around in the file (right, down, up, left)           |
| i                   | enter insert mode                                         |
| escape              | go back into normal mode                                  |
| o                   | open a new line below current line and enter insert mode  |
| dd                  | delete line                                               |
| v                   | enter visual mode so you can select text                  |
| shift-v             | select text line-by-line                                  |
| y                   | copy                                                      |
| yy                  | copy current line                                         |
| p                   | paste                                                     |
| gg, G               | move to top of file, bottom of file                       |
| shift-{, shift-}     | move up/down the file by paragraphs                       |
| 0, $                | move to the beginning/end of a line                       |
| zz                  | center the screen around the cursor                       |
| crtl-ww             | switch windows (for when you have multiple panels open)   |
| ctrl-b (my config)  | open up NERDTree                                          |
| :term               | open a terminal panel                                     |

See this [Vim cheat sheet](https://vim.rtorr.com/) for more.

## .vimrc

The weirdest thing about Vim for most people is that it runs in a terminal. It's boring and ugly! So that's why people customize the heck out of their Vim windows. My setup literally looks like my VSCode window, except that it's faster to launch and faster to code in. The way to customize Vim is to edit the .vimrc file that lives in your home directory. If it's not there, you'll have to make it. I'll include my config file in this repo so you can get a taste. (For Neovim the config file is called init.vim.)

Plug is a plugin manager, so that's the first thing I install, then I use plug to install a bunch of plugins, and the last section of the file is where I set various settings, some that are built into Vim and some that are for the plugins. There are also a few custom keybindings in there.

A word of advice: To get [NERDTree](https://github.com/preservim/nerdtree) to work with the [devicons](https://github.com/ryanoasis/vim-devicons) plugin, I had to install a ["nerd font"](https://www.nerdfonts.com/) onto my computer. For Mac all you have to do is download the nerd font of your choice, open it up (which will add it to Font Book) and then make sure your terminal app uses that font for non-unicode characters. (You can't use Mac's default Terminal app if you want cool colors, fyi, since Terminal doesn't allow more than a handful of different colors.)

For more info on customizing, see [this article](https://medium.com/better-programming/setting-up-neovim-for-web-development-in-2020-d800de3efacd). It's the one I followed to get Vim to look like this:

![my Neovim setup](screenshot.png)

