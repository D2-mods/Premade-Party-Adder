# Premade Party Adder
Download: https://github.com/D2-mods/Premade-Party-Adder/releases  
Installs on: IWD:EE, The Black Pits 1&2 (BGEE/BG2EE/EET)


#### Overview:
Adds custom premade parties to the New Game screen. Also a CHR to CRE converter (required for premade parties).

This replaces the default party. You can store up to 4 custom parties in the mod folder, and there are separate components for IWD and HoW, so you can have the same or different parties for each. There's also an option to just remove the default party, without adding a new one.

IWDEE: There's also a component to fix the bug where imported characters could start with the BG2 biography. More info below.


#### Installation:
- Place up to 6 CHR files in one of the party folders
- Run the installer
- Select party from the list
- CRE files are added to the override (these are what's used for the premade parties)
- CHR files are added to the characters folder to allow for importing individually

Folders:
- party => IWD:EE
- bpparty => Black Pits


#### Optional: 
- Biographies will also be added. These are just text files with the .BIO extension. They must have the same filename as the CHR file. Characters without a BIO file will instead get the generic biography used for Black Pits 2. It works well enough for any class. Note that the biographies are written directly into the CRE/CHR files (i.e. not added as a separate file to the characters folder).
- Portraits in the folder will be copied to the override (though not made selectable at character creation). This does not conflict with my Portrait Gender Separator mod, unless you have different portraits with the same filename.

Black Pits note: Only the premade party will have custom biographies. Imported characters will get the normal BG story-related biography.


#### Additional info:
- Characters are added in number/alphabetical order. This is mainly relevant for the first character, who is treated as the protagonist and cannot be kicked from the party. 
- If there are more than 6 CHR files in the folder, only the first 6 are added to the party (though all will be converted to CRE files in the override).


<details>
  <summary>Biography bug (IWD:EE)</summary>
  
---

- This mod fixes the bug that causes imported characters to start with the BG2 biography. This is done by default for characters added to premade parties. A separate component lets you patch all CHR files in the characters folder.

- This will also delete any BIO files in the folder (required to prevent the bug). The biographies are written directly into the CHR files instead. Characters without a BIO file will get the generic biography from Black Pits 2, but only if the CHR file doesn't already have a custom biography written in.

- It's not completely bug-free. To avoid issues, don't open up the biography screens before starting the game (the status screens are fine). Once you're in the game, you can view any screens without issues. I noticed at least two reproducible bugs on the party creation screen, which I'll describe here:

1. If you view the biography of Player1 (first character in order), then import more characters, then start the game, Player1 will have the BG2 biography.
2. If you view the biographies of any character other than Player1, then start the game, Player1 will have the same biography as the last character viewed. This bug happens with premade parties as well.

- Basically, as long as you don't view biographies while on the party creation screen, there shouldn't usually be issues.

---

</summary>
