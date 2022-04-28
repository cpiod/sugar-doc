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

## controls

```
controls([[
    0 > k:left, c:dpad:left
    1 > k:right, c:dpad:right
    2 > k:up, c:dpad:up
    3 > k:down, c:dpad:down
    action> k:x, c:a
    kick> k:c, c:b, c:x
    
    input_kb> k:x,k:c,k:v,k:left,k:right,k:up,k:down
    input_pad> c:dpad:left,c:lstick:left,c:dpad:right,c:lstick:right,c:dpad:up,c:lstick:up,c:dpad:down,c:lstick:down,c:a,c:ltrigger,c:b,c:x

    tab> k:tab

    ctrl> k:lctrl 
    shift> k:lshift
    pause>k:p, c:start, k:escape
    +> k:kp_plus
    -> k:kp_minus
    f> k:f
    r> k:r
    
    mx>m:x
    my>m:y
    lb>m:lb
    rb>m:rb
    
    test> k:space
    dev_skip_level> k:return
    
]])
```

Set the controls for the game. Uses a proprietary format?

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

## bnksize

TODO

## file

    file("save.bnk", expbnk("save"))

Save to a file

## dirload

    dirload("assets/sfx", "wav", newsfx)

Load assets from a directory

# Window management

## newwin

    newwin(name, width, height, pixel_size, [options])

Create a new window. This window will have width x height pixels. The size of the pixel is controlled by pixel_size.

Options include:
    - "resize"
    - "scale"
    - "crt_calmos.shader"

The first created window has the Sugar animation played automatically.

! Not sure about that.

## delwin

    delwin(name)

Delete a window.

## winspec

    winspec("title", "title of the window")
    winspec("screen", MCW * 2, MCH * 2)

Set options about the window

! Not sure about that.

## fpslimit

    fpslimit(60)

Limit the number of FPS (frame-per-second). Does not affect the UPS (udpate-per-second).

## fps

    fps()

Get the effective FPS.

## url

    url("http://...")

Opens a URL in the browser.

# Graphics

## spritesheet

    spritesheet(sheet)

Change the current sprite sheet?

## newsrf

    newsrf("../../punkcake/punkcake_sheet.png", "pcd_sheet")

Load a sprite sheet?

## sset

    sset(x,y,[col])

Set a pixel color in the sprite sheet

## sget

    sget(x,y)

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

   circfill(x, y, r, [col])

Draw a filled circle. Same as PICO-8.

## rectfill

    rectfill(x0, y0, x1, y1, [col])

Draw a filled rectangle. Same as PICO-8.

## trifill

    trifill(x0, y0, x1, y1, x2, y2, [col])

Draw a filled triangle.

## circ

   circ(x, y, r, [col])

Draw an empty circle. Same as PICO-8.

## rect

    rect(x0, y0, x1, y1, [col])

Draw an empty rectangle. Same as PICO-8.

## tri

    tri(x0, y0, x1, y1, x2, y2, [col])

Draw an empty triangle.

## line

    line(x0, y0, x1, y2, [col])

Draw a line. Contrary to PICO-8, both start and end points are mandatory.

## cls

    cls([col])

Clear the screen with a color.

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

## color

    color(col)

Change current color.

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

## log

    log("Some message)

Print a message to log file. Normal logs are preceded by "."

## wlog

    wlog("Some message")

Print a warning message to log file. Warning logs are preceded by "!!"

## rlog

    rlog("Some message")

Print an critical message to log file and abort. Error logs are preceded by "ERR". Such log automatically triggers the end of the program and produce a stack trace.

## sugar_step

    sugar_step()

Wait until next frame?

## t / time

    t()

Get current time from Sugar start-up in s. Alias for `time()`.

## srand

    srand(seed)

Set rand seed.

## rnd

    rnd(max_value)

Get random float value in `[0,max_value[`.

## irnd

    irnd(max_value)

Get random integer value in `[0,max_value[`. Short for `flr(rnd(max_value))`.

# GIF

## newgif

## gifframe

## endgif

## giflen

## gifstream

# Misc.

## sleep

    sleep(k)

Put the program to sleep for k seconds.

## freeze

Same as sleep?

## quit

Stop the program.

## reset

Segfaut?

# Virtual machine command

## load

## run

## stop

## step

## resume

## execute

## help

## man

## changelog

Segfault.

## mantxt

Generate a manual.txt file.

# Other functions

- dt
- delta
- aft
- ltime
- gtime
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
- quitting
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
- sysbat
- delsfx
- delmus
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


