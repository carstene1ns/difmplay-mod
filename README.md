# difmplay

> This is a modified version, the original can be found here:
http://tukaani.org/difmplay/

difmplay is a shell script to ease playing music from various AudioAddict Inc
internet radio streams. Both free and premium streams are supported. Playing
the premium streams naturally requires a paid subscription.

## Currently supported sites:

 * Digitally Imported (http://di.fm)
 * SKY.fm (http://sky.fm)
 * JAZZRADIO <http://jazzradio.com/>
 * ROCKRADIO <http://rockradio.com>

difmplay provides both command line and menu driven interfaces to select the
channel and the bitrate. difmplay constructs an URL matching the choices and
passes the URL to the selected audio player application. This way one doesn't
need to keep bookmarks of the playlist URLs for different channels and bitrates
just to avoid visiting (and in case of premium, logging in) the website
everytime one wants to play some music.

## Licensing

difmplay has been put into the public domain.

## [Download](https://github.com/carstene1ns/difmplay-mod/raw/master/difmplay.sh)

Save file from link as difmplay, put it to some directory in $PATH and make it
executable (chmod +x difmplay). difmplay has been used on GNU/Linux and OpenBSD
and probably works on many other operating systems too.

## Dependencies

Some audio player is needed to actually play the streams. Most players should
work, including most players with graphical user interface. The player just
needs to accept an URL to a .pls playlist as its last command line argument.
The default is MPlayer (MPlayer2, SMPlayer and mpv work as well).

To use interactive menus to select the settings, you need dialog. Many
GNU/Linux distributions include it in their default install.

Displaying multi-column channel list requires column command. It originates
from BSD but is available on all GNU/Linux systems too.

Updating the channel list requires curl.

Additionally only core utils are used (POSIX compatible shell, grep, sed, tr,
fold). They should be available everywhere.
