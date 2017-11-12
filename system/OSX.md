# File system

## Show all (including system/hidden/`.`) files

1. + http://osxdaily.com/2009/02/25/show-hidden-files-in-os-x/
write in the terminal
   +  **in OS X El Capitan 10.11, Yosemite 10.10, and OS X Mavericks 10.9**:
     + `defaults write com.apple.finder AppleShowAllFiles TRUE;killall Finder`
   + in Mac OS X 10.8 Mountain Lion, OS X 10.7 Lion, Mac OS X 10.6 Snow Leopard, and before:
     + `defaults write com.apple.Finder AppleShowAllFiles TRUE;killall Finder`
