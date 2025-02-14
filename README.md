# FIFA Freestyle 16
Mod for FIFA 16 that attempts to recreate gamemodes from FIFA Street 2012



## **[Requirements]**

- FIFA 16 exe product version **16.0.2904053, last updated July 6, 2016** (**I will not be providing any links to game executables**).
- Ability to play in windowed mode (if using the skill points UI without hotkeys (version 1.0.1 only)
- Moddingway Mod 28.0.4 installed (version 1.0.3 and below) or Scouser's FIFA 19-to-FIFA 16 conversion base: http://soccergaming.com/index.php?threads/fifa-19-conversions-db-kits-ect.6465940/ (version 1.0.3.5 and above)
- Understanding that the applications provided are generated through Cheat Engine
- If you choose to run the Cheat Table (.ct) files instead of the executables, download Cheat Engine: https://www.cheatengine.org/
- A bit of time to read through the remainder of this readme



## **[Features]**

- 5v5, 4v4, 3v3, 2v2, and 1v1 action, with or without goalies
- Smaller field
- Three goal sizes: mini, long, and futsal
- Three game modes: Regular (football rules), Last Man Standing, and Skills Battle (both as in FIFA Street)
- Option to set up invisible walls around pitch and disable out-of-play rules
- Heavier ball physics and added curve, roll friction
- Custom draggable street UI for Skills Battle scoring (two sizes):
        
        Color-coded skillmove ID panel:
            - White, Green, Yellow, Red in order of increasing points
            - Blue for Beats and Skill Beats
            - Purple for fancy passes, shots, and pannas
            - Orange for goals
            - Skill Bank displays current accumulated skill move points for dribble possession 
            (resets upon loss of possession)
 
- Disabled slide tackles to force AI into attempting more standing tackles. Leads to more missed tackles and improvement in player ability to beat defenders
(change AI_NO_SLIDE_TACKLE in cl.ini)
- Disabled fouls to recreate street feel
(change AI_SETTING_NO_FOUL in cl.ini)
- Hotkeys for all options (see **[Hotkeys]** section below for more info)



## **[Bugs]**

- AI doesn't do any skills as of this release. However, the AI does attempt flair passes and flair shots
- Players sometimes unresponsive to ball after bounce off walls (if not playing at Manchester Park with OOP disabled)
- Can't change controlled player at times because receiver selection bugs out upon expected out-of-play sequence (same reason as above)
- Goalies unaware of ball position if ball hits wall and bounces towards them (same reason as above)
- Close direct freekicks freeze for a minute during setup of wall due to second/third kick taker or goalkeeper positioned inside goal (recommended to turn off fouls in cl.ini)
- Offsides sometimes called incorrectly when goalies are disabled. **Turning off offsides solves the problem**.
- Player assigned to near post on corner kick will position where post would have stood if field were bigger. These are hard-coded reposition locations.
- Goalie doesn't hug post when ball is near corner
- Sometimes, all players must be teleported onto the field for freekicks to allow continuation of play
- Second, third freekick takers are glitched.
- Panna detection is a bit iffy due to limitations of in-game function used to detect pannas
- Injuries to AI players on the field cause the AI to play shorthanded following substitution of the injured player
(possible solution is to **disable injuries by setting Injury Frequency and/or Injury Severity sliders to 0**)
- Crossbar mesh height above pitch is fixed. However, the collision geometry scales down with the goal net.
- Red cards can cause a host of bugs including swapped-in player not leaving field at the end of a half and bench players floating in the air. To remedy this, **cards have been disabled** (can re-enable in cl.ini)



## **[Installation Instructions]**

**(1.)** 

Ensure that you have a "fifa16.exe" that was last updated on
**July 6, 2016**. Any other .exe version will not be compatible with this mod.

**(2.)** 

**For versions 1.0.3 and below**, install the Moddingway Mod, up to and including version 28.0.4:
https://www.moddingway.com/file/231051.html

This mod uses the 10.0 version of Moddingway's database.
NOTE: Make sure that you backup your current database, if you have one in use:
"fifa_ng_db.db" in FIFA 16\data\db

**For versions 1.0.3.5 and above**, install any graphics files you wish to use from the following thread:
http://soccergaming.com/index.php?threads/fifa-19-conversions-db-kits-ect.6465940/
Make sure that you then install the "Main Directory Files" pack below in the "Downloads" section afterward

**(3.)** 

Either install CG File Explorer 16, CM16, or i68's regenerator.

(If you haven't installed one already). This will be used to regenerate the mod's files once the
installation is complete.

- CG File Explorer:
http://3dgamedevblog.com/wordpress/?sdm_downloads=cg-file-explorer-16-v0-8

- Creation Master 16 2.0:
http://downloads.fifa-infinity.com/fifa-16/creation-master-16/

- i68 Controller 2.2.9:
http://downloads.fifa-infinity.com/fifa-16/i68-controller-2-0-2/


**(4.)** 
           
1. Download the mod's .exe files or the .ct files.
If you want to use the .exe file, then click on the "Programs" folder above, choose your version, and click the "Download" button.
If you want to use the .ct file, click on the "Cheat Tables" folder above, choose your version, click "Download", right-click on the resulting raw data, and save as a .ct file.

2. Then, download the FIFA directory files found below under **"[Downloads]"** for your version.

3.  * *(optional)* * You can also download the executables in the download section, but keep in mind that some antiviruses will flag them as malicious. (see below: "Starting FIFA Freestyle", (2.))

Where to extract:

- Extract the FIFA 16 folder within the archive above to your FIFA 16 main folder and overwrite files as 
necessary. 
- Extract the applications/script/tables in the other archive to a destination of your choice.

**(5.)** 

Regenerate .bh files using any of the programs listed in step 3.
    
Find your FIFA 16 main folder and then:

	a. CG File Explorer: "Regenerate All" button
	b. Creation Master 16: Tools->"Regenerate BH"
	c. i68 Controller: "Regenerator" button

**(6.)** 

Different options:

- cl.ini:

		To re-enable fouls, change AI_SETTING_NO_FOUL = 1 to AI_SETTING_NO_FOUL = 0
		(requires restart of game to confirm changes).
		You'll also find other settings (GK always throws ball, no slide tackling, etc) to play
		around with if you so desire

- pitch files (FIFA 16\data\sceneassets\pitch):

		The pitch file pitch_common_textures.rx3
		has two variants -- one with a white pitch and one with a green pitch. By default, the 
		white pitch is active, but if you want to try out the other version, rename the
		white variant to  something else and rename the green variant to "pitch_common_textures.rx3".

- database (FIFA 16\data\db):

		There are three different databases within the archive. By default, mini goals are enabled:
		-- fifa_ng_db.db             (mini goals)
		-- fifa_ng_db_futsal.db      (futsal-sized goals)
		-- fifa_ng_db_long.db        (long goals)

		If you wish to use a different goal size, rename the db file you want to use to "fifa_ng_db".
		Restart the game, choose the corresponding option in the futsal configurator, and you should 
		see the changes.


- Skills Battle UI:

		Two different sizes offered with versions 1.0.3 and lower (see which works best for you):
		-- Use the 1080p .exe or .ct if you are using a 1080p resolution or below.
		-- Use the 1440p .exe or .ct if you are using a 1440p resolution or above.

		
Once you regenerate, you can edit these files without regenerating again. Upon restart of FIFA 16, you should see your changes.
 
**(7.)** 

* *(optional)* * Install the following font for the UI if you want to: https://www.dafont.com/capture-it.font?l[]=10&l[]=1

**(8.)** 

Change your FIFA game settings to start in **windowed mode** so that the Skills Battle UI can display over the FIFA window.



## **[Starting FIFA Freestyle]**

**(1.)** 

   - If you are using an executable:   

       1. Simply start up the .exe file corresponding to your screen resolution.
       2. Start up FIFA 16.

   - If you are using the cheat table (.ct):

       1. Make sure you have Cheat Engine installed.
       2. Open up the cheat table you want to use.
       3. If Cheat Engine prompts you to run a LUA script, choose "Never".
          This is so that the script does not attach until we want it to.
          You can change this setting later in the "Settings" tab.
       4. Start up FIFA 16.
        
           

**(2.)** 

If your antivirus detects the .exe file as suspicious, it is because the .exe was generated by Cheat Engine and attaches to the FIFA process in order to debug and change its low-level code.

Read up on Cheat Engine here: https://www.cheatengine.org/


**(Optional) To view the Cheat Table's source code**:

Open up the cheat table (say no if it asks to run a LUA script), 
click on "Table" on the menu bar, and click "Show Cheat Table LUA Script". This script will correspond 
with the one found in this repository (same script for both cheat tables and executables).

**(Optional) To generate an exe file for yourself if you don't want to use the ones provided:**

You can generate an exe file of your own (how the exe files are generated) by clicking "Save As", 
change "Save as type" to "Cheat Engine Trainer Standalone", choose where you want to save it, and click "Save". 

A form will pop up. Choose the following settings: "Gigantic", "Target process is 64 bit, "LUA Symbols", 
"Max" for compression. Lastly, choose the icon file found within the downloaded zip file and click generate.


**(3.)** 
        
If you are using an **executable**, choose the settings you wish to play with 
(make sure goal size option matches the db you have active)

If you are using a **cheat table**, click on "Table" on the menu bar and click "Show Cheat Table LUA Script".
Then, when the script appears, click the "Execute" button at the bottom of the window.

If you don't have FIFA 16 open yet, you'll need to click the "Attach" or "Re-attach" button
after you see FIFA's window appear.

Now, you can choose your settings.
  

**(4.)** 

Once the **language selection screen appears**, you can enable the mod using hotkeys or the GUI. Please note that to remain in fullscreen mode, you must use the hotkeys to activate the mod. An audio message should play for each hotkey if activated successfully.

**(5.)** 

If any LUA errors occur, a console window will appear. Common sources of errors include enabling the mod too quickly, at the end of a match instead of before, and not re-attaching to a new FIFA process.

**IMPORTANT**: If error messages continue to print out in rapid succession, close the program and post your error in this thread (include line number).

http://www.soccergaming.com/index.php?threads/fifa-futsal-16.6465838/#post-6512379

## **[Hotkeys]**

Some useful hotkeys:

**General Settings**

- "Shift + F5": Toggle walls around field
- "Shift + F6": Toggle OOP (out-of-play)
- "Shift + F7": Toggle use of goalkeepers
- "Shift + F8": Toggle display of Skills Battle UI (can be shown in other game modes besides Skills Battle but will always show for Skill Battle)
- "Shift + F9": Enable/disable the mod
- "Shift + F10": Attach to the FIFA process. This will be done automatically the first time, but if you have to re-open FIFA, hit "Re-Attach" to attach FIFA Freestyle 16 to the new process (disables mod on re-attach).

**Game Mode Selection**

- "CTRL + 1": Regular game mode
- "CTRL + 2": Last Man Standing game mode
- "CTRL + 3": Skills Battle game mode

**Goal Size**

- "ALT + 1": Futsal goal size
- "ALT + 2": Long goal size
- "ALT + 3": Mini goal size

**Number of Players**

- "CTRL + SHIFT + 1": 1v1
- "CTRL + SHIFT + 2": 2v2
- "CTRL + SHIFT + 3": 3v3
- "CTRL + SHIFT + 4": 4v4
- "CTRL + SHIFT + 5": 5v5

## **[Recommendations and Notes]**

- Best played with fouls off as freekicks and any setplays cause glitches and break immersion because the game must reposition every player at times
- Also best played with walls enabled for the same reason as above
- The Skills Battle game mode emphasizes beating defenders off the dribble and forcing missed tackles
- For Last Man Standing, time is frozen at zero to allow the game to properly conclude when a team nets 5 goals
- Last Man Standing should be played with fouls off, as a red card prevents teams from winning (can't score one goal for every player).
- Halves must be skipped once a team reaches 5 goals to end the game. I have yet to find a way to directly trigger the end of a half

## **[Changelog]**

**1.0.1:**

	- Fixed bug preventing automatic end to half in Last Man Standing
	- Fixed skillgames crash bug (thanks PrinceDiman2018)
	- Removed 3D grass for all graphics settings (thanks PrinceDiman2018)
	- Turned off fouls by default
	
**1.0.2:**
	
	- Added hotkeys for game modes, goal size, number of players, and goalie
	- Changed hotkeys for walls, streetUI, enable, and attach
	- Fullscreen with Skills Battle now supported through hotkey-enabling of mod
	
**1.0.2.5**

	- Added text-to-speech confirmation for all hotkey presses
	
**1.0.3.5**
	
	- Included smaller changes from 1.0.3
	- Manchester Park added courtesy of PrinceDiman2018
	- New base database (Nov. 26, 2018) thanks to scouser09
	- Heavier ball physics, slightly more curve on shots, passes
	- Fixed halftime-end bug
	- Fixed player repositioning for penalties
	- Added OOP hotkey for use with Manchester Park
	- Auto-select Skills UI resolution based on FIFA 16 resolution
	- Realtime update of GUI options when using hotkeys
	- Fixed Skills UI toggler
	- Fixed hotkey activation messages
	- Fixed crashes related to improper unregistering of symbols

## **[Downloads]**

FIFA Main Directory Files for **1.0.3 and below**:

https://drive.google.com/open?id=1BgQg8sf4GmeX15-SB_dhcefuOB78fIW4

FIFA Main Directory Files for **1.0.3.5**:

https://drive.google.com/file/d/1OBhiQQFDBDuPj8AEt5DxZqW5YAym4Pv9/view?usp=sharing

FIFA Freestyle Executables (compiled with CE):

v1.0.1 1440p: 
https://drive.google.com/open?id=1jtoF8PsTIIRJ0QMK9SzrgP4tEp8GeHWW

v1.0.1 1080p: 
https://drive.google.com/open?id=1cvqgo89GG00U6cRv_3kK3dkMKqmdLIWh

v1.0.2 1440p:
https://drive.google.com/open?id=1m4n13qS-QgfiE_Zm0Ah8XVjgW0I8mAeE

v1.0.2 1080p:
https://drive.google.com/open?id=1E471adR5Fo3C_7Upq3F2RiDlRlL4nLLY

v1.0.2.5 (both resolutions):
https://drive.google.com/open?id=1H62uLjeXXte_GI6bRCnNj1ui2FhwYsPq

v1.0.3.5:
Found above in the "Programs" folder or below:
https://drive.google.com/file/d/1PkULtZLJUI3Wm6Hlg9dXKmKov9Oa1oZm/view?usp=sharing

## **[Contributors]**

**PrinceDiman2018:**
- pausemenuflow.nav file fix for skillgames crash pre-match
- Removal of 3d grass
- Manchester Park (replacing Training Center)
- Removal of autoexposure effects for uniform lighting independent of weather

## **[Credits]**

- Dark Byte for Cheat Engine:
https://www.cheatengine.org/

- Ariel and the Moddingway Team for the Moddingway Mod:
https://www.moddingway.com/

- Scouser09: 19->16 db, kit, ball, and logo conversions: 
http://www.soccergaming.com/index.php?threads/fifa-19-conversions-db-kits-ect.6465940/

- Tokke001: Loc files, jersey, kit fonts, shoe collection, minifaces:
http://www.soccergaming.com/index.php?threads/fifa-19-conversions-db-kits-ect.6465940/page-2

- imNICKED & eddyedwards10, nabo, pao and pillowbiter for the shoes included in tokke001's collection:
http://www.soccergaming.com/index.php?threads/imnicked-eddyedwards10-boot-thread.6465313/

- Rinaldo for Creation Master 16

- Shawminator for CG File Explorer 16

- iard68 for i68 Controller

- Koczman Bálint for the Capture It font
