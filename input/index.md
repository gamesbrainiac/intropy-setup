# Welcome to Introduction to Python - SETUP
__by Quazi Nafiul Islam__

__`@gamesbrainiac` on Twitter__

---------------------------------------

This document provides instructions for setting up your Python environment for your respective Operating System. If you need help regarding this, please send me a tweet `@gamesbrainiac` on twitter. However, before doing so, please read [this article](https://github.com/yyuu/pyenv/wiki/Common-build-problems).

---------------------------------------

## MAC OS

Mac already has Python installed, but its the wrong version. However, it is not the correct version. We are going to be using the latest version of the language, `3.4.1`. So, we are going to use a special tool called `pyenv`. We can install it using Homebrew, which is a package manager for MAC OS. If you do not have any other package manager installed, namely Finks or Macports, then please install Homebrew by pasting the following in the Terminal and hitting __ENTER__:

    ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"

Now, restart your terminal, and type in the following:

    brew install pyenv

Once that is done, just type the following into your terminal:

    echo "eval \"$(pyenv init -)\"" >> ~/.bashrc

___Note, that if you use zsh, then .zshrc___

Restart your terminal and now, you should be able to get `pyenv` available as one of your Terminal commands. Then simply install the version of Python that we need (this might take quite some time):

    pyenv install 3.4.1

After doing this, set your global python to `3.4.1` by doing the following:

    pyenv global 3.4.1

Now you're all set.

### Installing `bpython`

`pyenv` takes care of a lot of the problems associated with managing python installations. You can easily install packages for a particular version of python with ease. All you have to do now is:

    pip install bpython

And then:

    pip install bpython-curtsies

And then:

    pip install bpython-urwid

After that is done, you can invoke your special interpreter, `bpython` using `bpython` in your command line. This is a screen shot of what it should look like (_your colorscheme might be different, but the screen shot should look familiar_):

![bpython](assets/pics/bpython.png)

---------------------------------------

## Linux

In order to get our software running, we will need a couple of things, so just paste this into your Terminal and hit __ENTER__ (this might take some time):

    sudo apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev \
    libreadline-dev libsqlite3-dev wget curl llvm

If you're using Redhat/Fedora:

    yum install zlib-devel bzip2 bzip2-devel readline-devel sqlite sqlite-devel

Since we're using `sudo`, the Terminal will prompt you for your password.

You will need `pyenv` because most distributions of Linux (be it Fedora or Debian/Ubuntu or Arch) come with their own version of Python. In short you do not want to mess with that installation of Python since _a lot_ of your applications depends on it functioning properly.

Also, it might not be the right version, in most cases Python 2 is installed. So, we will install `pyenv`using the following script:

    curl -L https://raw.githubusercontent.com/yyuu/pyenv-installer/master/bin/pyenv-installer | bash

This should install `pyenv` for you. Now just append the following lines to your `~/.bashrc` or if you use `zsh` your `~/.zshrc`:

    export PATH="$HOME/.pyenv/bin:$PATH"
    eval "$(pyenv init -)"

Now that `pyenv` is installed, lets install the latest version of python (this might take quite some time):

    pyenv install 3.4.1

Now, all you have to do is set Python `3.4.1` as your default interpreter:

    pyenv global 3.4.1

### Installing `bpython`

    pip install bpython

And then:

    pip install bpython-curtsies

And then:

    pip install bpython-urwid

If the above ran without a hitch, then you're all set. Just restart your Terminal, and now you can open up bpython typing in `bpython` in the Terminal.

### Troubleshooting

Linux distros have a lot of platform specific problems. So, if things don't work out for you, you are going to have to use the bundled python that comes with your distribution. You can still use `pip` to do a `pip install bpython`, so make sure you do that.

## Windows (7, Vista and 8)

If you already have a version of Python installed, and its _not_ Python 3, then you're in trouble. But before addressing that problem, we will first need to install the latest version of Python.

What you need to determine _first_ is what architecture your OS runs on, whether its `32bit or x86` or `64bit or x64`. Here are the steps:

![explorer_click](assets/pics/win_2.png)

![right_click](assets/pics/win_3.png)

![info_arch](assets/pics/win_1.png)

If the highlighted region says `32` then use [this](https://www.python.org/ftp/python/3.4.1/python-3.4.1.msi) installer. Otherwise, use [this](https://www.python.org/ftp/python/3.4.1/python-3.4.1.amd64.msi) installer for `64` bit.

If you have installed things correctly, then you should be able to see a python prompt when you run `python` in the command line:

![getting_cmd](assets/pics/win_4.png)

![python_win](assets/pics/win_5.png)

### Installing `bpython`

This is where things become problematic for people who have _another_ version of Python installed. If you don't have another version of python installed, don't worry about anything. So, firstly in order to install bpython, you will need to install a library called `curses`, from [this](http://www.lfd.uci.edu/~gohlke/pythonlibs/#curses):

![curses_install_win](assets/pics/win_6.png)

Now all you have to do is go into your command prompt, and install `bpython`:

    pip install bpython

However, if you do have another version, then you are going to have to change your directory to `C:\Python34\Scripts`, and then run:

    pip.exe install bpython

Once that is done, stay in that directory and invoke `bpython.exe` from the command line.

# TEST

Open up your Terminal/CMD, and type in `python`. Then type in `import this`, hit __ENTER__. Which line do you like the best and why? Reply to gamesbrainiac@gmail.com, with your __name__ and **ID**.