Author: orkim
Date: April 5, 2016
Title: Shells, Shells, Shells
Category: How-to
Tags: zsh, shell, linux

# Overview

This is a quick post to document my personal shell setup. I've used bash for
years, but recently made the switch to zsh. Here's a few pointers from my
install.

# Installing ZSH

Since I'm on Debian unstable I just install from the repo's.

```shell
apt-get install zsh
```

Change our default shell to zsh.

```shell
chsh -s /usr/bin/zsh
```

Log out, and back in, and we're done.

# Oh My Zsh!

Now we can add some extras to zsh by using [Oh My Zsh!](http://ohmyz.sh/) which
describes itself as an "open source, community-driven framework for managing
your ZSH configuration."

### Basic Installation (Blatantly stolen from Oh My Zsh! wiki!)

Oh My Zsh is installed by running one of the following commands in your
terminal. You can install this via the command-line with either `curl` or
`wget`.

#### via curl

```shell
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

#### via wget

```shell
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

# Plug ins!

Everyone loves plug ins. Open up the ~/.zshrc file and edit the `plugins` line
to enable the desired plugs ins.  This is what I've settled on for now.

```shell
plugins=(git colored-man-pages vi-mode vundle tmux)
```

Documentation on these should be found in the ~/.oh-my-zsh/plugins/ directory.

# Theme

Personally I like the 'ys' theme, so update the them line to:

```shell
ZSH_THEME="ys"
```

# Conclusion

I've been using this configuration for a few days now. I'm still learning more
and discovering new things. As I come across things I plan on keeping notes and
doing a write up as they accumulate.
