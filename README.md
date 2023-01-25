# GameandWatch-SteamDeck

### Parser settings to play Nintendo Game and Watch games on the SteamDeck

One day I noticed that my SteamDeck had a rom folder for Game and Watch files so I ported my roms over with the hope of being able to play them on the SteamDeck going forward. After some trial and error, I discovered that the official EmuDeck parser wasn't setup to display Game and Watch files. I've created the following instructions to help all users fill in the parser information easily with a working game library. 

If you follow the detailed steps below, you will be able to play game and watch files on the steam deck. 

This system will only work with files that end with .mgw, I do not have instructions yet for the MAME version of these games which start with gnw_ and end in .zip. 

### You will need a keyboard and a mouse to perfom the following steps.

## Steps:
### Basic Configuration
1. Parser type: `Glob`
2. Configuration title: `Game and Watch`
3. Steam category: `${Game and Watch}`
4. Steam directory: `${steamdirglobal}`
5. User accounts: 
6. ![image for step 6](https://kndafst.com/wp-content/uploads/2023/01/step9.png)
7. ROMs directory: `${romsdirglobal}/gameandwatch`

### Executable Configuration
8. Executable: `${retroarchpath}`
9. ![image for step 9](https://kndafst.com/wp-content/uploads/2023/01/step6.png)
10. Command line arguments: `run org.libretro.RetroArch -L ${os:win|cores|${os:mac|${racores}|${os:linux|${racores}}}}${/}gw_libretro.${os:win|dll|${os:mac|dylib|${os:linux|so}}} "${filePath}"`
11. Executable modifier: `"${exePath}"`
12. Start in directory: 

### Parser Specific Configuration
13. User's glob: `${title}@(.mgw|.MGW|.7z|.7Z|.zip|.ZIP)`

No further changes are necessary, under welcome to parser configuration, at the bottom click on save, if everything is working properly you will see a green dot to the left of game and watch under your parser listing, go up to preview and generate a new app list.

[Game Controls](/Game_Controls.md)


####Very special thanks to Madrigals Simulators for all of the work they have done to make this a possibility. 