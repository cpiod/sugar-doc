# sugar-doc
Unofficial documentation for the SUGAR game engine

# System functions

## mkdir

    mkdir(SNAP_FOLDER)

Create a directory

## newbnk

    newbnk("save", 30, 7, 2)

Create a bank

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

# Graphics

## spritesheep

    spritesheet(sheet)

Load a spriteshoot?

## spr

    spr(fr, x, y)

Print a sprite

## sspr

    sspr(0, 0, 600, 320, x, y)

Resize and print a sprite

## sprgrid

    sprgrid(gw, gh)

Print a grid?

## palette

	palette(oplt)

Load a palette?

## pal

    pal(2, 1)

Change palette color

## clip 

    clip(clpx + 2, clpy + movy + 2, 124, 164)

Change current draw zone. `clip()` to disable.

## circfill

   circfill(cx, cy, 120, 1)

Draw a filled circle

## rectfill


    rectfill(clpx, clpy, clpx + 127, clpy + 167, 0)

Draw a filled rectangle

## camera

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

## music

    music("title_A")

## musvol

    musvol(MUTE or (bget(0, 0) / 12)^2)

Change music volume

## sfxvol

    sfxvol(MUTE or (bget(1, 0) / 10)^2)

Change sfx volume

Start a music

## delsfx

	delsfx("pcd_slap")

Unload a SFX

# Other

## wlog

    wlog("reset save")

Print to log file

# All functions

- srand
- rnd
- irnd
- fpslimit
- t
- dt
- time
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
- assert
- abort
- abort_brutal
- clipboard
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
- peek
- peek2
- peek4
- poke
- poke2
- poke4
- camera
- tcamera
- clip
- color
- pal
- palette
- rgb
- hsv
- newsrf
- delsrf
- expsrf
- target
- srfname
- srfmem
- srfsize
- srfshot
- newwin
- delwin
- window
- flip
- winspec
- fillp
- cls
- rectfill
- rect
- circfill
- circ
- trifill
- tri
- line
- pset
- pget
- spritesheet
- sprgrid
- palt
- sfillp
- spr
- aspr
- sspr
- sset
- sget
- newfnt
- delfnt
- font
- expfnt
- fntinfo
- strwidth
- print
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
- newbnk
- delbnk
- expbnk
- bank
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
- load
- run
- stop
- step
- resume
- execute
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
- cd
- ls
- mkdir
- folder
- desktop_path
- namefind
- file
- rm
- newgif
- gifframe
- endgif
- giflen
- gifstream
- help
- man
- changelog
- mantxt
- steam
- discord


