[![linux-keylogger Build](https://github.com/rounnus/linux-keylogger/actions/workflows/cmake.yml/badge.svg?branch=main)](https://github.com/rounnus/linux-keylogger/actions/workflows/cmake.yml)
# Introduction
This keylogger is a project that was made for educational purposes and does not send any keystroke to the internet. What it does is take the keystrokes and store them in a local file. I wanted to make such a keylogger for a long time to learn how a program could take keystrokes and use them either for good or for bad.<br>

<img src="https://user-images.githubusercontent.com/38585824/150214487-0cd08cfc-3b26-4975-8669-233acf9ee59b.gif" width="70%" height="50%">

# Installation requirements
The following packages must be installed.<br>
```
sudo apt-get install build-essential cmake git gcc
```

# Download & Build

First download the program from GitHub and go to the linux-keylogger folder.

```
% git clone https://github.com/rounnus/linux-keylogger.git
% cd linux-keylogger/
```

After installation the program must be built. In order to build the program, the following instructions must be
followed.<br>

```
% mkdir build
% cd build/
% cmake ../
% make
```

`
The cmake should be from version 3.20 and above, if you do not have this version please go to the following site and download the latest version:
https://cmake.org/download/
`

After this the program will be installed and ready to run.

# Features
- [x] Auto detect keyboard.
- [x] Work with multiple keyboards.
- [x] Detect any new keyboard on air.

# Log loction
Captured keystrokes stored at `~/.local/share/keylogger/logs/`
