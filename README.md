# FestivalPlayer_Exe
Repository with just an executables for 'FestivalPlayer'.

It has pretty much anything you need to just use the FestivalPlayer.
Somehow it properly works only as debug solution, so consider a slightly bigger size and perhaps a bit less of perfomance(I guess).

The only missing thing here is .pdb which stands for 'Programm Debug Data'. It's just too big for GitHub, but anyway should work fine without.

## If you interested in source code check [source page](https://github.com/Andrii-Berozkin/FestivalPlayer).

## Settings explained
All settings are inside [FestivalPlayer_Settings.json](https://github.com/Andrii-Berozkin/FestivalPlayer/blob/master/FestivalPlayer_Settings.json). ***!IMPORTANT this json file is only for showcase, the real one will be created at first run by a program where the executable is!***
### The most important one is -
 - **ReactionDelayMS** - it defines how long it takes to keys be pressed after image capturing and filtering. You want to adjust this value first one because it`s depends on user CPU and overall load on PC. Probably completely unique for everyone.
 - **bEnableDebug** - print or not pressed keys in console.

 - **MusicNoteTargetColor** - target color to find on each (5) sections. Finding this color will trigger button to be pressed. Used in cooperation with 'ColorTolerance'.
 - **ColorTolerance** - how much color spreading allowed to count as TargetColor. Tolerance value applied to each R, G, B individually. For example if target color (10,15,5) and tolerance is (5), this color (15,10,0) or (10,20,5) will return true. And this one (16, 15, 5) will be out of range.

 - CaptureSizeFromTotal
 - **SizeMultiplierX** - specify an width which actually need to be captured. Form an rectangle (work with SizeMultiplierY). For example 3840 px * 0.265 = 1017 px.
 - **SizeMultiplierY** - specify an height which actually need to be captured. Form an rectangle (work with SizeMultiplierX). For example 2160 px * 0.0150 = 32 px.

 - CapturePos
 - **ScreenPercentX** - specify shift by width of capturing area from center of screen. For example 0.5 the capturing will be perfectly centered at screen automatically. !Reccomendede value 0.503 as a Fortnite festival slightly shifted to the right!
 - **ScreenPercentY** - specify shift by height of capturing area from center of screen. For example 0.5 the capturing will be perfectly centered at screen automatically.

 - **MusicNoteSizeXMultiplier** - multiply on capturing width to create proportional sections. As expert mode used 5 lines of notes, recommended value is 0.2.
