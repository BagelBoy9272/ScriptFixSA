# ScriptFixSA

<p align="center">
  <img src="https://i.ibb.co/jkphV2dG/logo.png" alt="Logo">
</p>

ScriptFixSA aims to provide bugfixes and quality of life improvements to the original scripts. It also restores some of the cut content, but only the type that was cut unintentionally (due to a code bug) or something that developers likely forgot to add due to tight deadlines and that doesn't break the plot, characters or game's lore. There's no intent to reuse every bit of unused content for the sake of it, or to recreate cut/rumored missions. Based off of [UndefinifiedGrove](https://github.com/Sergeanur/UndefinifiedGrove). Heavily inspired by [SCFIX-Liberty](https://github.com/Sergeanur/SCFIX-Liberty), [SCFIX-Miami](https://github.com/Sergeanur/SCFIX-Miami), [GTA-SA---SCM-Fixes](https://github.com/Domiiniik/GTA-SA---SCM-Fixes) and [TTDISA](https://gtaforums.com/topic/939012-things-to-do-in-san-andreas-volume-ii/)

Relevant or otherwise interesting changes to the scripts were marked with a `FIXEDGROVE` comment.

Currently in beta status.

## Download

Get latest release here: https://github.com/BagelBoy9272/ScriptFixSA/releases

## Installation

Extract the downloaded .zip file and replace main.scm and scripts.img inside data\scripts directory, but read save files and mod compatibility note below first.

## List of changes

<details><summary>Click here to expand</summary>
<br>

®️ = (some) listed changes from official post PC 1.0 revisions.

General:
- Based on the latest official version (JP 2007), with merged changes from latest PC branch, without censorship
- Refactored code bloat created by the Japanese support
- Removed On Mission flag checks in some missions that were meant to bypass compiler errors
- Made cutscene skips consistently use IS_SKIP_CUTSCENE_BUTTON_PRESSED instead of a cross or circle button press check
- Corrected 'missions attempted' and 'missions passed' stats.

Intro cutscene:
- Restored PS2 REV 1 size for text
- Fixed stretched text

Big Smoke/Sweet & Kendl:
- Fixed drive-by Ballas standing still to the right of the player after the Mulholland Intersection cutscene, instead of being teleported and frozen under the map
- Made Groves hate scripted ballas
- Made Ballas respect scripted ballas
- Deleted some useless code

Ryder:
- Fixed Ryder's car spawning only being turned ON on mission pass
- Added ability to skip ending cutscene

Tagging Up Turf:
- Sweet now switches to the driver's seat before driving off
- Fixed Sweet being parked at Grove Street after driving off
- Added ability to skip ending cutscene

Cleaning the Hood:
- Fixed bat pickup clipping into the ground
- Removed "IS_IN_CAR" checks for the dialogue, to make it flow more naturally
- Made Ryder aggresive towards the drug dealer and the enemies inside the crack den
- The cutscene with the dead drug dealer will fade out if skipped
- Fixed chars not being set in their intended locations if you skip the cutscene inside the crack den
- Made "drugged" chars inside the crack den silent
- Added an anim to Ryder in the ending cutscene
- Made player and Ryder look at eachother in the ending cutscene to make it look more natural
- Added ability to skip ending cutscene
- Set SHUT_CHAR_UP_FOR_SCRIPTED_SPEECH for player to false in cleanup
- Added STOP_CHAR_FACIAL_TALK for player in cleaup
- Slight refactoring

Drive-Thru:
- Fixed Sweet and Smoke changing seats after the drive-thru cutscene
- Made freeroam Ballas respect scripted Ballas
- Made Groves hate scripted Ballas

Nines And AKs:
- Made "cycling through targets" help box only show up if using a controller, otherwise display unused help box about gun recoil

Cesar Vialpando:
- Fixed ghost town after getting the Savanna and before entering Loco Low Co.
- Lowrider meet peds are only deleted after the cutscene
- Fixed mission passed tune not playing

Sweet's Girl:
- Fixed possible softlock in the initial cutscene

Home Invasion:
- Fixed Ryder vanishing in the ending cutscene
- Made player look at Ryder during 'CJ, you gotta get it into your head...' line to make it look more natural
- Moved task clearing after the fade out so they aren't stopped suddenly during it

Catalyst:
- Removed check that prevented Ryder from teleporting to intended location in ending cutscene
- Added facial talk anim to voicelines
- Added ability to skip intro cutscene
- Fixed a bug where the car conversation wouldn't resume if you got out of the car
- Replaced fake explosion with real explosion, bringing back unused lines and the possibility to destroy the car in the box throwing section
- Fixed a now revealed bug where the unused quotes in the box throwing section would trigger when a box was thrown, and not when it exploded
- Changed Grove's Uzis to Tec9s
- Changed Balla's Greenwood to a Tahoma
- Made player stop looking at Ryder before the fade out in the ending cutscene
- Removed some pointless code

Robbing Uncle Sam:
- Added a fade in after the initial cutscene
- Fixed 'Now get in there and open the damn gate!' line not playing at 30 FPS due to the gate closing sooner at higher framerates

OG Loc:
- Added facial talk anim to voicelines
- Deleted redundant SHUT_CHAR_UP calls, since now its handled by the audio code
- Reverted a timer that was set to zero for debug
- Deleted redundant DRAW_SPHERE calls, and moved it to after the cutscene where you go to Jeffrey's house ends
- Commented a tiny bit of debug code
- Removed "IS_IN_CAR" checks for the dialogue after killing Jeffrey, to make it flow more naturally
- Increased upper limit in random number generator, effectively bringing back an unintentionally unused random car plate
- Swapped an if chain with a switchcase

Running Dog:
- Added facial talk anim to voicelines
- Fixed an animation check that was supposed to make the running vagos member faster
- Made Smoke respect player and Grove members, so he doesn't shoot them if provoked
- Set SHUT_CHAR_UP_FOR_SCRIPTED_SPEECH for player to false in cleanup

Wrong Side Of The Tracks:
- Added facial talk anim to voicelines
- Added small pause before the dialogue plays on the way to the train station
- Now you can kill the 4th vagos member before he gets killed by the railing
- In case of the railing killing him, an unused voice line plays
- Now smoke's warning for the second train will only play if you choose the lower path, otherwise, an unused voice line plays
- Removed "IS_IN_CAR" checks for the dialogue on the way back, to make it flow more naturally
- Added ability to skip ending cutscene
- Made difficulty flag global, so now it works as intended
- Restored objetive text when you get out of the car
- Tweaked order of widescreen commands so they aren't set during a fadeout, only after one

Just Bussiness:
- Added facial talk anim to voicelines
- Restored a possibly unintentionally unused line
- Made difficulty flag global
- Sligthly changed the order of STOP_CHAR_FACIAL_TALK commands to be more precise

Burning Desire:
- Now if player already has molotovs, they are not required to go pick them up in the alley
- Added timers to ending cutscene to prevent softlocks
- Proofed Denise in ending cutscene to prevent softlocks
- Remove the alley molotov pickup in cleanup

Los Sepulcros:
- Removed respect requirement to enable unused part of the mission back

Reuniting The Families:
- Added facial talk anim to voicelines 
- Added facial talk anim to Grove members outside the motel
- Added back missing subititles for swat lines
- Fixed code for healing the player setting his health to 100 even if he had more 
- Disabled collision for Grove member that falls from the railling, and made him silent 
- Slightly adjusted dead Grove member position to avoid clipping and make sense contextually 
- Changed detection radius a bit for breach door swats, and made one stand rather than duck to match his anim 
- Grove member behind table will now shoot the swats in the hallway, and will die if he's not dead after a certain point 
- Fixed a bug where the upside down swat would sometimes freeze after killing him, fixed muzzleflash and trace positions, fixed him not hitting you if you're crouched, and Increased damage and reduced time between shots 
- Fixed CJ still moving his mouth after 'It's Smoke and Ryder!' line 
- Fixed facial anim for CJ's 'hit the gas' line
- Made difficulty flag global, so now it works as intended
- Added CJ and Sweet to donuts cutscene 
- Fixed cop car not breaking all the scaffolding when he crashes through it in the chase section 
- Replaced reused nonsensical 'Hey CJ, watch to the left' line with unused Smoke line 
- Added back commented fences in heli setpiece 
- Fixed heli going limp in the next camera shot
- Opened front passanger seat of sweet's car in final cutscene
- Fixed jarring time shift in ending cutscene caused by the script setting the time to 7:00 AM 
- Fixed characters not using their intented animation groups 
- Add 4 star wanted level if the player fails the mission after getting to the motel 

Tanker Commander:
- Proofed Whittaker in final cutscene to prevent softlocks

Big Smoke's Cash:
- Fixed mission cancelling suddenly if player gets a phonecall
- Courier blip is only added if the mission was accepted
- Earnings and Weekday reminder are only displayed if the mission was accepted
- Added mission passed tune
- Gave a weapon to the courier, in case he ever gets out of the car
- Increased upper limit in a random number generator, effectively bringing back a unintentionally unused route
- Increased cash reward: each crate rewards you with $1200, for a total of $7200
- The mission can no longer be rejected if the player cancels the phonecall the first time around
- If player starts another mission, the mission will be considered "cancelled" and will effectively be treated as if it wasn't accepted
- The courier and his car are made vulnerable on mission cleanup
- If the player completes the mission (collects all crates) the courier will try to pursue the player, and the goons will keep shooting the player

Yay Courier:
- Fixed mission cancelling suddenly if the player got a phonecall
- Fixed edge case where if the player kills the courier without damaging the coke, very little money will be awarded since the timer used for earnings calculations is never set to 0
- Courier blip is only added if the mission was accepted
- Earnings and Weekday reminder are only displayed if the mission was accepted
- Increased maximum cash reward to $8000
- Use unused negative responde audio for phonecall choice (instead of reused one from 'Life's A Beach')
- Removed some pointless cleanup

King In Exile:
- Fixed softlock if player dies during the phonecall after the cutscene

Farewell, My Love...:
- Fixed Woozie ped model being used instead of Claude
- Swapped an opponent's car with Claude's car, to match the cutscene

Air Raid:
- Fixed "stealing" of player's heavy weapons

Supply Lines:
- Fixed rural cops and streaming issues

Beefy Baron:
- Fixed rural cops and streaming issues

Mountain Cloud Boys:
- Fixed occasional softlock when you reached the meeting area

Lure:
- Now uses intended variant of Rancher

Ice Cold Killa:
- Fixed typo in coords for CREATE_BIRDS command 

Customs Fast Track:
- Fixed the ped model used for the guard not matching their voice

You've Had Your Chips:
- Fixed an issue where you could skip the creation of an enemy if you never destroyed exactly 3 machines

Fender Ketchup:
- Fixed right handbrake turns not counting 

Up, Up And Away!:
- Fixed stationary minigun removing the player's heavy weaponry
- Fixed minigun not being removed if the player dies while using it

Breaking The Bank At Caligula's:
- Fixed this mission permanently altering PEDTYPE_CIVMALE relationship towards player
- Fixed the player's haircut being temporarily reset for no apparent reason

Home Coming:
- Fixed the player dying if he was still in the Vincent when the mission ended

Cut Throat Bussiness:
- Set camera behind the player and fade in after the initial cutscene

Grove 4 Life:
- Fixed Sweet and player spawning outside CJ's house instead of Sweet's house

Riot:
- Fixed duplicated Sweet's car in Grove Street

Los Desperados:
- Made Aztecas friendly to the Grove after this mission

End Of The Line:
- Fixed swat member being spawned out of the map due to typo
- Disabled mod garages to prevent issues

GFs:
- Disabled sex censorship
- Made locked version of GFs' cars have the unlocked version's license plate
- Fixed Katie not liking stunts
- Fixed Katie not liking fast driving
- Fixed Katie not liking the zone she lives in
- Fixed Katie tai chi exit animation when meeting her
- Fixed GF's door visibly snapping back in the initial cutscene when you pick her up
- Fixed wrong variable usage for LIKES_PARKING_ROMANTIC check, restoring proper functionality
- Fixed a diner that was marked as a bar
- Now GFs that like fast driving will comment on it
- Only play TAKE_HOME_HAPPY context if the date was actually good, otherwise play TAKE_HOME_ANGRY context
- Play unused GFRIEND_OFFER_DANCE context while on a club if player is on a dancing date
- Fixed Millie using a Feltzer instead of a Club in two-timing events
- Fixed two-timing only working if you always rolled the chance for it, and never got caught
- Fixed car bj increasing progress indefinitely
- Fixed progress only increasing from kissing if the GF liked kissing in public
- Fixed slightly lopsided two-timing chance
- Fixed jealous girlfriend not being considered dead if the player destroyed her car
- Fixed two-timing being triggered while exiting interiors, causing the cutscene to take place in the void
- Two-timing cars will now appear with their correct license plates
- Slightly changed timing of two-timing cutscenes to make them more natural
- Don't loop two-timing cutscene anims, and make them play all the way through when changing camera angle
- Fixed GF not running away in the "caught" two-timing cutscene, as was originally intended
- Fixed jealous GF not being properly marked as dead (previously you could still go on a date with her, in which she dumped you)
- Now when you kill a jealous GF, the ominous "Your girlfriend is dead." message will appear
- Fixed special GF phonecall help box (It's a call from X) only working for the dump phonecall and the 1st conversation variation
- Fixed date phonecalls reducing progress if the player couldn't answer
- Made dump phonecalls retry if the player couldn't answer
- Refactored GF phonecalls related code

Parachute:
- Fixed landing animation
- Fixed a bug where the parachute "fails to open" if you have the "keep weapons after death" bonus and you die with a parachute in your inventory
- Fixed weird twitch after landing
- Fixed parachute going through the floor
- Uncommented some code to allow the full "landing in water" anim for parachute to play

Misc:
- Fixed Ryder's car not spawning depending on mission order
- Fixed pimp submission undoing the relationship change from Ballas towards player set in 'Drive-By'
- Fixed Didier Sachs not being flagged as unlocked
- Fixed possible softlock if the player answered a loanshark phone call while 'Are You Going To San Fierro?' wasn't unlocked
- Fixed script not checking if player answered Rosenberg's phone call before enabling 'Vertical Bird'
- Fixed gym glitch by using 'Days Passed' stat instead of calendar date
- Fixed basketball glitch
- Fixed Quadruple Insane Stunt
- Fixed crappy cone deletion code in bike school and driving school deleting random objects (Blackboard glitch)
- Fixed missing Pizza Stack icon in Montgomery
- ®️ Fixed missing barber shop icon in El Quebrados
- Fixed duplicated Binco icon in Juniper Hill, SF
- Fixed 'The Big Spread Ranch' private dance not counting towards 'strip club budget' stat
- Fixed scripted idle stance in pool not working if the player was fat or muscular
- Fixed upper bound on a random number generator in the dance minigame, effectively bringing back an unintentionally unused partner model
- Fixed typo in the license plate of Cesar's car
- Fixed badly positioned 'no medal' sprite in Driving School introduced in JP version development
- Fixed infrared goggles not respawning after being picked up
- Fixed body armour inside Madd Dogg's mansion not respawning after being picked up
- Fixed a country rifle pickup that was inside the stadium in SF
- Fixed a knife pickup that was under the ground near an underpass in SF
- Moved AK47 pickup in film studios closer to the ground
- Moved bribe pickup inside a building in Doherty to an alley nearby based on comment and Bradygames guide position
- Made Ryder's car stop spawning after 'Pier 69'
- Disable spawning of Sweet's car after 'Reuniting the Families' and don't enable it until 'Home Coming' is completd
- Changed 'Customs Fast Track' reward vehicle to a Jester instead of a Savanna
- Changed Maverick in San Fierro police helipad to a police Maverick
- Moved Hunter and Leviathan spawn coords in the abandoned airstrip to allow both of them to spawn simultaneously
- Moved Seasparrow spawn coords in the helipad near the boat school so it doesn't overide the Maverick spawn
- Moved Import/Export Huntley spawn coords outside the driving school so it doesn't override the reward Hotknife
- ®️ Moved NRG-500 and FCR-900 spawn coords outside the bike school to allow both of them to spawn simultaneously
- Turn taxi lights off when the taxi submission ends
- Made Bike Shool and Boat School use blank 'no medal' sprite in languages other than english
- Made food carts use corresponding ped models
- Swapped NOT HAS_MISSION_AUDIO_LOADED check for 'At least it was before I fucked everything up' voice line to before the actual audio plays
- Made triad members spawn as bouncers in Four Dragons casino
- Pool now increases previously unused win, losses, and 8 balls stats
- Increased weekday check for Kick Start by one, now its avaliable on sundays, tuesdays and thursdays, instead of mondays and wednesdays (previously the first check was, if weekday = 0, which is impossible since the valid range for "weekday" is 1 thru 7)
- Made the motel props from 'Reuniting The Families' spawn in freeroam
- Made the storm drain grate from 'Just Business' spawn in freeroam
- Made the house windows from 'Burning Desire' spawn in freeroam
- Made crack factory front gate spawn in freeroam
- Restored unique custom plates for import/export from PS2 REV 1
- ®️ Now you can quit the "Let's Get Ready to Bumble" arcade game mid-game
- ®️ Now you can quit the "Go Go Space Monkey" arcade game mid-game
- Added facial talking anim to phonecalls
- Each Trucking and Quarry mission now plays the mission complete tune (previously only the last one did)
- Each Trucking and Quarry mission now counts towards total progress % (previously only the last one did)
- Each mountain bike race now counts towards total progress % (previously only the last one did)
- Burglary now counts towards total progress %
- Triathlons now count towards total progress %
- Now if you complete both triathlons, you'll be awarded maximum stamina, previously this only worked if the player completed the Fisher's Lagoon triathlon first
</details>

## Save files compatibility

At this point it's incompatible with old save files made with original script. In future it's possible to come up with a save file converter once a stable release will be decided upon.

## Mod compatibility

Not compatible with some CLEO scripts.

If using SilentPatch, its recommended to set `EnableScriptFixes` to `-1` in its .ini file, although this is not strictly necessary because SilentPatch is designed to bail out any script fixes if the code doesn't match. Doing so also stops the save pickup inside Madd Dogg's mansion from being relocated since a different method is used to fix the "Basketball Bug".

## How to compile

You need to get sc.exe from 3master and then patch the 3master plague out of it. Also you need some extra files for sc.exe to work properly.
To patch sc.exe, put it in `patch` directory and launch **xdelta3.bat**. Then take sc.exe back to `data` directory and take these files from `patch` directory too: `AudioEvents_PS2.txt`, `AudioEvents_PC.txt`, `AudioEvents_XBOX.txt`, `HID_Base.h`, `TouchInterface_SA.h`.

Notes and pro tips:
- Changing target platform via command line is possible only for PC. To pick different platform you must launch sc.exe, pick it in Target, and then close it. The target platform will be saved in a registry key. Then you can compile sc with command line, the platform you chose will be saved
- I don't know what Xbox 360 target does. Since it's a plague leftover I just ignore it and so should you.
- Compiled OG files always had debug lines converted to UPPERCASE, however plagued sc.exe doesn't do that and leaves case as is. I decided not to bother patching that for now, since it's a benign side effect.

## Thanks

Sergeanur for curing the original scripts.  
Silent for help in implementing his script fixes.  
bamspeedy1298 for his stats guide on GameFAQS.  

OrionSR, TheoTTG, Deezire, Silent, Domiiniik, ArmanCan, StreetFonso, Nick007J, Vadim M and Kaizo M for documenting script bugs and oddities.

