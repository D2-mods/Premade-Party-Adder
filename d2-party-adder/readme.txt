Premade Party Adder
Github: https://github.com/D2-mods/Premade-Party-Adder
Installs on: IWD:EE, The Black Pits 1&2 (BGEE/BG2EE/EET)


==================================================
Overview
==================================================
Adds custom premade parties to the New Game screen. Also a CHR to CRE converter (required for premade parties).

This replaces the default party. You can store up to 4 custom parties in the mod folder, and there are separate components for IWD and HoW, so you can have the same or different parties for each. There's also an option to just remove the default party, without adding a new one.

IWDEE: There's also a component to fix the bug where imported characters could start with the BG2 biography. More info below.


==================================================
Installation
==================================================
- Place up to 6 CHR files in one of the party folders
- Optional: Add biography and/or portrait files to the folder
- Run the installer
- Select party from the list
- CRE files are added to the override (these are what's used for the premade parties)
- CHR files are added to the characters folder to allow for importing individually

Folders:
- party => IWD:EE
- bpparty => Black Pits

Optional: 
- Biographies will also be added. These are just text files with the .BIO extension. They must have the same filename as the CHR file. Characters without a BIO file will instead get the generic biography used for Black Pits 2. It works well enough for any class. Note that the biographies are written directly into the CRE/CHR files (i.e. not added as a separate file to the characters folder).
- Portraits in the folder will be copied to the override (though not made selectable at character creation). This does not conflict with my Portrait Gender Separator mod, unless you have different portraits with the same filename.

Black Pits note: Only the premade party will have custom biographies. Imported characters will get the normal BG story-related biography.


==================================================
Additional info
==================================================
- Characters are added in number/alphabetical order. This is mainly relevant for the first character, who is treated as the protagonist and cannot be kicked from the party. 
- If there are more than 6 CHR files in the folder, only the first 6 are added to the party (though all will be converted to CRE files in the override).


==================================================
Biography bug (IWD:EE)
==================================================
This mod fixes the bug that causes imported characters to start with the BG2 biography. This is done by default for characters added to premade parties. A separate component lets you patch all CHR files in the characters folder.

This will also delete any BIO files in the folder (required to prevent the bug). The biographies are written directly into the CHR files instead. Characters without a BIO file will get the generic biography from Black Pits 2, but only if the CHR file doesn't already have a custom biography written in.

It's not completely bug-free. To avoid issues, don't open up the biography screens before starting the game (the status screens are fine). Once you're in the game, you can view any screens without issues. I noticed at least two reproducible bugs on the party creation screen, which I'll describe here:

1. If you view the biography of Player1 (first character in order), then import more characters, then start the game, Player1 will have the BG2 biography.
2. If you view the biographies of any character other than Player1, then start the game, Player1 will have the same biography as the last character viewed. This bug happens with premade parties as well.

Basically, as long as you don't view biographies while on the party creation screen, there shouldn't usually be issues.


==================================================
Tools and Resources:
==================================================
- WeiDU (https://github.com/WeiDUorg/weidu)
- NearInfinity (https://github.com/Argent77/NearInfinity)
- Notepad++ (https://notepad-plus-plus.org/)
- Git Bash (https://git-scm.com/downloads)
- Infinity Auto Packager (https://github.com/InfinityTools/InfinityAutoPackager)
- IESDP (https://gibberlings3.github.io/iesdp/main.htm)


==================================================
Version info
==================================================
v1.3
- Small update for Component 3 (Biography fix): Fixed an issue that could prevent the generic biography from being written into a CHR file. This would happen if trying to patch a CHR file created with the Export button, but also without a .BIO file (i.e. you deleted the BIO because you wanted the generic biography from this mod). This bug did not affect pregenerated characters, only exported ones.

v1.2
- Changed name of marker file to make it more clear it's from this mod.
- Party components will fail to install if no CHR files are in the folder. This won't give a WeiDU error. It'll just say "INSTALLATION ABORTED". If using a mod manager, installation will continue uninterrupted.

v1.1
- changed backup folder to weidu_external
- improved tp2 files
- added marker to characters folder when any component is installed

v1.0 - release version
v0.5 - fixed biography bug in IWD:EE (for imported characters)
v0.4 - minor fixes/adjustments
v0.3 - split off IWD2 to separate mod
v0.2 - working on IWD2
v0.1 - initial version