Author: orkim
Date: April 4, 2016
Title: A Text Editor Story
Category: How-to
Tags: vim, neovim, nvim, linux

## Getting started with Vim.

Getting started with Vim can be pretty daunting. These are a few of the things
which I have found helpful to me get comfortable with using Vim. Let's start
with an overview.

 - Install NeoVim! Or at least Vim; not vi! (Version 7.4+).
 - Disable vi compatibility mode.
 - Add a few plug ins (listed below) to make things a bit nicer.
 - Disable the arrow keys. Seriously, do this!

For each of these points I have written a small section to outline what needs
to be done.

## NeoVim (Blatantly stolen from NeoVim documentation!)

If a package is not provided for your platform, see
[Building-Neovim](https://github.com/neovim/neovim/wiki/Building-Neovim).  Once
you've built Neovim, install it with the following commands:

    make
    sudo make install

For Unix-like systems this installs Neovim to `/usr/local`, while for Windows
to `C:/Program Files`. Note, however, that this can complicate uninstallation.
The following example avoids this by isolating an installation under
`$HOME/neovim`:

    rm -r build/
    make CMAKE_EXTRA_FLAGS="-DCMAKE_INSTALL_PREFIX:PATH=$HOME/neovim"
    make install
    export PATH="$HOME/neovim/bin:$PATH"

Note that the `rm -r build/` step above is needed if you've built Neovim
before, as the install location will be the same as before since CMake caches
build information.

## Initial plug ins.

 - [Vundle](https://github.com/VundleVim/Vundle.vim) - This is a plug in which
   manages all of the other plug ins. It is by far the easiest way I have found
   to keep your plug ins up to date. It makes it pretty pain free to
   install/remove as well as update.

 - [Airline](https://github.com/vim-airline/vim-airline) - This is a status
   line for Vim. This identifies the current tab/buffer in use, the
   mode you are in, filename, line endings, and much more.

 - [vim-ctrlspace](https://github.com/vim-ctrlspace/vim-ctrlspace) - This
   plugin helps with buffers/tabs/file management, fast fuzzy searching,
   workspaces (sessions), and bookmarks for projects.

 - [vim-easymotion](https://github.com/easymotion/vim-easymotion) - This is one
   of the best plug ins to extend motions. This gives a really nice interface
   to jumping exactly where you want quickly and with minimal key presses.

This sums up the absolutely required plug ins in my opinion. With only these
installed you have gained quite a bit from the default installation of Vim.

## Setting it all up.

Get NeoVim/Vim installed. I'm leaving that up to you to do. I suggest using the
latest source build of NeoVim, or use at least version 7.4 (or better) of Vim.
I'll leave the rest as an exercise for the reader.

Next we need to configure Vim to be more "Vim-like". Open up the dot file (or
create it if it doesn't exist) for vim

    nvim ~/.config/nvim/init.vim

...and add in "set nocompatible" to disable the legacy features we do not want.

Read the [install instructions for
Vundle](https://github.com/VundleVim/Vundle.vim) and complete the required
steps.

Finally, add in Airline, vim-ctrlspace,  and vim-easymotion plug ins from above.

Run a `:PluginInstall` and restart NeoVim/Vim.

## Learning how to move.

Now it is time to actually learn to move within Vim. One of the best features
of Vim are 'motions'. Instead of thinking in terms of "I need to go right 15
spaces" and pressing the arrow key 15 times, you can think in terms of
'motions' such as "I need to move 2 words forward" or "I need to move 4
paragraphs back".

Here's a short list of some of the most common keystrokes:

 - j - Down
 - k - Up
 - h - Left
 - l - Right

 - w - Forward to next word.
 - e - Forward to end of next word.

 - b - Backwards to previous word.
 - ge - Backwards to end of previous word.

 - f<char> - Forward to next <char> character.
 - F<char> - Backwards to previous <char> character.

 - H - Screen top.
 - M - Screen middle.
 - L - Screen bottom.

 - } - Forward to next paragraph.
 - { - Backwards to previous paragraph.

 - * - Next identifier.
 - # - Previous identifier.

