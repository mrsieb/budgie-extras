# budgie-extras

Additional enhancements for the user experience

## Plugins:

 - Hotcorners
 - Quicknote
 - Workspace Switcher Overview
 - Wallpaper Switcher
 - Workspace Mover
 - ShowTime
 - CountDown
 - Automatic Keyboard Layout Switcher
 - Screen Rotation Lock
 - ClockWorks
 - DropBy
 - Kangaroo
 - WeatherShow
 - Trash
 - App-launcher
 - RecentlyUsed
 - Take-A-Break
 - Workspace Stopwatch
 - Fuzzy Clock
 - Brightness Controller
 - Visualspace

## Standalone

budgie mini-apps - see the individual components for details

 - Budgie Extras Daemon
 - Budgie Wallstreet
 - Budgie Quickchar (needs the extras daemon as a runtime dependency)
 - Budgie Window Previews (needs the extras daemon as a runtime dependency)

 ## Installation

 By default all applets are compiled and installed:

     mkdir build && cd build
     meson --buildtype plain --prefix=/usr --libdir=/usr/lib
     ninja -v
     sudo ninja install

If individual applets (or groups of applets) are to be compiled and installed use
the options described in meson_options.txt i.e. use `-Dbuild-all=false -Dbuild-appletoption=true`

e.g. to build just the hotcorners and weathershow applets

     mkdir build && cd build
     meson --buildtype plain -Dbuild-all=false -Dbuild-hotcorners=true -Dbuild-weathershow=true --prefix=/usr --libdir=/usr/lib
     ninja -v
     sudo ninja install

## Distro's

We love Budgie-Extras to work across as many distro's as possible.  So please let us know if your distro has packaged budgie-extras and how to install.

 - Arch - https://www.archlinux.org/packages/community/x86_64/budgie-extras/
 - Ubuntu - use the ubuntu-budgie-welcome snap - and install via Menu - Budgie Applets
 - Debian - packages are available in Buster named "budgie-insertname-applet" https://goo.gl/R4eF7q
 
 [![Packaging status](https://repology.org/badge/vertical-allrepos/budgie-extras.svg)](https://repology.org/project/budgie-extras/versions)

## Build/Runtime dependencies

Use the debian/control file on the debian branch to understand the build and runtime package dependencies for each applet.

Overall, the following packages are required for the various Python plugins to work:

 - wmctrl
 - xdotool
 - xprintidle
 - python3
 - python3-gi
 - python3-gi-cairo
 - python3-cairo
 - zenity
 - ogg123 (from vorbis-tools)
 - gir1.2-budgie-1.0
 - gir1.2-gtk-3.0
 - gir1.2-glib-2.0
 - gir1.2-wnck-3.0
 - python3-psutil
 - dconf-cli
 - sound-theme-freedesktop
 - imagemagick
 - python3-pil
 - python3-svgwrite
 - python3-cairosvg
 - python3-pyudev
 - python3-requests
 - notofonts
 - python3-xlib

The following packages are required for the various Vala plugins to work:
 - gobject-introspection
 - libgtk-3-dev
 - valac
 - meson
 - budgie-core-dev
 - libbudgie-plugin0
 - libpeas-dev
 - libjson-glib-dev
 - libgee-0.8-dev
 - libsoup2.4-dev
 - libwnck-3-dev
 - libkeybinder-3.0-dev
 - gnome-settings-daemon-dev
