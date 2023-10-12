# Play GameBoy console game in Project Zomboid

!!!!!! Do Not Use this MOD !!!!!!


![screen1](https://github.com/yanmingsohu/zPlayableGameBoy/blob/master/screen.png)


This mod is just as a technical demonstration, he shows a possibility that allows you to go through hard times with old GB game in default, but you find that GB is very slow, so much that this GB makes you feel like dying is a good choice.

Trust me.



# Install

If you must try it, follow the complicated steps described below:

0. Install This mod: https://steamcommunity.com/sharedfiles/filedetails/?id=2831786301
1. Donload mod
2. Download GB game roms, note that 99% of roms won’t work, well, maybe you want to try Super Mario Land(1989)
3. Copy the .gb file to `zPlayableGameBoy\media\lua\client\cartridge`
4. Download and install Nodejs: `https://nodejs.org/en/download`
5. Double-click the file to run it: `zPlayableGameBoy\media\lua\client\cartridge\convert.cmd`
6. If you did the previous step correctly, you will get the compiled .gb file, for example, `xxx.gb` will generate the file: `xxx.gb.lua`
7. If you don't want to download nodejs, you can read the source code of rom-to-lua.js and then follow the commands there to convert the .gb file yourself (good luck ;)
8. Let me think......
9. Emmmm.......
10. Open And EDIT: `zPlayableGameBoy\media\lua\client\cartridge\gb-game-mapping.lua`
11. Find the corresponding game name modification `=` the path behind
12. Enter the PZ game and find the GB cartridge and GB console.
13. Emmmmm.........



# Technical details

This emulator comes from `https://github.com/zeta0134/LuaGB`

This is an unfinished emulator, and many roms cannot run. It runs very fast on the original lua interpreter, but PZ's lua interpreter is very slow, which results in you having to wait 100 years for a fast enough cpu. Go run it. Because PZ has no way to create a pixel buffer, it can only simulate the display with a bunch (about 10,000) texture blocks, which in turn results in slow rendering. I also didn't find a way to create an audio buffer, so there is no sound. Since PZ has no method of reading files, the rom must be compiled into a lua script resource file.

This library simulates bit operations, which is another reason for slowness.: `https://github.com/AlberTajuelo/bitop-lua`


Anyway, I don't want to touch this code anymore, so I put it on github so anyone can do whatever they want: `https://github.com/yanmingsohu/zPlayableGameBoy`