# sugar-doc
Unofficial documentation for the SUGAR game engine

# Game loop

## \_init

Initialize the game, called once

## \_draw

Draw the game, called for each frame

## \_update

Update the game, called for each frame

# System functions

## mkdir

    mkdir(SNAP_FOLDER)

Create a directory

## cd

Change directory

## ls

List directory

## rm

Remove file

## newbnk

    newbnk("save", 30, 7, 2)

Create a bank

## delbnk

Delete a bank

## bank

    bank("save")

Set a bank as current

## bset

    bset(x, y, 0)

Set a value in the current bank

## expbnk

    file("save.bnk", expbnk("save"))

Serialize bank file?

## file

    file("save.bnk", expbnk("save"))

Save to a file

## dirload

    dirload("assets/sfx", "wav", newsfx)

Load assets from a directory

# Window management

## newwin

    newwin("civ", MCW, MCH, MSC, "resize", "scale", "crt_calmos.shader")

Create a new window

## delwin

Delete a window

## winspec

    winspec("title", "Roguechess")
    winspec("screen", MCW * 2, MCH * 2)

Set options about the window

## fpslimit

    fpslimit(60)

Limit the number of frame-per-second

# Graphics

## spritesheet

    spritesheet(sheet)

Change the current sprite sheet?

## newsrf

    newsrf("../../punkcake/punkcake_sheet.png", "pcd_sheet")

Load a sprite sheet?

## sset

Set a pixel color in the sprite sheet

## sget

Get a pixel color from the sprite sheet

## spr

    spr(fr, x, y)

Print a sprite

## sspr

    sspr(0, 0, 600, 320, x, y)

Resize and print a sprite

## sprgrid

    sprgrid(gw, gh)

Print a grid?

## pset

    pset(x + dx, y + dy, bright(pget(x + dx, y + dy), inc))

Set a pixel color

## pget

    pget(x + dx, y + dy), inc)

Get a pixel color

## clip 

    clip(clpx + 2, clpy + movy + 2, 124, 164)

Change current draw zone. `clip()` to disable.

## circfill

   circfill(cx, cy, 120, 1)

Draw a filled circle

## rectfill

    rectfill(clpx, clpy, clpx + 127, clpy + 167, 0)

Draw a filled rectangle

## trifill

Draw a filled triangle

## tri

Draw an empty triangle

## rect

Draw an empty rectangle

## circ

Draw an empty circle

## line

Draw a line

## cls

    cls(0)

Clear the screen

## camera

    camera(shkx, shky - movy)

Move the camera?

## tcamera

    tcamera(x,y)

Move the camera?

## winspec

    winspec("wmode", bget(2, 0) == 0 and "resize" or "fullscreen")

Change window mode

# Controls

## defbtn

    defbtn("mouse_tracker_y", 0, "m:y")

Define a button

## btnv

    btnv("mouse_tracker_x")
    btnv("mouse_tracker_y")

Get button value

# Sounds

## newmus

Load a music

## music

    music(s, 0, loop, fade_sec)

Start a music

## nxtmusic

    nxtmusic(sub(s, 1, #s - 1) .. "B", -1, true)

Change music?

## sfx

    sfx(str, -1, vol)

Play an SFX

## musvol

    musvol(MUTE or (bget(0, 0) / 12)^2)

Change music volume

## sfxvol

    sfxvol(MUTE or (bget(1, 0) / 10)^2)

Change sfx volume

## newsfx

	newsfx("../../punkcake/slap.wav", "pcd_slap", 0.6)

Load a SFX

## delsfx

	delsfx("pcd_slap")

Unload a SFX

# Text

## newfnt

Import font

## delfnt

Delete font

## font

Change current font?

## print

Print some text on screen?

# Palette

## palette

	palette(oplt)

Load a palette?

## pal

    pal(2, 1)

Change palette color

## palt

Change palette transparency

## rgb

Get color from RGB values?

## hsv

Got color from HSV values?

# Memory

## peek/peek2/peek4

Read from memory

## poke/poke2/poke4

Write to memory

# Other

## clipboard

    cb = clipboard()

Not clear

## wlog

    wlog("reset save")

Print to log file. Warning log?

## sugar_step

    sugar_step()

Wait until next frame?

## t / time

    t()

Get current time (in s?). Alias for time()?

## srand

Set rand seed

## rnd

Get random value?

# GIF

## newgif

## gifframe

## endgif

## giflen

## gifstream


# Virtual machine command

##  load

## run

## stop

## step

## resume

## execute

## help

## man

## changelog

## mantxt

# Other functions

- irnd
- dt
- delta
- sleep
- freeze
- fps
- aft
- ltime
- gtime
- log
- wlog
- rlog
- logdupe
- hex
- newchk
- delchk
- modchk
- chunk
- chkinfo
- wipe
- write
- read
- transfer
- memcpy
- memset
- memsbs
- color
- newsrf
- delsrf
- expsrf
- target
- srfname
- srfmem
- srfsize
- srfshot
- window
- flip
- fillp
- sfillp
- aspr
- expfnt
- fntinfo
- strwidth
- shader
- shdrf
- shdrf2
- shdrf3
- shdrf4
- shdri
- shdri2
- shdri3
- shdri4
- shdrsrf
- expbnk
- bnksize
- bset
- bget
- quit
- quitting
- controls
- defbtn
- inpnum
- btn
- btnp
- btnr
- btnv
- btnclr
- getinp
- txtinp
- mouse
- ctrlr
- sugar_step
- export
- reset
- sysbat
- url
- newsfx
- newmus
- delsfx
- delmus
- sfxvol
- musvol
- sfx
- music
- nxtmusic
- lockaudio
- unlockaudio
- chnlfx
- chnlprog
- folder
- desktop_path
- namefind
- file
- steam
- discord


