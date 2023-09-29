Version 1.9 - by Richy Rich

Table of Contents - CTRL+F and copy one of these to go straight to the desired Command/Section
Commands:

# Better borderless window support
# God Mode!
# Immortal Mode!
# Player weapon damage resistance
# No fall damage
# Increased melee damage
# Disables enemy health gain per level
# Add credits
# Sets your character to the specified level
# Add XP
# XP Multiplier
# Add skill points
# Movement speed multiplier
# Increasing CO2 multiplier
# Digipicks
# Carryweight
# Removes all items from the inventory of the target
# Change character crew amount
# Unlocks the targeted door or container
# Activates the targeted item
# Sets ownership of targeted item to player
# Shows all markers on a planet
# Toggles the UI on and off
# Toggle All AI Processing
# Unlocks all 24 powers
# Total power
# Power recovery speed
# Power recovery rate
# Relax faster after aggro
# No Clip
# Toggle free camera
# Camera FOV
# Distance to recieve greeting missions
# Gets the ref ID of the grabbed item
# Duplicates targeted item
# Kills all hostile NPCs in the vicinity
# NPCs will no longer target and attack you
# All speech challenges automatically succeed
# Passes the specified number of hours
# Opens the wait/pass time menu
# Opens the character creator
# Suicide
# Kills target
# Resurrects target
# Reload speed
# Aim stability increase
# Change max ownable ships
# Increase max scan range
# Instant scan
# Increased highlight range
# Show more points of interest
# More custom landing sites
# Pickpocket 100% chance
# Make current NPC a teammate
# NPC visual abilities
# Distance from enemies from being detected
# NPC View Cone
# Vendor selling price multiplier
# Days to restock Vendor inventory
# Give max auto hack attempts
# Earn auto attempts per hack
# Encounter zone levels
# Chance for NPC to drop equipped armor

Sections:
# Legendary enemy spawn chance multiplier
# Damage multipliers
# Boostpack settings
# Auto-Aim Settings
# Ship IDs
# Ship modifiers
# Outpost settings
# Companion Affinity
# Get companions unstuck
# Fast travel locations
# Crime settings
# House prices
# NeuroAmps
# Resources/Parts/Minerals/Crafting Material Items
# Food/Drinks/Aid
# Powers
# Perks/Backgrounds
# Companion perks
# Backpacks
# Backpack mods
# Spacesuits
# Armor mods
# Clothes
# Apparel mods
# Helmets
# Helmet mods
# Weapons
# Weapon modifiers
# Ammo
# Mission/Quest settings
# All Main Mission IDs
# Shipyard parts
# Easy Lockpicking
# Spawn Enemies
# Plushies
# Magazines
# Artifacts
-------------------------------------------------------
# Better borderless window support(keep game active when alt+tab)(Default "0")
SetINISetting "bAlwaysActive:General" "1"

# God Mode! Makes you and your ship invincible and gives you unlimited ammo + boostpack + CO2
tgm

# Immortal Mode! You can take damage but your health will never hit 0
tim

# Player weapon damage resistance(Adds to the total value each time, do - to decrease value)
player.modav DamageResist 1000
player.modav EnergyResist 1000
Player.modav electromagneticdamageresist 1000
player.setav ENV_Resist_Airborne 85
player.setav ENV_Resist_Corrosive 85
player.setav ENV_Resist_Radiation 85
player.setav ENV_Resist_Thermal 85

#No fall damage
Setgs fJumpFallDamageMult 0

#Increased melee damage(Default 1)
player.setav meleedamage 10

#Disables enemy health gain per level(Default 20)(Increase to make enemies harder to kill per level)
setgs fNPCHealthLevelBonus 0

#Add credits - Note: You can also replace "player" with a "vendor ref ID" to give a vendor credits
player.additem f 100000000

#Sets your character to the specified level(Note: your level can only go up not down, max is 998)
player.setlevel 10

#Add XP
player.modav experience 100000

#XP Multiplier(Default 1)
setgs fXPModBase 2

#Add skill points
CGF “Game.AddPerkPoints" 1000

#Movement speed multiplier(Default: 100). Increase to run faster
player.setav speedmult 500

#Increasing CO2 multiplier(Default 2)
SetGS fOxygenToCarbonDioxideMult 1.50000

#Digipicks
player.additem a 100

#Carryweight
player.modav carryweight 100000000

#Removes all items from the inventory of the target - Open console and click the target to reveal their ref ID and enter the command.
removeallitems				Removes items
removeallitems player		Removes items and moves to players inventory
removeallitems (target ID)	Removes items and moves to specified target

#Change character crew amount
player.setav 160030 50 

#Unlocks the targeted door or container - Open the console and click the object you want to unlock with your mouse to reveal the ref ID
unlock

#Activates the targeted item - Open the console and click the object you want to unlock with your mouse to reveal the ref ID
activate

#Sets ownership of targeted item to player - Open the console and click the object you want to unlock with your mouse to reveal the ref ID
setownership

#Shows all markers on a planet
tmm 1

#Toggles the UI on and off.
tm

#Toggle All AI Processing
tai

#Unlocks all 24 powers
psb

#Total power(Default 60)
player.setav starpower 60

#Power recovery speed(Default 100)
player.setav starpowerratemult 100

#Power recovery rate(Default 1)
player.setav starpowerrecoverrate 1

#Relax faster after aggro(Default 1)
SetGS fGunPlayerRelaxedWaitTime 0.5

#No Clip. Allows you to move through walls and other objects
tcl

#Toggle free camera
tfc

#Camera FOV(70-120)
First person: SetINISetting "fFPWorldFOV:Camera" "120"   Default 75
Third person: SetINISetting "fTPWorldFOV:Camera" "120"   Default 75
SetGS "fFlightCameraFOV:FlightCamera" 120                Default 90

#Distance to recieve greeting missions
getgs fAIMinGreetingDistance       Get current value
setgs fAIMinGreetingDistance 20    Set current value

#Gets the ref ID of the grabbed item
getplayergrabbedref

#Duplicates targeted item
spawndupe

#Kills all hostile NPCs in the vicinity
kah

#NPCs will no longer target and attack you
tcai

#All speech challenges automatically succeed(2 varients, Dont need to use both)
setforcespeechchallengealwayssucceed 1
Player.setav playerpersuasionskillsuccesschancemult 100

#Passes the specified number of hours.
passtime 1

#Opens the wait/pass time menu.
showmenu sleepwaitmenu

#Opens the character creator. (Note you will need to alt+F4 if you wish to exit without editing)
showlooksmenu player 1		Original start game creator
showlooksmenu player 2		Enhanced creator

#Suicide
player.kill

#Kills target - Open console and click the target to reveal ref ID then enter command
kill

#Resurrects target - Open console and click the target to reveal ref ID then enter command
resurrect

#Reload speed
Default(Dont change): player.forceav WeapReloadSpeedMult 0.00
Increased(0.75 = 75% increased from default): player.modav WeapReloadSpeedMult 0.75

#Aim stability increase
Default(Dont change): player.forceav AimStability 1.00
Increased(0.75 = 75% increased from default): player.modav AimStability 0.75

#Change max ownable ships
SetGS uSpaceshipMaximumOwnedSpaceships 500

#Increase max scan range(Default 10)
SetGS fHandScannerScanRange 250.0

#Instant scan
SetGS iHandScannerAnimalCountBase 1
SetGS iHandScannerPlantsCountBase 1

#Increased highlight range(Default 100)
SetGS fHandScannerBaseRange 500.0

#Show more points of interest
Note: Setting the value higher than 1500 is not recommended. This may result in POIs not being displayed in close proximity.
SetGS fHandScannerMapMarkerMinRange 1500

#More custom landing sites(Default 3)
SetINISetting "uLandingKeepBufferSize:Landing" "49"

#Pickpocket 100% chance
setgs fPickPocketMinChance 100
setgs fPickPocketMaxChance 100

#Make current NPC a teammate(0 removes teammate status)
SetPlayerTeammate 1

#NPC visual abilities(Stealth level)(Default -20)
SetGS fSneakVisualBaseValue -100.0000

#Distance from enemies from being detected(Default 2)
SetGS fSneakDistanceAttenuationExponent 10.0000

#NPC View Cone(How wide is their vision)(Default 190)
SetGS fDetectionViewCone 170.0000

#Vendor selling price multiplier(Default 0.125)
SetGS fVendorSellPriceMult 0.5000

#Days to restock Vendor inventory(Default 2)
SetGS iDaysToRespawnVendor 1

#Give max auto hack attempts(Do 1 hack to apply)
player.setav 3b0 1000

#Earn auto attempts per hack(Do 1 hack to apply)
player.setav 3b1 1000

#Encounter zone levels
setgs uDefaultLevelZone01max 100	Default 5
setgs uDefaultLevelZone02max 100	Default 14
setgs uDefaultLevelZone03max 100	Default 25

#Chance for NPC to drop equipped armor(Default .1)
SetGS fEquippedArmorChanceToDrop 0.75
-------------------------------------------------------
#Legendary enemy spawn chance multiplier
Very Easy game mode(Default 0.2500)
SetGS fDiffMultLegendaryChance_VE 0.5000

Easy game mode(Default 0.5000)
SetGS fDiffMultLegendaryChance_E 0.7500

Normal game mode(Default 1.0000)
SetGS fDiffMultLegendaryChance_N 1.5000

Hard game mode(Default 1.5000)
SetGS fDiffMultLegendaryChance_H 3.0000

Very Hard game mode(Default 2.0000)
SetGS fDiffMultLegendaryChance_VH 5.000
-----------------------------------------------------
#Damage multipliers(Default 1) - Note: This works for ships and player
Damage by player(Increase to give instant kill)
setgs fDiffMultHPByPCVE 10		Very Easy
setgs fDiffMultHPByPCE 10		Easy
setgs fDiffMultHPByPCN 10		Normal
setgs fDiffMultHPByPCH 10		Hard
setgs fDiffMultHPByPCVH 10		Very Hard

Damage to player(0 is god mode)
setgs fDiffMultHPToPCVE .1		Very Easy
setgs fDiffMultHPToPCE .1		Easy
setgs fDiffMultHPToPCN .1		Normal
setgs fDiffMultHPToPCH .1		Hard
setgs fDiffMultHPToPCVH .1		Very Hard
-----------------------------------------------------
#Boostpack settings

Hold boostpack button instead of pressing
SetINISetting "bUsePressAndHoldControls:Boostpack" "1"

Energy drain rate for sustained flight(Default - 160)
player.setav boostpackdraininitial 0

Energy drain rate for initiating flight(Default - 35)
player.setav boostpackdrainsustained 0

Upward thrust for sustained flight(Default - 250)
player.setav BoostpackThrustInitial 175

Upward thrust for initiating flight(Default - 60)
player.setav BoostpackThrustSustained 45

Increase horizontal boostpack(set & use alt jump key in Bindings)
player.setav BoostpackHorizontalPercentage 2.55

Unlimited boost pack hover(aiming and shooting weapon while boosting)
player.setav boostpackhoverfueldrainav -999
-------------------------------------------------------
#Auto-Aim Settings - put all of them to 0.0000 to disable Auto-Aim feature
First Person Auto-Aim(Default 1):
SetGS fAutoAimMaxDegrees 0.0000

3rd Person Auto-Aim(Default 2):
SetGS fAutoAimMaxDegrees3rdPerson 0.0000

Auto-Aim Screen Percentage(Default 6):
SetGS fAutoAimScreenPercentage 0.0000
-------------------------------------------------------
#Ship IDs - Instructions to spawn and save:
Spawn your desired ship and Noclip by entering the command tcl. Find the entrance, open the command console, use your mouse to select the door and to see the Ref ID(DOOR " (ID)(Tip: scroll and you might be able to find it)), use the "unlock" command to unlock the door and gain access. Should this not work, try opening the door from the inside of the ship. When the ship is finally accessible, be sure to retype the command "tcl" to turn off clipping mode.

A Class
player.placeatme 001322D8 	Star Eagle 				A
player.placeatme 0000B730 	Frontier 				A
player.placeatme 0002CC6C 	Razorleaf 				A
player.placeatme 001322D8 	Star Eagle 				A
player.placeatme 00180F18 	Starborn Guardian 		A
player.placeatme 001E29E5 	UC Prison Shuttle 		A
player.placeatme 00038B42 	Wanderwell 				A
player.placeatme 003A2E83 	Achilles 				A
player.placeatme 0031DF00 	Crimson Fleet Ghost 	A
player.placeatme 0031DF60 	Crimson Fleet Haunt 	A
player.placeatme 00322BE1 	Crimson Fleet Phantom 	A
player.placeatme 002E7461 	Discovery 				A
player.placeatme 002CE40B 	Econohaul 				A
player.placeatme 0021CEAD 	Galileo 				A
player.placeatme 00147C8D 	Gladius 				A
player.placeatme 0038895D 	Kfir 					A
player.placeatme 0021C44B 	Longsword 				A
player.placeatme 001EB556 	Mako 					A
player.placeatme 000F2C63 	Marathon 				A
player.placeatme 003A2E8F 	MULE 					A
player.placeatme 00388965 	Mustang 				A
player.placeatme 0020C644 	Narcissus 				A
player.placeatme 001E052A 	Pik Up 					A
player.placeatme 00042372 	Rambler 				A
player.placeatme 003A2E6B 	Responder 				A
player.placeatme 00215E9B 	Sparrow 				A
player.placeatme 000423AB 	Thresher 				A
player.placeatme 003A2E5F 	Transpo 				A
player.placeatme 001A39A8 	Trebuchet 				A
player.placeatme 000F31CE 	Vagabond 				A
player.placeatme 000F31C9 	War Horse 				A
player.placeatme 0020AFD0 	Watchdog 				A
player.placeatme 003A2E71 	Wendigo 				A

B Class
player.placeatme 000F2DBE 	Shieldbreaker 			B
player.placeatme 003A2E35 	Starhawk 				B
player.placeatme 000F3078 	Aegis 					B
player.placeatme 001E0528 	Big Rig 				B
player.placeatme 0038239C 	Bireme 					B
player.placeatme 002E753C 	Falcon 					B
player.placeatme 001A7F69 	Hammerhead 				B
player.placeatme 000D5575 	Hoplite 				B
player.placeatme 000F31C5 	Murasame 				B
player.placeatme 003A2E41 	Naginata 				B
player.placeatme 0037F546 	Privateer 				B
player.placeatme 003A2E3B 	Pterosaur 				B
player.placeatme 0033A1C6 	Ranger 					B
player.placeatme 0021CEAB 	Roanoke 				B
player.placeatme 000F31C7 	Shackleton 				B
player.placeatme 000FAFE8 	Slipstream 				B
player.placeatme 0036D871 	Space OX 				B
player.placeatme 003A2E35 	Star Hawk 				B
player.placeatme 003A2E1D 	Sunsail 				B
player.placeatme 00347145 	Trade Wagon Train 		B
player.placeatme 0018D3F0 	Venture 				B
player.placeatme 003A2E47 	Wagontrain 				B
player.placeatme 000F31D0 	Wanderlust 				B
player.placeatme 0002C88F 	Zumwalt 				B

C Class
player.placeatme 000F31DB 	Abyss Trekker 			C
player.placeatme 0038D65C 	Autobahn 				C
player.placeatme 0038D656 	Civshuttle 				C
player.placeatme 003A2E11 	Dragonfire				C
player.placeatme 003A2E0B 	Dullahan 				C
player.placeatme 000F3076 	Narwhal					C
player.placeatme 0038234D 	Orca 					C
player.placeatme 000F2E5B 	Silent Runner			C
player.placeatme 0003CFB2 	Star Semi 				C
player.placeatme 000F31E4 	Stronghold 				C
player.placeatme 00001E9F 	Vanquisher 				C
player.placeatme 0003CF9C 	Vindicator 				C
-------------------------------------------------------
#Ship modifiers - Use command "player.getspaceship" to get Ref ID of spaceship, Must be in ship. Or go into space in your ship, open your scanner and enter photo mode then open the console and click your ship to reveal the ref id and then enter the command you want.
(Ref ID).setav (command)

.setav spaceshipreactorpower 72		Add reactor power to current amount
.setav spaceshippartmass 0			Change your part mass in total
.setav spaceshipgravjumpfuel 10000	Change your jump fuel amount
.setav spaceshippassengerslots 50	Carry more passengers on your ship
.setav SpaceshipCrewRating 50		Change max crew rating of the ship
.setav SpaceshipCrewSlots 50		Change max crew slots of the ship

Ship Cargo limit increase
Note: Shielded cargo is a separate value and it will add to the amount you enter.  You can remove all your standard cargo containers and it won't effect anything but shielded seems to be a separate value so have a few of those if you plan on smuggling.

.setav carryweight 1000000

Increased space loot distance(Default 500)
SetGS fSpaceshipLootingDistanceDefault 5000

Lower incoming ship dmg due to the dramatic damage scaling(this applies to ship weapons as well as player weapons) - Default 0.650
player.setav PlayerIncomingShipDamageMult 0.081

Max Docking Distance(Default 500)
SetGS fSpaceshipMaxDockingDistance 5000

Increase ship inventory transfer distance(Default 250)
setgs fMaxShipTransferDistance 5000

Shield health(default 1)
.setav ShieldMaxHealth 10

Shield health multiplier(default 1)
.setav ShieldMaxHealthMult 10

Shield Regeneration rate multiplier(.1 = 10%)
.setav shieldregenrate 1

Shield max power - Not personaly tested
.setav spaceshipsheildpartmaxpower 10000

Grav jump settings - Not personaly tested
.setav spaceshipgravjumpthrust 100							
.setav spaceshipgravjumpmaxpower 							Max power for gravdrive
.setav spaceshipgravjumppowerbonus 
.setav spaceshipgravjumpmaxdistance 						Max jumpable distance
.setav spaceshipgravjumpflatfuelcost 						Cost per mile in fuel
.setav spaceshipgravjumpdistanceperfuel 					Distance per gallon
.setav spaceshipgravjumpinterplanetarydistancemultiplier 	

Ship engine settings - Not personaly tested
.setav spaceshipenginepartforce 40000				Engine Thrust
.setav spaceshipenginepartmaxpower 					Max engine power
.setav spaceshipenginepartpowerbonus				
.setav spaceshipenginepartmaxforwardspeed 1000		
.setav spaceshipenginepartmaxforwardvelocity		
.setav spaceshipenginepartmaxforwardacceleration	
.setav spaceshipforwardspeedmult
.setav spaceshipboostspeed

Thruster settings - Not personaly tested
.setav spaceshipthrusterpartforce 20000				Manuverability
.setav spaceshipthrusterpartstrafeforce				Force for moveing left-right-up-down if you have alt control mode and thruster parts from the structural tab.
.setav spaceshipthrusterpartmaxstrafespeed			Speed for moveing left-right-up-down
.setav spaceshipthrusterpartmaxpower 0				Default
.setav spaceshipthrusterpartpowerbonus 0			Default

Bigger ship sizes. Copy all lines. Note: any bigger could cause issues and cliping
setgs fSpaceshipLandableMaxSizeX 120			Default: 80
setgs fSpaceshipLandableMaxSizeY 120			Default: 80
setgs fSpaceshipLandableMaxSizeZ 120			Default: 80
setgs fSpaceshipLandableSmallSize 69			Default: 45
setgs fSpaceshipBuilderMaxSizeZ 60				Default: 40
setgs uSpaceshipBuilderMaxModules 195			Default: 130
setgs uSpaceshipBuilderModuleHardLimit 195		Default: 130

Ship builder settings
SetINISetting "fShipBuilderMouseZoomSpeedMultiplier:Spaceship" "4"
SetINISetting "fShipBuilderGamepadZoomSpeedMultiplier:Spaceship" "1.2"
SetINISetting "fShipBuilderZoomMinScale:Spaceship" "4"
SetINISetting "fShipBuilderMaxFloor:Spaceship" "50"
SetINISetting "fShipBuilderMinFloor:Spaceship" "-50"
SetINISetting "fShipBuilderMousePanSpeed:Spaceship" "2.25"
SetINISetting "fShipBuilderGamepadPanSpeed:Spaceship" "45"
SetINISetting "fShipBuilderMouseRotationSpeedMultiplier:Spaceship" "9"
SetINISetting "fShipBuilderFloorChangeDuration:Spaceship" "0.35"
SetINISetting "fShipBuilderEquipmentSnapDistance:Spaceship" "1.5"
SetINISetting "fShipBuilderSnapDistance:Spaceship" "1.75"
-------------------------------------------------------
#Outpost settings

Max outposts
player.getav 002a84f7           Check current amount of outposts left
player.setav 002a84f7 50        Change outpost max limit

Increases the border height for outposts to make it more visible(Default 10)
setgs fWorkshopVisibleBorderHeight 100

Allows the workshop freecam to leave the build area
SetINISetting "bConstrainWorkshopIsoCamToBuildArea:Camera" "0"

Increases the timeout when outside the outpost
setgs fPlayerOutsideBuildAreaTimerDuration 999999

Place outpost beacon anywere
player.placeatme 002C60E9

Max cargo links per outpost(Default 3)
set 190D57 to 16

Max crew stations per outpost(Default 3)
set 1b4bb2 to 24

Max mannequins per outpost(Default 6)
set 3f4aee to 16

Max robots per outpost(Default 3)
set 1d9f5e to 24

Max turrets per outpost(Default 6)
set f7c96 to 24

Memorial Easel(Default 1)
set 0007875A to 9999

Max Landing Pads(Default 1)
set 0022F4C9 to 10

Max Transfer Containers(Default 1)
set 002CE192 to 10

Disables the budget. Note: You will experience performance issues if you build too much in your outpost
SetINISetting "bBudgetEnabled:Workshop" "0"
SetINISetting "fBudgetBaseCost:Workshop" "0.0"
SetINISetting "fBudgetBaseline:Workshop" "99999.0"

Sets the max rotation speed for objects
SetINISetting "fItemRotationSpeedMax:Workshop" "5"

Production Multiplier(Set to 2x):
Lower Fractions = faster, Higher Fractions = slower
Example: 10 = 10 times slower, -10 = 10 times slower, 0.001 = 1000 times faster

Instructions:
While in game, open the command console and click on a production unit (make sure the value type shows   CONT " (ID)) and enter a command(On the unit's next cycle it will update the new production speed):

OutpostResourceProductionIntervalCommon(default=0.01)
set 0005ED87 to 0.005

OutpostResourceProductionIntervalUncommon(default=0.01)
set 0005EF3F to 0.005

OutpostResourceProductionIntervalRare(default=0.02)
set 0005EF3E to 0.01

OutpostResourceProductionIntervalExotic(default=0.03)
set 0005EF40 to 0.015

OutpostResourceProductionIntervalUnique(default=0.03)
set 0005EF41 to 0.015

OutpostResourceProductionIntervalMfgCommon(default=0.00)
set 0014E8C2 to 0.000

OutpostResourceProductionIntervalMfgUncommon(default=0.01)
set 0014E924 to 0.005

OutpostResourceProductionIntervalMfgRare(default=0.02)
set 0014EA72 to 0.01

OutpostResourceProductionIntervalMfgExotic(default=0.01)
set 0014EB51 to 0.005

OutpostResourceProductionIntervalMfgUnique(default=0.02)
set 0014EB75 to 0.01
-------------------------------------------------------
#Companion Affinity
Instruvtions: 
Open console ~
Click on companion to see their ref ID
Enter a command below

GetAV COM_AngerLevel       Get current anger level of companion
SetAV COM_AngerLevel 0     Set current anger level on companion
GetAV COM_Affinity         Get current affinity level of companion
SetAV COM_Affinity 100     Set current affinity level on companion
GetAV COM_AffinityLevel    Get current affinity level of companion
SetAV COM_AffinityLevel 1  Set current affinty level on companion

No more annoyed companions(Default 30). Companions wont get angry
﻿set 002A8033 to 0

Disliked events will no longer remove affinity
set 00005ACA to 0

Hated events will no longer remove affinity
set 00005ACB to 0
-------------------------------------------------------
#Get companions unstuck - Must be an active companion
Type "prid" line first, hit enter, then type "moveto player" and hit enter again.

Adoring Fan:
prid 001631C5
moveto player

Andreja:
prid 000059A9
moveto player

Barrett:
prid 00005788
moveto player

Gideon Aker:
prid 00015064
moveto player

Heller:
prid 0000563C
moveto player

Lin:
prid 00005639
moveto player

Sam Cole:
prid 0029D488
moveto player

Sarah Morgan:
prid 00005986
moveto player

Simeon Bankowski:
prid 00015063
moveto player

Vasco:
prid 000057BE
moveto player
-------------------------------------------------------
#Fast travel locations - For additional help for your own custom locations refer to my "Help command teleport tips.txt"

Move to currently selected quest
Movetoquesttarget

Lodge Marker
ft 000F93F0

MAST Marker
ft 0024C546

Neon City Marker
ft 0000DB23

Ship services:
player.moveto 00212b52  Akila City
player.moveto 005c81d   New Atlantis
player.moveto 0014a7ff  The Clinic
player.moveto 0016e1d6  Cydonia
player.moveto 001433e7  The Den
player.moveto 000d87a3  Eleos Retreat
player.moveto 0015cf3c  Gagarin
player.moveto 00146dcb  New Homestead
player.moveto 001b4bf2  Hope Town
player.moveto 000153a3  The Key(pirate base)
player.moveto 0015636e  Neon
player.moveto 0015d3c7  Paradiso

Exterior Cells
coc CityAkilaCityCoePlaza01				Akila City
coc NewAtlantisSpacePort				New Atlantis
coc ssStationTheClinic					The Clinic
coc CydoniaOrigin01						Cydonia
coc StationTheDen						The Den
coc SettleEleosRetreatExt				Eleos Retreat
coc GagarinExt01						Gagarin
coc SettleNewHomesteadMainBuilding01	New Homestead
coc	SettleHopeTown01					Hope Town
coc	StationTheKeyInterior				The Key(pirate base)
coc	NeonOrigin							Neon
coc	SettleParadiso						Paradiso
-------------------------------------------------------
#Crime settings
Pay Off Bounties for a specific Faction
player.paycrimegold 0 0 00010B30  Crimson Fleet
player.paycrimegold 0 0 000638E5  Freestar Collective
player.paycrimegold 0 0 00096529  Freestar Rangers
player.paycrimegold 0 0 002758C5  House Va'ruun
player.paycrimegold 0 0 002B209D  Red Mile
player.paycrimegold 0 0 0026FDEA  Neon/Ryujin Industries
player.paycrimegold 0 0 0022E53D  Trade Authority
player.paycrimegold 0 0 0005BD93  United Colonies
player.paycrimegold 0 0 0022892D  Xenofresh Corporation

Credits that an object is valued at in order for that object to be considered stolen(Default 20)
SetGS iCrimeStealDontCareValue 20

Number of days that an NPC or a faction will be hostile towards the player after committing a crime(Default 3)
SetGS iAINumberDaysToStayAngryforCrime 3
-------------------------------------------------------
#House prices - Note: When talking with people that sell these houses, dialogue will still say default values. Quicksave before buying house in case it doesnt work so you can revert back.
set 0009B0F3 to 1		Core Manor				Default 78000
set 0009B0F4 to 1		The Stretch Apartment	Default 45000
set 000A62BC to 1		Well Apartment			Default 30000
set 00370987 to 1		Sky Suite				Default 225000
set 0037098B to 1		Sleep Create			Default 6500
set 0032AF91 to 1		Daily Apartment Cost	Default 300
set 0032AF92 to 1		Weekly Apartment Cost	Default 2000
-------------------------------------------------------
#NeuroAmps(Defaults - Mk1 0.05(5%), Mk2 0.10(10%), Mk3 0.15(15%)) 1=100%
player.setav 00100546 1  Mk1 Intimidation 
player.setav 00100547 1  Mk2 Intimidation
player.setav 0010054E 1  Mk3 Intimidation

player.setav 00100549 1  Mk1 Diplomacy
player.setav 0010054A 1  Mk2 Diplomacy
player.setav 0010054B 1  Mk3 Diplomacy

player.setav 0010054C 1  Mk1 Instigation
player.setav 0010054D 1  Mk2 Instigation
player.setav 0010054E 1  Mk3 Instigation
-------------------------------------------------------
#Resources/Parts/Minerals/Crafting Material Items
Minerals
player.additem 00005DEC 1	Aldumite
player.additem 0000557D 1	Aluminum
player.additem 0000557B 1	Antimony
player.additem 000057D9 1	Beryllium
player.additem 000788D6 1	Caelumite
player.additem 00005575 1	Cobalt
player.additem 00005576 1	Copper
player.additem 00005569 1	Dysprosium
player.additem 000057E1 1	Europium
player.additem 00005579 1	Gold
player.additem 0004BA37 1	Indicite
player.additem 0000558A 1	Iridium
player.additem 0000556E 1	Iron
player.additem 00005568 1	Lead
player.additem 0000557F 1	Lithium
player.additem 00005580 1	Neodymium
player.additem 00005572 1	Nickel
player.additem 00005574 1	Palladium
player.additem 00005573 1	Platinum
player.additem 0000558C 1	Plutonium
player.additem 0000556A 1	Silver
player.additem 0000556D 1	Titanium
player.additem 00005589 1	Uranium
player.additem 0000558B 1	Vanadium
player.additem 00005DEF 1	Vytinium

All Resources
player.additem 00246B6A 1	Adaptive Frame
player.additem 000055B1 1	Adhesive
player.additem 00261295 1	Adhesive (Bone)
player.additem 00261294 1	Adhesive (Carapace)
player.additem 00260DBB 1	Adhesive (Flower)
player.additem 00261293 1	Adhesive (Gland)
player.additem 00261292 1	Adhesive (Hide)
player.additem 00260DBA 1	Adhesive (Leaf)
player.additem 00260DB9 1	Adhesive (Root)
player.additem 00260DB8 1	Adhesive (Sap)
player.additem 00260DB7 1	Adhesive (Seed)
player.additem 00260DB6 1	Adhesive (Stalk)
player.additem 00261291 1	Adhesive (Tissue)
player.additem 00261290 1	Adhesive (Vital Fluids)
player.additem 00005DEC 1	Aldumite
player.additem 00202F5A 1	Aldumite Drilling Rig
player.additem 00005570 1	Alkanes
player.additem 0000557D 1	Aluminum
player.additem 000055CD 1	Amino Acids
player.additem 0026128F 1	Amino Acids (Bone)
player.additem 0026128E 1	Amino Acids (Carapace)
player.additem 00260DB5 1	Amino Acids (Flower)
player.additem 0026128C 1	Amino Acids (Gland)
player.additem 0026128B 1	Amino Acids (Hide)
player.additem 00260DB4 1	Amino Acids (Leaf)
player.additem 00260DB3 1	Amino Acids (Root)
player.additem 00260DB2 1	Amino Acids (Sap)
player.additem 00260DB1 1	Amino Acids (Seed)
player.additem 00260DB0 1	Amino Acids (Stalk)
player.additem 0026128A 1	Amino Acids (Tissue)
player.additem 0026128D 1	Amino Acids (Vital Fluids)
player.additem 000055A9 1	Analgesic
player.additem 00261289 1	Analgesic (Bone)
player.additem 00261288 1	Analgesic (Carapace)
player.additem 00260DAF 1	Analgesic (Flower)
player.additem 00261286 1	Analgesic (Gland)
player.additem 00261285 1	Analgesic (Hide)
player.additem 00260DAE 1	Analgesic (Leaf)
player.additem 0260DAD  1	Analgesic (Root)
player.additem 00260DAC 1	Analgesic (Sap)
player.additem 00260D78 1	Analgesic (Seed)
player.additem 00260D77 1	Analgesic (Stalk)
player.additem 00261284 1	Analgesic (Tissue)
player.additem 00261287 1	Analgesic (Vital Fluids)
player.additem 000055AB 1	Antimicrobial
player.additem 002612C8 1	Antimicrobial (Bone)
player.additem 002612C7 1	Antimicrobial (Carapace)
player.additem 00260DFB 1	Antimicrobial (Flower)
player.additem 002612C9 1	Antimicrobial (Gland)
player.additem 0024F5C0 1	Antimicrobial (Hide)
player.additem 00260DF9 1	Antimicrobial (Leaf)
player.additem 00260DFA 1	Antimicrobial (Root)
player.additem 00260DF7 1	Antimicrobial (Sap)
player.additem 00250DF8 1	Antimicrobial (Seed)
player.additem 00260DFC 1	Antimicrobial (Stalk)
player.additem 0024F5BF 1	Antimicrobial (Tissue)
player.additem 0024F5C1 1	Antimicrobial (Vital Fluids)
player.additem 0000557B 1	Antimony
player.additem 00005588 1	Argon
player.additem 000055B8 1	Aromatic
player.additem 002612B3 1	Aromatic (Bone)
player.additem 002612AF 1	Aromatic (Carapace)
player.additem 00260DDC 1	Aromatic (Flower)
player.additem 002612B2 1	Aromatic (Gland)
player.additem 002612AE 1	Aromatic (Hide)
player.additem 00260DDB 1	Aromatic (Leaf)
player.additem 00260DDA 1	Aromatic (Root)
player.additem 00260DD9 1	Aromatic (Sap)
player.additem 00260DD8 1	Aromatic (Seed)
player.additem 002612B1 1	Aromatic (Tissue)
player.additem 002612B0 1	Aromatic (Vital Fluids)
player.additem 00246B7C 1	Austenitic Manifold
player.additem 00005585 1	Benzene
player.additem 000057D9 1	Beryllium
player.additem 000055B2 1	Biosuppressant
player.additem 00261274 1	Biosuppressant (Bone)
player.additem 00261273 1	Biosuppressant (Carapace)
player.additem 00260D67 1	Biosuppressant (Flower)
player.additem 00261271 1	Biosuppressant (Gland)
player.additem 00261270 1	Biosuppressant (Hide)
player.additem 00260D66 1	Biosuppressant (Leaf)
player.additem 00260D65 1	Biosuppressant (Root)
player.additem 00260D64 1	Biosuppressant (Sap)
player.additem 00260D63 1	Biosuppressant (Seed)
player.additem 00260D62 1	Biosuppressant (Stalk)
player.additem 0026126E 1	Biosuppressant (Tissue)
player.additem 00261272 1	Biosuppressant (Vital Fluids)
player.additem 00101273 1	Bulk Tranquilitea Breakfast
player.additem 000B2EE4 1	Bulk Tranquilitea Classic
player.additem 0010FA05 1	Bulk Tranquilitea Chamomile
player.additem 00097F0B 1	Bulk Tranquilitea Dynastic
player.additem 00097F0D 1	Bulk Tranquilitea Earl Grey
player.additem 00120D33 1	Bulk Tranquilitea Lemon
player.additem 00101274 1	Bulk Tranquilitea Lotus
player.additem 00097F0C 1	Bulk Tranquilitea Sleepy
player.additem 000F2C84 1	Bulk Tranquilitea Sunray
player.additem 000057DF 1	Caesium
player.additem 00005586 1	Carboxylic Acids
player.additem 0013BD9C 1	Chasmbass Oil
player.additem 000557C  1	Chlorine
player.additem 0000557E 1	Chlorosilanes
player.additem 0000557D 1	Cobalt
player.additem 0025B0FB 1	Coffee Bag
player.additem 00246B64 1	Comm Relay
player.additem 00246B7B 1	Control Rod
player.additem 00005576 1	Copper
player.additem 000055A8 1	Cosmetic
player.additem 002612AD 1	Cosmetic (Bone)
player.additem 002612AC 1	Cosmetic (Carapace)
player.additem 00260DD7 1	Cosmetic (Flower)
player.additem 002612AA 1	Cosmetic (Gland)
player.additem 002612A9 1	Cosmetic (Hide)
player.additem 00260DD6 1	Cosmetic (Leaf)
player.additem 00260DD5 1	Cosmetic (Root)
player.additem 00260DD4 1	Cosmetic (Sap)
player.additem 00260DD3 1	Cosmetic (Seed)
player.additem 00260DD2 1	Cosmetic (Stalk)
player.additem 002612A8 1	Cosmetic (Tissue)
player.additem 002612AB 1	Cosmetic (Vital Fluids)
player.additem 0020A02F 1	Drilling Rig
player.additem 00005569 1	Dysprosium
player.additem 000057E1 1	Europium
player.additem 000055AF 1	Fiber
player.additem 002612C2 1	Fiber (Bone)
player.additem 002612C3 1	Fiber (Carapace)
player.additem 0024F5C4 1	Fiber (Hide)
player.additem 00260DEE 1	Fiber (Leaf)
player.additem 00260DF0 1	Fiber (Root)
player.additem 0024F5C3 1	Fiber (Tissue)
player.additem 00005577 1	Fluorine
player.additem 00005579 1	Gold
player.additem 0029F405 1	Hallucinogen
player.additem 00261283 1	Hallucinogen (Bone)
player.additem 00261282 1	Hallucinogen (Carapace)
player.additem 00260D76 1	Hallucinogen (Flower)
player.additem 00261280 1	Hallucinogen (Gland)
player.additem 0026127F 1	Hallucinogen (Hide)
player.additem 00260D75 1	Hallucinogen (Leaf)
player.additem 00260D74 1	Hallucinogen (Root)
player.additem 00260D73 1	Hallucinogen (Sap)
player.additem 00260D72 1	Hallucinogen (Seed)
player.additem 00260D71 1	Hallucinogen (Stalk)
player.additem 0026127E 1	Hallucinogen (Tissue)
player.additem 00261281 1	Hallucinogen (Vital Fluids)
player.additem 0000558E 1	Helium-3
player.additem 0029F40D 1	Hypercatalyst
player.additem 0026126F 1	Hypercatalyst (Bone)
player.additem 0026126D 1	Hypercatalyst (Carapace)
player.additem 00260D61 1	Hypercatalyst (Flower)
player.additem 0026126B 1	Hypercatalyst (Gland)
player.additem 0026126A 1	Hypercatalyst (Hide)
player.additem 00260D60 1	Hypercatalyst (Leaf)
player.additem 00260D5F 1	Hypercatalyst (Root)
player.additem 00260D30 1	Hypercatalyst (Sap)
player.additem 00260D25 1	Hypercatalyst (Seed)
player.additem 00260D0C 1	Hypercatalyst (Stalk)
player.additem 00261269 1	Hypercatalyst (Tissue)
player.additem 0026126C 1	Hypercatalyst (Vital Fluids)
player.additem 000055B3 1	Immunostimulant
player.additem 0004BA37 1	Indicite
player.additem 00203EB4 1	Indicite Wafer
player.additem 0000557A 1	Ionic Liquids
player.additem 0000558A 1	Iridium
player.additem 0000556E 1	Iron
player.additem 00246B77 1	Isocentered Magnet
player.additem 00246B76 1	Isotopic Coolant
player.additem 00005568 1	Lead
player.additem 0000557F 1	Lithium
player.additem 000055BA 1	Lubricant
player.additem 00260D0B 1	Lubricant (Flower)
player.additem 00261267 1	Lubricant (Gland)
player.additem 00261266 1	Lubricant (Hide)
player.additem 00260D0A 1	Lubricant (Leaf)
player.additem 00260CE2 1	Lubricant (Root)
player.additem 00260CB6 1	Lubricant (Sap)
player.additem 00260C79 1	Lubricant (Seed)
player.additem 00260C74 1	Lubricant (Stalk)
player.additem 00261265 1	Lubricant (Tissue)
player.additem 00261268 1	Lubricant (Vital Fluids)
player.additem 0000559E 1	Luxury Textile
player.additem 00246B70 1	Mag Pressure Tank
player.additem 000055B0 1	Membrane
player.additem 002612A7 1	Membrane (Carapace)
player.additem 00260DD1 1	Membrane (Flower)
player.additem 002612A6 1	Membrane (Gland)
player.additem 002612A5 1	Membrane (Hide)
player.additem 00260DD0 1	Membrane (Leaf)
player.additem 00260DCF 1	Membrane (Root)
player.additem 00260DCE 1	Membrane (Stalk)
player.additem 002612A4 1	Membrane (Tissue)
player.additem 0027C4A1 1	Mercury
player.additem 0029F3FC 1	Metabolic Agent
player.additem 002612C1 1	Metabolic Agent (Bone)
player.additem 002612C0 1	Metabolic Agent (Carapace)
player.additem 00260DEC 1	Metabolic Agent (Flower)
player.additem 002612BF 1	Metabolic Agent (Gland)
player.additem 002612BE 1	Metabolic Agent (Hide)
player.additem 00260DEB 1	Metabolic Agent (Leaf)
player.additem 00260DEA 1	Metabolic Agent (Root)
player.additem 00260DE9 1	Metabolic Agent (Sap)
player.additem 00260DE8 1	Metabolic Agent (Seed)
player.additem 00260DED 1	Metabolic Agent (Stalk)
player.additem 0029F3F8 1	Metabolic Agent (Tissue)
player.additem 0029F3F9 1	Metabolic Agent (Vital Fluids)
player.additem 00246B5F 1	Microsecond Regulator
player.additem 00246B75 1	Molecular Sieve
player.additem 00246B74 1	Monopropellant
player.additem 00005580 1	Neodymium
player.additem 00005587 1	Neon
player.additem 00005572 1	Nickel
player.additem 00246B79 1	Nuclear Fuel Rod
player.additem 000777FD 1	Nutrient
player.additem 002612C6 1	Nutrient (Bone)
player.additem 002612C4 1	Nutrient (Carapace)
player.additem 00260DF6 1	Nutrient (Flower)
player.additem 002612C5 1	Nutrient (Gland)
player.additem 0029F3F6 1	Nutrient (Hide)
player.additem 00260DF5 1	Nutrient (Leaf)
player.additem 00260DF4 1	Nutrient (Root)
player.additem 00260DF3 1	Nutrient (Sap)
player.additem 00260DF2 1	Nutrient (Seed)
player.additem 00260DF1 1	Nutrient (Stalk)
player.additem 0024F5C2 1	Nutrient (Tissue)
player.additem 0029F3F7 1	Nutrient (Vital Fluids)
player.additem 002612BD 1	Ornamental (Bone)
player.additem 002612BC 1	Ornamental (Carapace)
player.additem 00260DE7 1	Ornamental (Flower)
player.additem 002612B9 1	Ornamental (Gland)
player.additem 002612BA 1	Ornamental (Hide)
player.additem 00260DE6 1	Ornamental (Leaf)
player.additem 00260DE5 1	Ornamental (Root)
player.additem 00260DE4 1	Ornamental (Sap)
player.additem 00260DE3 1	Ornamental (Seed)
player.additem 00260DE2 1	Ornamental (Stalk)
player.additem 002612B8 1	Ornamental (Tissue)
player.additem 002612BB 1	Ornamental (Vital Fluids)
player.additem 000055A7 1	Ornamental Material
player.additem 00005574 1	Palladium
player.additem 00246B73 1	Paramagnon Conductor
player.additem 0029F400 1	Pigment
player.additem 002612A3 1	Pigment (Bone)
player.additem 002612A2 1	Pigment (Carapace)
player.additem 00260DCD 1	Pigment (Flower)
player.additem 002612A0 1	Pigment (Gland)
player.additem 0026129F 1	Pigment (Hide)
player.additem 00260DCC 1	Pigment (Leaf)
player.additem 00260DCB 1	Pigment (Root)
player.additem 00260DCA 1	Pigment (Sap)
player.additem 00260DC9 1	Pigment (Seed)
player.additem 00260DC8 1	Pigment (Stalk)
player.additem 0026129E 1	Pigment (Tissue)
player.additem 002612A1 1	Pigment (Vital Fluids)
player.additem 00005573 1	Platinum
player.additem 000055A6 1	Polymer
player.additem 0026125E 1	Polymer (Bone)
player.additem 0026125D 1	Polymer (Carapace)
player.additem 00260C3B 1	Polymer (Flower)
player.additem 0026125B 1	Polymer (Gland)
player.additem 0026125A 1	Polymer (Hide)
player.additem 00260C38 1	Polymer (Leaf)
player.additem 00260C36 1	Polymer (Root)
player.additem 00260C2D 1	Polymer (Sap)
player.additem 00260C1C 1	Polymer (Seed)
player.additem 00260BFF 1	Polymer (Stalk)
player.additem 00261259 1	Polymer (Tissue)
player.additem 0026125C 1	Polymer (Vital Fluids)
player.additem 00246B72 1	Polytextile
player.additem 00246B71 1	Positron Battery
player.additem 00246B5C 1	Power Circuit
player.additem 00122EB8 1	Quark-Degenerate Tissues
player.additem 00246B6F 1	Reactive Gauge
player.additem 000028DF 1	Rothicite
player.additem 00203EB2 1	Rothicite Magnet
player.additem 000055CC 1	Sealant
player.additem 0026129D 1	Sealant (Carapace)
player.additem 00260DC7 1	Sealant (Flower)
player.additem 0026129C 1	Sealant (Gland)
player.additem 002AB397 1	Sealant (Hide)
player.additem 00260DC6 1	Sealant (Leaf)
player.additem 00260DC5 1	Sealant (Root)
player.additem 00260DC4 1	Sealant (Sap)
player.additem 00260DC3 1	Sealant (Seed)
player.additem 00260DC2 1	Sealant (Stalk)
player.additem 002AB399 1	Sealant (Tissue)
player.additem 002AB398 1	Sealant (Vital Fluids)
player.additem 000055AD 1	Sedative
player.additem 0026127D 1	Sedative (Bone)
player.additem 0026127C 1	Sedative (Carapace)
player.additem 00260D70 1	Sedative (Flower)
player.additem 0026127A 1	Sedative (Gland)
player.additem 00260D6F 1	Sedative (Leaf)
player.additem 00260D6E 1	Sedative (Root)
player.additem 00260D6D 1	Sedative (Sap)
player.additem 00260D6C 1	Sedative (Seed)
player.additem 00260D6B 1	Sedative (Stalk)
player.additem 00261278 1	Sedative (Tissue)
player.additem 0026127B 1	Sedative (Vital Fluids)
player.additem 00246B6D 1	Semimetal Wafer
player.additem 0000556A 1	Silver
player.additem 000055CE 1	Solvent
player.additem 00260BF7 1	Solvent (Flower)
player.additem 00261257 1	Solvent (Gland)
player.additem 00260BF6 1	Solvent (Leaf)
player.additem 00260BF5 1	Solvent (Root)
player.additem 00260BF4 1	Solvent (Sap)
player.additem 00260BF3 1	Solvent (Seed)
player.additem 00260BF2 1	Solvent (Stalk)
player.additem 00261256 1	Solvent (Tissue)
player.additem 00261258 1	Solvent (Vital Fluids)
player.additem 000055AC 1	Spice
player.additem 0026129B 1	Spice (Bone)
player.additem 0026129A 1	Spice (Carapace)
player.additem 00260DC1 1	Spice (Flower)
player.additem 00261298 1	Spice (Gland)
player.additem 00261297 1	Spice (Hide)
player.additem 00260DC0 1	Spice (Leaf)
player.additem 00260DBF 1	Spice (Root)
player.additem 00260DBE 1	Spice (Sap)
player.additem 00260DBD 1	Spice (Seed)
player.additem 00260DBC 1	Spice (Stalk)
player.additem 00261296 1	Spice (Tissue)
player.additem 00261299 1	Spice (Vital Fluids)
player.additem 00246B6C 1	Sterile Nanotubes
player.additem 000055AE 1	Stimulant
player.additem 00261264 1	Stimulant (Bone)
player.additem 00261263 1	Stimulant (Carapace)
player.additem 00260C66 1	Stimulant (Flower)
player.additem 00261260 1	Stimulant (Gland)
player.additem 00261261 1	Stimulant (Hide)
player.additem 00260C66 1	Stimulant (Leaf)
player.additem 00260C5C 1	Stimulant (Root)
player.additem 00260C3F 1	Stimulant (Sap)
player.additem 00260C3E 1	Stimulant (Seed)
player.additem 00260C3C 1	Stimulant (Stalk)
player.additem 0026125F 1	Stimulant (Tissue)
player.additem 00261262 1	Stimulant (Vital Fluids)
player.additem 000055B9 1	Structural Material
player.additem 00202782 1	Substrate Molecule Sieve
player.additem 00246B69 1	Supercooled Magnet
player.additem 0000556F 1	Tantalum
player.additem 00005DED 1	Tasine
player.additem 00203EAF 1	Tasine Superconductor
player.additem 00246B68 1	Tau Grade Rheostat
player.additem 00005578 1	Tetrafluorides
player.additem 0000556D 1	Titanium
player.additem 000055CB 1	Toxin
player.additem 002612B7 1	Toxin (Bone)
player.additem 002612B6 1	Toxin (Carapace)
player.additem 00260DE1 1	Toxin (Flower)
player.additem 002612B5 1	Toxin (Gland)
player.additem 002612B4 1	Toxin (Hide)
player.additem 00260DE0 1	Toxin (Leaf)
player.additem 00260DDF 1	Toxin (Root)
player.additem 00260DDE 1	Toxin (Sap)
player.additem 00260DDD 1	Toxin (Seed)
player.additem 0024F5C5 1	Toxin (Tissue)
player.additem 0024F5C6 1	Toxin (Vital Fluids)
player.additem 0028E7AB 1	Tranquilitea Breakfast Pack
player.additem 0028E7AC 1	Tranquilitea Classic Pack
player.additem 00188248 1	Tranquilitea Chamomile Pack
player.additem 001557FD 1	Tranquilitea Dynastic Pack
player.additem 001557F5 1	Tranquilitea Earl Gray Pack
player.additem 001346D9 1	Tranquilitea Lemon Pack
player.additem 00110F93 1	Tranquilitea Lotus Pack
player.additem 00094733 1	Tranquilitea Sleepy Pack
player.additem 00094732 1	Tranquilitea Sunray Pack
player.additem 000556B  1	Tungsten
player.additem 00005589 1	Uranium
player.additem 0000558B 1	Vanadium
player.additem 00005DEE 1	Veryl
player.additem 00203EB0 1	Veryl-Treated Manifold
player.additem 00203EBD 1	Veryl Explosive
player.additem 00005DEF 1	Vytinium
player.additem 00203EB3 1	Vytinium Fuel Rod
player.additem 00005591 1	Water
player.additem 000057DD 1	Xenon
player.additem 00005571 1	Ytterbium
player.additem 00246B65 1	Zero Wire
player.additem 00246B66 1	Zero-G Gimbal 
-------------------------------------------------------
#Food/Drinks/Aid
player.additem 0029A851 1	Addichrone
player.additem 000C1F57 1	Alien Genetic Material
player.additem 00299592 1	AMP
player.additem 0003D3AD 1	Anchored Immobilizers
player.additem 002F4436 1	Antibiotics
player.additem 0003D3A9 1	Antibiotic Cocktail
player.additem 0003D3AF 1	Antibiotic Injector
player.additem 0003D3AE 1	Antibiotic Paste
player.additem 00299590 1	Antibiotic Paste
player.additem 002543B9 1	Baguette
player.additem 002F4459 1	Bandages
player.additem 002A5024 1	Battlestim
player.additem 00249C2A 1	Blend
player.additem 0003D3AC 1	Boosted Injector
player.additem 0029959F 1	Boudicca
player.additem 0029A849 1	Boudicca
player.additem 002C7211 1	Bourbon
player.additem 002C7C0A 1	Butter
player.additem 002C722D 1	Can-uck! Bacon
player.additem 00249C49 1	Can-uck! Double Double
player.additem 00249C4A 1	Can-uck! Edmontonian
player.additem 00249C4C 1	Can-uck! Ham Boys
player.additem 00249C4D 1	Can-uck! Haligonian
player.additem 00249C48 1	Can-uck! Maple Cola
player.additem 002C720D 1	Can-uck! Pilsner
player.additem 002C7231 1	Can-uck! Poutine
player.additem 00249C4B 1	Can-uck! Shepherd's Pie
player.additem 002C7232 1	Can-uck! Tourtiere
player.additem 00092B98 1	Carrot
player.additem 00092B99 1	Celery
player.additem 002C7236 1	Cheddar Snack Crackers
player.additem 001FC9C1 1	Cheese
player.additem 002C7202 1	Chandra Cabernet Sauvignon
player.additem 002C7204 1	Chandra Chardonnay
player.additem 002C7203 1	Chandra Malbec
player.additem 002C7208 1	Chandra Merlot
player.additem 002C7206 1	Chandra Pinot Noir
player.additem 002C7209 1	Chandra Port
player.additem 002C7207 1	Chandra Sauvignon Blanc
player.additem 002C7205 1	Chandra Riesling
player.additem 00206770 1	Chunks Apple
player.additem 00206771 1	Chunks Apple - Packaged
player.additem 00206763 1	Chunks Beef
player.additem 0020676F 1	Chunks Beef - Packaged
player.additem 0020676D 1	Chunks Cake
player.additem 0020676E 1	Chunks Cake - Packaged
player.additem 0020676B 1	Chunks Cheesesteak
player.additem 0020676C 1	Chunks Cheesesteak - Packaged
player.additem 00206764 1	Chunks Chicken
player.additem 0020676A 1	Chunks Chick - Packaged
player.additem 00206769 1	Chunks Choco
player.additem 00206769 1	Chunks Choco - Packaged
player.additem 00206767 1	Chunks Cola - Packaged
player.additem 00206765 1	Chunks Egg
player.additem 001E29A8 1	Chunks Egg - Packaged
player.additem 0020675F 1	Chunks Pie
player.additem 00206760 1	Chunks Pie - Packaged
player.additem 00206761 1	Chunks Potato
player.additem 00206762 1	Chunks Potato - Packaged
player.additem 0020675D 1	Chunks Wine
player.additem 0020675E 1	Chunks Wine - Packaged
player.additem 00249C1A 1	Codos Crater
player.additem 0029A85E 1	CQB-X
player.additem 00139E45 1	Dark Lager
player.additem 002C72117 1	Drink Pack: Beer
player.additem 002C7216 1	Drink Pack: Milk
player.additem 002C721A 1	Drink Pack: Orange Juice
player.additem 002C7218 1	Drink Pack: Water
player.additem 002C7214 1	Drink Pack: White Wine
player.additem 002C7219 1	Drink Pack: Whiskey
player.additem 002C7215 1	Drink Pack: Red Wine
player.additem 0029B00E 1	Drink Pack: Vodka
player.additem 002A9DE8 1	Emergency Kit
player.additem 001FF69C 1	Erdebrau Dark Can
player.additem 001FF69E 1	Erdebrau Lager Can
player.additem 001FF6A0 1	Erdebrau Light Can
player.additem 001FF69A 1	Erdebrau Pils Can
player.additem 00249C20 1	Fried Pickles
player.additem 002995A1 1	Frostwolf
player.additem 002C5885 1	Frostwolf
player.additem 000304CE 1	FullFood Spiced Worms
player.additem 002C7235 1	Granola Mix
player.additem 00092B9A 1	Grapes
player.additem 0003D3AB 1	Heal Gel
player.additem 002F445C 1	Heal Paste
player.additem 0029CAD9 1	Heart Plus
player.additem 002C5883 1	Hippolyta
player.additem 002F445B 1	Immobilizer
player.additem 0029A85C 1	Infantry Alpha
player.additem 0003D3B0 1	Infused Bandages
player.additem 002F445A 1	Injector
player.additem 00143CB1 1	Junk Flush
player.additem 002C7213 1	Kefir
player.additem 0004B1D8 1	Lemon
player.additem 00092B9B 1	Lettuce
player.additem 0004B1D7 1	Lime
player.additem 002C7238 1	Marshmallow Treat Cereal
player.additem 00191214 1	Meal Kit
player.additem 002C7221 1	Meal Pack - Cereal
player.additem 002C721C 1	Meal Pack - Chicken
player.additem 002C7222 1	Meal Pack - Eggs
player.additem 002C721F 1	Meal Pack - Ramen
player.additem 002C721D 1	Meal Pack - Shrimp
player.additem 002C7220 1	Meal Pack - Sushi
player.additem 002C721E 1	Meal Pack - Tofu
player.additem 0000ABF9 1	Med Pack
player.additem 0019121F 1	Milk
player.additem 001EE5C7 1	Miso Soup Multipack
player.additem 001EDDDF 1	Mochi
player.additem 001EDDDE 1	Mochi Minibite
player.additem 001EDDE0 1	Mochi Multipack
player.additem 0029958F 1	Neurajack
player.additem 00003A22 1	Orange
player.additem 00139E44 1	Pale Ale
player.additem 002995A3 1	Panacea
player.additem 002C5881 1	Paramour
player.additem 00249C21 1	Patty Melt
player.additem 00003A23 1	Peach
player.additem 00003A21 1	Pear
player.additem 0029A84F 1	Penicillin X
player.additem 001944E4 1	Pepper Steak Sandwich
player.additem 00003A26 1	Potato
player.additem 002C7237 1	Raisin Bran Cereal
player.additem 001EE441 1	Ramen
player.additem 001EE442 1	Ramen Minibite
player.additem 001EE440 1	Ramen Multipack
player.additem 0029A855 1	Reconstim
player.additem 00139E43 1	Red Ale
player.additem 0001BBAB 1	Red Harvest Amber Ale
player.additem 0003614B 1	Red Harvest Double Malt Whiskey
player.additem 002C7241 1	Red Harvest Lentils
player.additem 0001BBAC 1	Red Harvest Milk Stout
player.additem 002C723F 1	Red Harvest Naan
player.additem 0001BBAA 1	Red Harvest Pale Ale
player.additem 0029B013 1	Red Harvest Rice
player.additem 002C723C 1	Red Harvest Rye
player.additem 0003614C 1	Red Harvest Single Malt Whiskey
player.additem 002C7240 1	Red Harvest Spaghetti
player.additem 002C723D 1	Red Harvest Wheat
player.additem 002C723E 1	Red Harvest White
player.additem 002C587F 1	Red Trench
player.additem 0003D3B1 1	Repairing Immobilizer
player.additem 002543B7 1	Sandwich
player.additem 002C724D 1	Seaweed Minibite
player.additem 0030283B 1	Seaweed Snacks Multipack
player.additem 0003FB19 1	Ship Parts
player.additem 0029A860 1	Smoked Salmon Fillet
player.additem 002C7223 1	Snack Pack - Apple Bites
player.additem 002C7225 1	Snack Pack - Choco Bites
player.additem 002C7226 1	Snack Pack - Gummi Bugs
player.additem 002C7224 1	Snack Pack - Protein Bar
player.additem 0029A850 1	Snake Oil
player.additem 001EDDE5 1	Soba
player.additem 001EDDE4 1	Soba Minibite
player.additem 00249C1B 1	Solomon's Reserve
player.additem 000304CC 1	Sparkling Water
player.additem 001DFCB4 1	Sparkling Wine
player.additem 002A9DE7 1	Squall
player.additem 00243FA5 1	Supernova
player.additem 001DFCAB 1	Sushi Rolls Minibite
player.additem 001DFCAC 1	Sushi Rolls Multiplack
player.additem 002C5880 1	Synapse Alpha
player.additem 002C7242 1	Synthameat Chicken
player.additem 002C7246 1	Synthameat Ham
player.additem 002C7243 1	Synthameat Hamburger
player.additem 000304D0 1	Synthameat Multi
player.additem 002C7244 1	Synthameat Steak
player.additem 0029A861 1	Synthameat Turkey
player.additem 002C7245 1	Synthameat Veal
player.additem 00249C15 1	Ta'ameya Pita
player.additem 00249C4E 1	TerraBew Cappuccino
player.additem 00249C50 1	TerraBew Classic
player.additem 003E3407 1	TerraBew Cortado
player.additem 0029A894 1	TerraBew Espresso
player.additem 00249C4F 1	TerraBew Latte
player.additem 003E3408 1	TerraBew Macchiato
player.additem 001DFCAE 1	Toast
player.additem 00092B96 1	Tomato
player.additem 0010FA09 1	Tranquilitea Earl Gray
player.additem 0029A847 1	Trauma Pack
player.additem 0029A893 1	UC BattleMeal
player.additem 0030283E 1	UC BattleMeal Multipack
player.additem 001EDF0F 1	Udon
player.additem 001EDF10 1	Udon Minibite
player.additem 001EDF10 1	Udon Multipack
player.additem 00249C1F 1	Veggie Grinder
player.additem 002C7C09 1	Yogurt
player.additem 0014098A 1	Yuko's Coffee
player.additem 0003D3AA 1	Zipper Bandages

Cooking Station Food and Drink IDs
player.additem 0029B046 1	Alien Broth
player.additem 0029B047 1	Alien Energy Drink
player.additem 002C7C0C 1	Alien Jerky
player.additem 0029B061 1	Alien Kebabs
player.additem 0029B04F 1	Alien Liquor
player.additem 0029B063 1	Alien Pie
player.additem 0029B062 1	Alien Sandwich
player.additem 0029B065 1	Alien Scramble
player.additem 0029B066 1	Alien Stew
player.additem 0029B064 1	Alien Stir Fry
player.additem 0029B052 1	Alien Tea
player.additem 0029B048 1	Alien Tonic
player.additem 0029B054 1	Barbacoa Wrap
player.additem 0029B050 1	Boba Alien Tea
player.additem 002C71F8 1	Boom Pop! Black Licorice
player.additem 0029A863 1	Boom Pop! Cherry
player.additem 002C71F5 1	Boom Pop! Cola
player.additem 0029B040 1	Boom Pop! Dynamite
player.additem 002C71F5 1	Boom Pop! Orange
player.additem 003038FE 1	Boom Pop! Reactor
player.additem 002C71F7 1	Boom Pop! Rhubarb
player.additem 002C71F4 1	Boom Pop! Root Beer
player.additem 0029B04B 1	Bullet Coffee
player.additem 0029B03E 1	Chai Latte
player.additem 002C7C0D 1	Chapaguri
player.additem 0029B05C 1	Chicken Marsala
player.additem 0029B05A 1	Chicken Tikka
player.additem 0029B04E 1	Colonel's Choice
player.additem 0029B05E 1	Creature Jam
player.additem 0029B060 1	Crispy Alien Nuggets
player.additem 0029B056 1	Dal Makhai
player.additem 0029B042 1	Disastrous Shipwreck
player.additem 0029B053 1	Distilled Water
player.additem 0029B059 1	Doro Wat
player.additem 0029B03F 1	Fully-Loaded Bloody Mary
player.additem 00122E94 1	Galaxy Lo Mein
player.additem 0029B05D 1	Grilled Cheese Sandwich
player.additem 002C722B 1	Ham and Cheese Sandwich
player.additem 002383E9 1	Latkes
player.additem 0029B04D 1	Lumberjack Julep
player.additem 0029B05B 1	Meatloaf
player.additem 00122E96 1	Nebula Wat
player.additem 0029B057 1	Pappardelle Bolognese
player.additem 0029B055 1	Reuben
player.additem 0029B058 1	Spaghetti Carbonara
player.additem 00122E95 1	Star Cluster Marsala
player.additem 00122E98 1	Stellar Kebabs
player.additem 0029B04C 1	Sunray Tonic
player.additem 0029B041 1	Very Heavy Water
player.additem 0029B05F 1	Xenowurst
-------------------------------------------------------
#Powers
addspell = Give power
addperk = Rank up the power(Max is 10)

player.addspell 2BACBA Anti-Gravity Field
player.addperk 25E19C
player.addspell 2C5390 Create Vacuum
player.addperk 25E19B
player.addspell 2C538D Creators' Peace
player.addperk 25E19A
player.addspell 2BACB5 Earthbound
player.addperk 25E199
player.addspell 2C5391 Elemental Pull
player.addperk 25E198
player.addspell 2C538F Alien Reanimation
player.addperk 25E19D
player.addspell 2BACB4 Eternal Harvest
player.addperk 25E197
player.addspell 2C538C Grav Dash
player.addperk 25E196
player.addspell 2BACB7 Gravity Wave
player.addperk 25E195
player.addspell 2C5A62 Gravity Well
player.addperk 25E193
player.addspell 2C5399 Inner Demon
player.addperk 25E192
player.addspell 2C538B Life Forced
player.addperk 25E191
player.addspell 2C5A4E Moon Form
player.addperk 25E190
player.addspell 2C5A67 Parallel Self
player.addperk 25E18E
player.addspell 2C5A66 Particle Beam
player.addperk 25E18D
player.addspell 2C5389 Personal Atmosphere
player.addperk 25E18C
player.addspell 2C5A63 Phased Time
player.addperk 25E18B
player.addspell 2C538A Precognition
player.addperk 25E18F
player.addspell 2BACB6 Reactive Shield
player.addperk 25E19E
player.addspell 2C5A54 Sense Star Stuff
player.addperk 25E18A
player.addspell 2C5A59 Solar Flare
player.addperk 25E189
player.addspell 2C5388 Sunless Space
player.addperk 25E188
player.addspell 2C5387 Supernova
player.addperk 25E187
player.addspell 2C5A53 Void Form
player.addperk 25E186
-------------------------------------------------------
#Perks/Backgrounds
player.removeperk [perk id] - to remove any perk
Note: Enter the code multiple times to rank the perk up

Physical Skills
player.addperk 002C59DF 	Boxing
player.addperk 002CE2DD 	Fitness
player.addperk 002CFCB2 	Stealth
player.addperk 002C59D9 	Weight Lifting
player.addperk 002CE2E1 	Wellness
player.addperk 002C59E2 	Energy Weapon Dissipation
player.addperk 0028AE17 	Environmental Conditioning
player.addperk 0028AE29 	Gymnastics
player.addperk 002CFCAD 	Nutrition
player.addperk 002CFCAE 	Pain Tolerance
player.addperk 0028AE14 	Cellular Regeneration
player.addperk 002CE2A0 	Decontamination
player.addperk 002C5554 	Martial Arts
player.addperk 002C555E 	Concealment
player.addperk 002C53B4 	Neurostrikes
player.addperk 0028AE13 	Rejuvenation

Social Skills
player.addperk 002C5A8E 	Commerce
player.addperk 002C5A94 	Gastronomy
player.addperk 0022EC82 	Persuasion
player.addperk 0028B853 	Scavenging
player.addperk 002C555B 	Theft
player.addperk 002CFCAF 	Deception
player.addperk 002C59E1 	Diplomacy
player.addperk 002C59DE 	Intimidation
player.addperk 002C53AE 	Isolation
player.addperk 002C555F 	Negotiation
player.addperk 002C555D 	Instigation
player.addperk 002C890D 	Leadership
player.addperk 0023826F 	Outpost Management
player.addperk 002C5555 	Manipulation
player.addperk 002C53B3 	Ship Command
player.addperk 002C53B0 	Xenosociology

Combat Skills
player.addperk 002CFCAB 	Ballistics
player.addperk 002CFCB0 	Dueling
player.addperk 002C59DD 	Lasers
player.addperk 002080FF 	Pistol Certification
player.addperk 0027DF97 	Shotgun Certification
player.addperk 002C5556 	Demolitions
player.addperk 00147E38 	Heavy Weapons Certification
player.addperk 0027DF96 	Incapacitation
player.addperk 0027BAFD 	Particle Beams
player.addperk 002CE2E0 	Rifle Certification
player.addperk 002C890B 	Marksmanship
player.addperk 002C555A 	Rapid Reloading
player.addperk 002C53B1 	Sniper Certification
player.addperk 002C59DA 	Targeting
player.addperk 0027DF94 	Armor Penetration
player.addperk 0027CBBA 	Crippling
player.addperk 002C53AF 	Sharpshooting

Science Skills
player.addperk 002C5560 	Astrodynamics
player.addperk 002CE29F 	Geology
player.addperk 002CE2DF 	Medicine
player.addperk 002C555C 	Research Methods
player.addperk 0027CBC1 	Surveying
player.addperk 002C5557 	Botany
player.addperk 002CFCB1 	Scanning
player.addperk 0027CBC3 	Spacesuit Design
player.addperk 002C890C 	Weapon Engineering
player.addperk 002C5552 	Zoology
player.addperk 0027CBBB 	Astrophysics
player.addperk 002CE2C0 	Chemistry
player.addperk 002C59E0 	Outpost Engineering
player.addperk 002C2C5A 	Aneutronic Fusion
player.addperk 0027CBC2 	Planetary Habitation
player.addperk 0004CE2D 	Special Projects

Tech Skills
player.addperk 002CE2C2 	Ballistic Weapon Systems
player.addperk 00146C2C 	Boost Pack Training
player.addperk 002CFCAC 	Piloting
player.addperk 002CE2E2 	Security
player.addperk 002C5559 	Targeting Control Systems
player.addperk 002C59DB 	Energy Weapon Systems
player.addperk 002CE2DE 	Engine Systems
player.addperk 00143B6B 	Payloads
player.addperk 002C2C59 	Shield Systems
player.addperk 002C5558 	Missile Weapon Systems
player.addperk 002C2C5B 	Particle Beam Weapon Systems
player.addperk 002C5553 	Robotics
player.addperk 002C59DC 	Starship Design
player.addperk 002AC953 	Starship Engineering
player.addperk 0027B9ED 	Automated Weapon Systems
player.addperk 0008C3EE 	Boost Assault Training
player.addperk 002C53B2 	EM Weapon Systems

Traits
player.addperk 00227FDA 	Alien DNA
player.addperk 00227FDF 	Dream Home
player.addperk 00227FD6 	Empath
player.addperk 00227FD7 	Extrovert
player.addperk 00227FD5 	Freestar Collective Settler
player.addperk 00227FD9 	Hero Worshipped
player.addperk 00227FD8 	Introvert
player.addperk 00227FDE 	Kid Stuff
player.addperk 00227FD3 	Neon Street Rat
player.addperk 00227FD2 	Raised Enlightened
player.addperk 00227FD1 	Raised Universal
player.addperk 00227FD0 	Serpent's Embrace
player.addperk 00227FE2 	Spaced
player.addperk 00227FE0 	Taskmaster
player.addperk 00227FE1 	Terra Firma
player.addperk 00227FD4 	United Colonies Native
player.addperk 00227FDD 	Wanted

Backgrounds
player.addperk 0022EC76 	Beast Hunter
player.addperk 0022EC81 	Bouncer
player.addperk 0022EC80 	Bounty Hunter
player.addperk 0022EC7F 	Chef
player.addperk 0022EC7E 	Combat Medic
player.addperk 0022EC7D 	Cyber Runner
player.addperk 0022EC7C 	Cyberneticist
player.addperk 0022EC7B 	Diplomat
player.addperk 0022EC79 	Explorer
player.addperk 0022EC78 	Gangster
player.addperk 0022EC77 	Homesteader
player.addperk 0022EC7A 	Industrialist
player.addperk 0022EC75 	Long Hauler
player.addperk 0022EC73 	Pilgrim
player.addperk 0022EC72 	Professor
player.addperk 0022EC74 	Ronin
player.addperk 0022EC71 	Sculptor
player.addperk 0022EC70 	Soldier
player.addperk 0022EC6F 	Space Scoundrel
player.addperk 0022EC6E 	Xenobiologist
player.addperk 002DFD1A 	File Not Found 
-------------------------------------------------------
#Companion perks - An item's Reference ID can be obtained while in the Command Console(~) and using your mouse to click on the NPC to reveal their Reference ID. Use the NPCs ref ID before the perk ID.

Enter multiple times to rank up. The number in () is the max rank.
(NPC ref ID).addperk (Mod ID)
(NPC ref ID).removeperk (Mod ID)

.addperk 22274		EM Weapons(3)
.addperk 2ce1a0		Piloting(4)
.addperk 222f83		Aneutronic Fusion(1)
.addperk 1c06c		Shield Systems(4)
.addperk 222f84		Payload(4)
.addperk 0021b8dd	Marksmanship(3)
.addperk 0021b8dc	Sharpshooting(1)
.addperk 0021b8de	Sniper Cerification(3)
.addperk 0021b8df	Shotgun Certification(3)
.addperk 0021b8e1	Rifle Certification(4)
.addperk 00220bb6	Ballistic Weapon Systems(3)
.addperk 0021b8e6	Ballistics(4)
.addperk 0021b8e0	Particle Beams(4)
.addperk 00222f85	Particle Beam Weapon Systems(4)
.addperk 00222f86	Missile Weapon Systems(3)
.addperk 0021b8c7	Scavenging(1)
.addperk 0021b8d4	Concealment(1)
.addperk 0021b8c5	Gastronomy(4)
.addperk 0021b8cd	Robotics(4)
.addperk 0021b8c2	Satrship Engineering(3)
.addperk 0021b8c8	Outpost Engineering(3)
.addperk 0021b8c3	Outpost Management(3)
.addperk 0021b8cc	Geology(4)
.addperk 0021b8ca	Botany(4)
.addperk 0020e35b	Leadership(4)
.addperk 0021b8e4	Lasers(4)
.addperk 0001bf38	Astrodynamics(4)
.addperk 0021b8da	Stealth(4)
.addperk 0021b8d9	Weight Lifting(3)
.addperk 0021b8c6	Theft(4)
.addperk 0021b8e3	Demolitions(3)
.addperk 0021b8c9	Chemistry(1)
.addperk 0021b8d3	Energy Weapon Dissipation(3)
.addperk 00222f87	Energy Weapon Systems(4)
.addperk 0021b8d5	Wellness(3)
.addperk 0021b8e2	Incapacitation(3)
.addperk 0021b8cb	Medicine(1)
.addperk 0021b8c4	Xenosociology(1)
.addperk 0021b8d2	Pain Tolerance(3)
.addperk 00222f88	Starship Engineering(4) 
-------------------------------------------------------
#Backpacks
Legendary:
player.additem 0010A25D 1 UC AntiXeno Armor Plated (Legendary)

Basic:
player.additem 001773BD 1 SY-920 Pilot
player.additem 00169F59 1 Shocktroop
player.additem 0003B423 1 Cydonia
player.additem 001C0F35 1 Bounty Hunter Stalk
player.additem 001C0F34 1 Bounty Hunter Seek
player.additem 001C0F33 1 Bounty Hunter Track
player.additem 00166402 1 Trackers Alliance
player.additem 001E2B19 1 Constellation
player.additem 00066824 1 Pirate Raiding
player.additem 00066825 1 Pirate Survival
player.additem 0016D15B 1 Deepseeker
player.additem 00166407 1 Ecliptic
player.additem 00169F51 1 Explorer
player.additem 0003084C 1 Old Earth
player.additem 002392B3 1 Ground Crew
player.additem 0001754E 1 Mark I
player.additem 0016E0B6 1 Mercenary
player.additem 001D0F95 1 Mercury
player.additem 002EDF1F 1 Deep Mining
player.additem 00026BEF 1 Deimos
player.additem 00029C7A 1 Tunnel Mining
player.additem 00026BF2 1 Deimos Tunnel
player.additem 000FD333 1 Deepcore
player.additem 0016640B 1 Mantis
player.additem 00067C95 1 Navigator
player.additem 001E2AF7 1 Ranger
player.additem 00169F55 1 Deep Recon
player.additem 0013F97C 1 Peacemaker
player.additem 0016E0BB 1 Space Trucker
player.additem 00003E90 1 Star Roamer
player.additem 00003A77 1 High School Backpack
player.additem 0021A86C 1 UC Shock Armor
player.additem 0020612F 1 UC AntiXeno Skip Pack
player.additem 00257807 1 UC Marine
player.additem 00398105 1 SysDef
player.additem 000EF9AC 1 UC Security
player.additem 0016640E 1 UC Ace Pilot
player.additem 002AAF43 1 SysDef Pilot
player.additem 003E3D4F 1 UC Vanguard Pilot
player.additem 0016D3D0 1 VA Ruun power pack
-------------------------------------------------------
#Backpack mods - The specified modification will be installed on your reference backpack. An item's Reference ID can be obtained while in the Command Console(~) and using your mouse to click on the item dropped on the ground to reveal their Reference ID(It will look like this in the console 'ARMO " (FF01E117).

Example command: FF01E117.amod 000FF442

(reference weapon ID).amod (modification ID) - add mod
(reference weapon ID).rmod (modification ID) - remove mod

Backpack upgrade:
.amod 3AF7F  mod_Armor_Backpack_Quality_05

.amod 3E612F Balanced Boostpack
.amod 3AD4D9 Ballistic Shielding
.amod 3E6131 Basic Boostpack
.amod 3AD4DA EM Shielding
.amod 34BAA3 Emergency Aid
.amod 3AD4DB Energy Shielding
.amod 3A83E7 Exo Servos
.amod F77AA  Explosive Shielding
.amod 24529A Extra Capacity
.amod F77B7  Gravitic Composites
.amod 2C43DA Hacker
.amod 1CAC94 Hazard Protection
.amod F77AF  Heavy Shielding
.amod 2983   Incendiary
.amod 34BAA4 Medic
.amod 3A83E1 Optimized Servos
.amod 50AB3  Oxygen Reserve
.amod 3A83EA Pocketed
.amod 3E6130 Power Boostpack
.amod 34BAA6 Regeneration
.amod 3A83D9 Sensor Array
.amod 3E6132 Skip Capacity Boostpack
.amod 1336BC Technician

ENV Backpack omods
.amod 001C1E05  mod_Armor_Backpack_ENV_Thermal04
.amod 001C1E01  mod_Armor_Backpack_ENV_Radiation04
.amod 001C1DFD  mod_Armor_Backpack_ENV_Corrosive04
.amod 001C1DF5  mod_Armor_Backpack_ENV_Airborne04
.amod 001C1DF6  mod_Armor_Backpack_ENV_Balanced01
Experimental
.amod 000164DB  mod_Armor_Backpack_ENV_Mercury
-------------------------------------------------------
#Spacesuits
Legendary:
player.additem 00065925 1 Incendiary Experimental Nishina Spacesuit
player.additem 0007B2B9 1 Sentinel's UC Antixeno Spacesuit

Epic:
player.additem 0022B8F6 1 Repulsing Explorer Spacesuit

Rare:
player.additem 0013F97D 1 Peacemaker Spacesuit

Basic:
player.additem 00228570 1 Bounty Hunter Spacesuit
player.additem 001E2B18 1 Constellation Spacesuit
player.additem 0005278E 1 Deep Mining Spacesuit
player.additem 002265AE 1 Deep Recon Spacesuit
player.additem 002265AE 1 Deepcore Spacesuit
player.additem 0016D2C4 1 Deepseeker Spacesuit
player.additem 00026BF1 1 Deimos Spacesuit
player.additem 0022856F 1 Ecliptic Spacesuit
player.additem 002265AF 1 Explorer Spacesuit
player.additem 001F22BB 1 Gran-Gran’s Spacesuit
player.additem 002392B5 1 Ground Crew Spacesuit
player.additem 00226299 1 Mantis Spacesuit
player.additem 0001754D 1 Mark I Spacesuit
player.additem 001D0F96 1 Mercury Spacesuit
player.additem 00225FC9 1 Monster Costume
player.additem 00067C94 1 Navigator Spacesuit
player.additem 0003084E 1 Old Earth Spacesuit
player.additem 00066821 1 Pirate Assault Spacesuit
player.additem 00066826 1 Pirate Charger Spacesuit
player.additem 00066828 1 Pirate Corsair Spacesuit
player.additem 0006682A 1 Pirate Sniper Spacesuit
player.additem 00227CA0 1 Ranger Spacesuit
player.additem 002265AD 1 Shocktroop Spacesuit
player.additem 0021C780 1 Space Trucker Spacesuit
player.additem 00004E78 1 Star Roamer Spacesuit
player.additem 0012E187 1 Starborn Spacesuit Astra
player.additem 001CBA52 1 Starborn Spacesuit Avitus
player.additem 001CBA4E 1 Starborn Spacesuit Bellum
player.additem 0021C77E 1 Starborn Spacesuit Gravitas
player.additem 001CBA4A 1 Starborn Spacesuit Locus
player.additem 001CBA49 1 Starborn Spacesuit Locus
player.additem 002D7365 1 Starborn Spacesuit Solis
player.additem 002D7346 1 Starborn Spacesuit Tempus
player.additem 001CBA4D 1 Starborn Spacesuit Tenebris
player.additem 0021C77F 1 Starborn Spacesuit Venator
player.additem 002AAF44 1 SysDef Ace Spacesuit
player.additem 00398104 1 SysDef Assault Spacesuit
player.additem 0039810A 1 SysDef Combat Spacesuit
player.additem 00398108 1 SysDef Sec Recon Spacesuit
player.additem 00398103 1 SysDef Spacesuit
player.additem 00166404 1 Trackers Alliance Spacesuit
player.additem 00166410 1 UC Ace Spacesuit
player.additem 00206130 1 UC AntiXeno Spacesuit
player.additem 00257808 1 UC Combat Spacesuit
player.additem 00257805 1 UC Marine Spacesuit
player.additem 000EF9B0 1 UC Sec Combat Spacesuit
player.additem 000EF9AF 1 UC Sec Recon Spacesuit
player.additem 000EF9AE 1 UC Sec Starlaw Spacesuit
player.additem 000EF9AD 1 UC Security Spacesuit
player.additem 00257809 1 UC Startroop Spacesuit
player.additem 0021A86A 1 UC Urbanwar Spacesuit
player.additem 00248C0F 1 UC Vanguard Spacesuit
player.additem 0025780A 1 UC Wardog Spacesuit
player.additem 00227CA3 1 Va’Ruun Spacesuit
-------------------------------------------------------
#Armor mods - The specified modification will be installed on your reference armor. An item's Reference ID can be obtained while in the Command Console(~) and using your mouse to click on the item dropped on the ground to reveal their Reference ID(It will look like this in the console 'ARMO " (FF01E117).

Example command: FF01E117.amod 000FF442

(reference weapon ID).amod (modification ID) - add mod
(reference weapon ID).rmod (modification ID) - remove mod

Armor upgrade:
.amod 3AF7D   mod_Armor_Spacesuit_Quality_05

Slot 1
.amod 0013369C 	Ablative 	-15% incoming Energy damage.
.amod 0013369E 	Anti-Ballistic 	-15% incoming Physical damage from ranged weapons.
.amod 001336BD 	Beast Hunter 	-15% damage from Alien enemies.
.amod 001336C6 	Bolstering 	Grants up to +100 Energy resistance and Physical resistance, the lower your health.
.amod 001336C1 	Chameleon 	Blend with the environment while sneaking and not moving.
.amod 001336BE 	Combat Veteran 	-15% damage from Human enemies.
.amod 000690B0 	O2 Boosted 	+20% oxygen capacity.
.amod 000690AE 	O2 Filter 	-25% oxygen consumption.
.amod 00133699 	Sturdy 	-15% incoming Melee damage.
.amod 001336BC 	Technician 	-15% damage from Robot enemies.

Slot 2
.amod 000710FD 	Acrobat 	-50% fall damage.
.amod 000690AF 	Analyzer 	+10% damage to scanned targets.
.amod 000710FA 	Antiseptic 	+25 Airborne Resistance.
.amod 000C9A43 	Auto Medic 	Automatically use a Med Pack when hit and health is below 25%, once every 60 seconds.
.amod 002EDE4E 	Fastened 	+20 carry capacity.
.amod 000710F7 	Galvanized 	+25 Corrosive Resistance.
.amod 002C43DA 	Hacker 	+2 max auto attempts that can be banked while hacking.
.amod 000710F5 	Leadlined 	+25 Radiation Resistance.
.amod 000710F6 	Liquid Cooled 	+25 Thermal Resistance.
.amod 00060293 	Resource Hauler 	Resources weigh 25% less.
.amod 00060295 	Weapon Holsters 	Weapons weigh 50% less.

Slot 3
.amod 002EDE59 	Armor-Plated 	-10% incoming Physical, Energy, an EM damage.
.amod 002EDE4F 	Assisted Carry 	Drain 75% less 02 when running while encumbered.
.amod 002C43DC 	Headhunter 	Deals +25% damage on the next attack after hitting a target's head.
.amod 00002983 	Incendiary 	10% chance to ignite nearby attackers.
.amod 000BE542 	Mechanized 	+40 carry capacity.
.amod 00059AE8 	Mirrored 	4% chance to reflect attacks.
.amod 002D01A2 	Peacemaker 	Rifles do 10% more damage.
.amod 0006029F 	Reactive 	10% chance to stagger nearby attackers.
.amod 0006029D 	Repulsing 	5% chance to disarm nearby attackers.
.amod 002C43DB 	Sensor Chip 	+20% accuracy while firing on the move.
.amod 000BE540 	Sentinel 	75% chance to reduce damage by 50% while standing still. 

Tiers
.amod 0011E2B5  Base
.amod 0011E2B6  Calibrated
.amod 0011E2B7  Refined
.amod 0011E2B8  Advanced
.amod 0003AF80  Superior
.amod 25AF2B    Combat resist +1
.amod 1C5AA4    Combat resist +2
.amod 1C5AA6    Combat resist +3
.amod 1C5AAC    Combat resist +4
.amod 1C5AAD    Combat resist +5
.amod 1C5AFA    Haz. Resist +1
.amod 1C5AFB    Haz. Resist +2
-------------------------------------------------------
#Clothes
player.additem 0012B4B3 1	Akila Secruity Hat
player.additem 00227720 1	Akila Security Uniform
player.additem 001E426E 1	Amanirenas Hat
player.additem 003E3D51 1	Ambassador Suit
player.additem 0021BBEC 1	Argos Extractor Jumpsuit
player.additem 001C84DB 1	Argos Jacketed Jumpsuit
player.additem 003FDBF7 1	B.Morgan's Suit
player.additem 0019219C 1	Batball Cap
player.additem 003E8E7F 1	Bayu's Corpwear
player.additem 001466EE 1	Black Elbow Grease Gear
player.additem 001466F2 1	Black Engineering Outfit
player.additem 001466EA 1	Black Leather Jumpsuit
player.additem 00246B32 1	Blue Collar Offwork Duds
player.additem 00246B30 1	Blue Collar Offwork Hat
player.additem 00077814 1	Blue Elbow Grease Gear
player.additem 003A264E 1	Blue Lab Outfit
player.additem 0029E174 1	Blue Labor Jumpsuit
player.additem 001B52FF 1	Blue Neocity Formwear
player.additem 002619F1 1	Blue Neocity Poncho
player.additem 00077810 1	Blue UC Leather Jumpsuit
player.additem 001466EF 1	Brown Elbow Grease Gear
player.additem 001466F3 1	Brown Engineering Outfit
player.additem 00062EA3 1	Brown Leather Jumpsuit
player.additem 001466EB 1	Brown Leather Jumpsuit
player.additem 001B5300 1	Brown Neocity Formwear
player.additem 002619F6 1	Casual Street Suit
player.additem 00235B7D 1	Clean Suit
player.additem 00185A6F 1	Chunks Cap
player.additem 001A8DDD 1	Chunks Service Uniform
player.additem 001A4253 1	Corpo Boardroom Suit
player.additem 00190D0B 1	Corpo Executive Suit
player.additem 002265B0 1	Corpo Power Suit
player.additem 0019F9C1 1	Corpo Salary Suit
player.additem 002265B1 1	Corpo Sleek Suit
player.additem 001F1DCE 1	Cream and Blue Dress
player.additem 000788AB 1	Cyberware Streetwear
player.additem 00177494 1	Dalton Fiennes' Suit
player.additem 00185A6E 1	Deimos Cap
player.additem 002BA0E1 1	Deputy Hat
player.additem 002262D3 1	Disciples Tagwear
player.additem 001625DC 1	DJ Headphones
player.additem 001625DB 1	DJ Headphones Cap
player.additem 0017A439 1	ECS Captain Actionwear
player.additem 0017A437 1	ECS Officer Uniform
player.additem 0017A438 1	ECS Uniform
player.additem 001A8DE6 1	Enhance Service Uniform
player.additem 00077816 1	Engineering Outfit
player.additem 003FC344 1	Explorer Adventure Hat
player.additem 00204002 1	Farming Hat
player.additem 002262D5 1	Farming Outfit
player.additem 00250C86 1	Fashionable Suit
player.additem 0010799A 1	Faye Sengsavahn's Outfit
player.additem 0009F0F6 1	Festive Neocity Poncho
player.additem 003EC02E 1	Filthy Physician Uniform
player.additem 0024EF42 1	Fishworker Mask
player.additem 0024EF40 1	Fishworker Splashwear
player.additem 0024EF41 1	Fishworker Wetwear
player.additem 003E5D26 1	First Mercenary Outfit
player.additem 0021113E 1	First Officer Hat
player.additem 00228826 1	First Officer Outfit
player.additem 00228825 1	First Soldier Outfit
player.additem 000788A1 1	Formal Slack Suit
player.additem 0021BBF1 1	Franklin Roosevelt's Outfit
player.additem 0022856C 1	Freestar Duelwear
player.additem 00224FE9 1	Freestar Dustwear
player.additem 0021712A 1	Freestar Militia Hat
player.additem 00228827 1	Freestar Militia Uniform
player.additem 001CB843 1	GalBank Service Uniform
player.additem 003CD80F 1	Generdyne Lab Uniform
player.additem 003CD810 1	Generdyne Security Uniform
player.additem 001D8426 1	Genghis Khan's Hat
player.additem 002262D2 1	Genghis Khan's Outfit
player.additem 00177492 1	Genevieve Monohan's Suit
player.additem 001466F0 1	Gray Elbow Grease Gear
player.additem 0029E175 1	Gray Labor Jumpsuit
player.additem 001466EC 1	Gray Leather Jumpsuit
player.additem 002619EF 1	Green Fashionable Suit
player.additem 0029AEAE 1	Hazmat Suit
player.additem 00273C05 1	Homesteader Scout Hat
player.additem 00185A6C 1	Hopetech Cap
player.additem 00108353 1	Ikande's SysDef Officer Uniform
player.additem 00177493 1	Imogene Salzo's Suit
player.additem 0025DEF0 1	Inclement Weather Outfit
player.additem 000788AA 1	Jacketed Leatherwear
player.additem 00009CC7 1	Leatherwear
player.additem 002619FD 1	Leather Streetwear
player.additem 002619FE 1	Leather Pocketwear
player.additem 00177495 1	Linden Calderi's Suit
player.additem 00030B4B 1	Matteo Khatri's Hat
player.additem 00030B4D 1	Matteo's Outfit
player.additem 00226298 1	Masako Imada's Outfit
player.additem 001A52D1 1	Megacorp Executive Suit
player.additem 000028A5 1	Medic Uniform
player.additem 002262D1 1	Mei Devine's Outfit
player.additem 0026D8AA 1	Miner Hard Hat Outfit
player.additem 0001D1D7 1	Miner Jumpsuit
player.additem 0001D1D9 1	Miner Jacketed Jumpsuit
player.additem 0009B72F 1	Miner Orebreaker Outfit
player.additem 0001D1E7 1	Miner Utility Outfit
player.additem 00225FCA 1	Naeva's Outfit
player.additem 000C47A0 1	NASA Lab Uniform
player.additem 001F1DC9 1	Navy Tan Dress
player.additem 002266A2 1	Neocity Corpwear
player.additem 000788A4 1	Neocity Hustler Outfit
player.additem 002266A3 1	Neon Businesswear
player.additem 001F1DD0 1	Neon Clublife Skirt
player.additem 000C900A 1	Neon Dancer Headwear
player.additem 00225FCC 1	Neon Dancer Outfit
player.additem 003556E7 1	Neon Nightlife Jumpsuit
player.additem 001F1DCF 1	Neon Nightlife Skirt
player.additem 00225D9E 1	Neon Security Uniform
player.additem 00165720 1	Neon Socialite Skirt
player.additem 0021BBF2 1	New Atlantis Sec Uniform
player.additem 001A2507 1	NeuroBoost Mark I
player.additem 00100517 1	NeuroBoost Mark II
player.additem 00100518 1	NeuroBoost Mark III
player.additem 00100519 1	NeuroCom Mark I
player.additem 0010051A 1	NeuroCom Mark II
player.additem 0010051B 1	NeuroCom Mark III
player.additem 0010051C 1	NeuroTac Mark I
player.additem 0010051D 1	NeuroTac Mark II
player.additem 0010051F 1	NeuroTac Mark III
player.additem 00225DA0 1	Nightwear
player.additem 00036AFC 1	Noel's Outfit
player.additem 0018DE02 1	Nyx's Outfit
player.additem 0018B54A 1	Operative Suit
player.additem 00261A03 1	Padded Hat
player.additem 0002FE70 1	Paradiso Staff Uniform
player.additem 002BC183 1	Patient's Clothes
player.additem 003E5D27 1	Paxton's Officer Hat
player.additem 0022766B 1	Pirate Captain Outfit
player.additem 002491EA 1	Prison Scrubs
player.additem 00208E8B 1	Prisoner Uniform
player.additem 00226297 1	Physician Uniform
player.additem 001BF2F8 1	Pryce's Suit
player.additem 0013730B 1	Ranger Deputy Uniform
player.additem 002BA0E1 1	Ranger Hat
player.additem 001CFA01 1	Red Mile Service Uniform
player.additem 000028A6 1	Reliant Medical Uniform
player.additem 00003BF6 1	Resort Wear
player.additem 00003C4D 1	Resort Wear
player.additem 003EB4B4 1	Rokov's Officer Hat
player.additem 0037A34E 1	Ryujin Guard Uniform
player.additem 00034110 1	Ryujin Lab Outfit
player.additem 001823CB 1	Ryujin Lab Worker Hood
player.additem 001823CC 1	Ryujin Lab Worker Outfit
player.additem 00034114 1	Ryujin R&D Outfit
player.additem 0001D1DE 1	Sam Coe's Outfit
player.additem 0016571D 1	Sanctum Priest Headwear
player.additem 00055905 1	Sarah Morgan's Outfit
player.additem 0021C786 1	Sari Dress
player.additem 000CC4D1 1	Security Flightsuit
player.additem 0021C783 1	Service Industry Uniform
player.additem 0025DEEF 1	Settler Adventure Hat
player.additem 00258039 1	Settler Casual Hat
player.additem 0024EF65 1	Settler Hat
player.additem 000753F4 1	Shielded Lab Outfit
player.additem 0021C782 1	Shinya Voss Outfit
player.additem 0016E0B9 1	Ship Captain Hat
player.additem 0021C781 1	Ship Captain's Uniform
player.additem 0029080F 1	Space Rogue Muscle Gear
player.additem 0029080E 1	Space Rogue Outfit
player.additem 002456F2 1	Space Trucker Bar Duds
player.additem 002456F3 1	Space Trucker Cap
player.additem 00246B31 1	Space Trucker Cargowear
player.additem 002456F4 1	Space Trucker Casualwear
player.additem 002470D1 1	Space Trucker Flannel
player.additem 002470D2 1	Space Trucker Flannel
player.additem 0029080D 1	Space Trucker Hat
player.additem 002470D0 1	Space Trucker Haul Wrap
player.additem 00165722 1	Space Undersuit
player.additem 002E18F6 1	Striker Maskwear
player.additem 00064A2E 1	Striker Streetwear
player.additem 00027189 1	Suit with Lapel Pin
player.additem 0002FA4  1	Swimsuit
player.additem 000D41F8 1	SY-920 Fatigues
player.additem 0011F3A8 1	Syndicate Capo Suit
player.additem 0011F3AC 1	Syndicate Club Suit
player.additem 0011F3AD 1	Syndicate Boss Suit
player.additem 0011F3B0 1	Syndicate Pinstripes
player.additem 0011F3A7 1	Syndicate Thug Suit
player.additem 002619FC 1	Synth Leatherwear
player.additem 002619FC 1	Synthleather Streetwear
player.additem 003329BB 1	SysDef Crew Uniform
player.additem 003329B4 1	SysDef Formal Uniform
player.additem 0021C1FB 1	SysDef Officer Uniform
player.additem 000D981C 1	SysDef Prison Scrubs
player.additem 00185A69 1	Taiyo Astroneering Cap
player.additem 001466F1 1	Teal Elbow Grease Gear
player.additem 001466F9 1	Teal Engineering Outfit
player.additem 001466ED 1	Teal Leather Jumpsuit
player.additem 003CF431 1	TerraBrew Barista Outfit
player.additem 0007F88D 1	TerraBrew Uniform
player.additem 001CB7E7 1	Trade Authority Uniform
player.additem 00164BDD 1	Trident Crew Uniform
player.additem 000DBFDA 1	Trident Guard Uniform
player.additem 00185A68 1	Trident Luxury Lines Cap
player.additem 00034111 1	Tritek Lab Outfit
player.additem 00077818 1	UC Gray Utility Jumpsuit
player.additem 002C6E7D 1	UC Navy Armored Fatigues
player.additem 0018E260 1	UC Navy Crew Hat
player.additem 0021A86E 1	UC Navy Crew Uniform
player.additem 003E3ACF 1	UC Navy Duty Fatigues
player.additem 002C6E7F 1	UC Navy Fatigues
player.additem 002C6E7E 1	UC Navy Hat
player.additem 003E3AD1 1	UC Navy Recon Fatigues
player.additem 0021A86D 1	UC Navy Officer Uniform
player.additem 0025E8D4 1	UC Security Uniform
player.additem 003329BC 1	UC SysDef Crew Hat
player.additem 003B2A81 1	Ularu's Suit
player.additem 00185A67 1	United Colonies Cap
player.additem 002619FB 1	Urban Operator Outfit
player.additem 000788A2 1	Urban Slackwear
player.additem 00251F56 1	Utility Flightsuit
player.additem 000781F9 1	Utility Headphone Cap
player.additem 00252AE7 1	Utility Headphones
player.additem 003CAF7E 1	Vanguard Officer Uniform
player.additem 002619F7 1	Vested Suit
player.additem 0002B5EE 1	White Neocity Poncho
player.additem 0029E173 1	Yellow Labor Jumpsuit
player.additem 0004008C 1	Xenofresh Clean Suit
player.additem 001466FF 1	Xenofresh Tech Outfit
-------------------------------------------------------
#Apparel mods - The specified modification will be installed on your reference armor. An item's Reference ID can be obtained while in the Command Console(~) and using your mouse to click on the item dropped on the ground to reveal their Reference ID(It will look like this in the console 'ARMO " (FF01E117).

Example command: FF01E117.amod 000FF442

(reference weapon ID).amod (modification ID) - add mod
(reference weapon ID).rmod (modification ID) - remove mod

.amod 0010052B   Mk1 Intimidation
.amod 0010052D   Mk2 Intimidation
.amod 0010052F   Mk3 Intimidation

.amod 00100531   Mk1 Diplomacy
.amod 00100533   Mk2 Diplomacy
.amod 00100535   Mk3 Diplomacy

.amod 00100537   Mk1 Instigation
.amod 00100539   Mk2 Instigation
.amod 0010053B   Mk3 Instigation 
-------------------------------------------------------
#Helmets

Helmet upgrade:
.amod 3AF80   mod_Armor_Helmet_Quality_05

Legendary Helmets
player.additem 00065926 1	Reactive Experimental Nishina Helmet (Legendary)
player.additem 0010A25E 1	Incendiary UC AntiXeno Space Helmet (Legendary)

Base Helmets
player.additem 001466F6 1	Black Graviplas Helmet
player.additem 001466FA 1	Black Open Graviplas Helmet
player.additem 001C0F32 1	Bounty Hunter Space Helmet
player.additem 002EDE9C 1	Broken Constellation Space Helmet
player.additem 001466F7 1	Brown Graviplas Helmet
player.additem 001E2B17 1	Constellation Space Helmet
player.additem 0003B424 1	Cydonia Space Helmet
player.additem 00052792 1	Deep Mining Space Helmet
player.additem 00169F54 1	Deep Recon Space Helmet
player.additem 0006ABFF 1	Deepcore Space Helmet
player.additem 0016D15C 1	Deeseeker Space Helmet
player.additem 00026BF0 1	Deimos Space Helmet
player.additem 00228829 1	Ecliptic Space Helmet
player.additem 00169F50 1	Explorer Space Helmet
player.additem 0021F3F4 1	First Solider Helmet
player.additem 003CD812 1	Generdyne Guard Helmet
player.additem 001F22BC 1	Gran-Gran's Space Helmet
player.additem 000781F7 1	Graviplas Merc Helmet
player.additem 001466F8 1	Gray Graviplas Helmet
player.additem 001466FC 1	Gray Open Graviplas Helmet
player.additem 002392B4 1	Ground Crew Space Helmet
player.additem 0016640A 1	Mantis Space Helmet
player.additem 0001754F 1	Mark I Space Helmet
player.additem 0016E0B5 1	Mercenary Space Helmet
player.additem 001D0F94 1	Mercury Space Helmet
player.additem 00067C93 1	Navigator Space Helmet
player.additem 001F73EF 1	Neon Security Helmet
player.additem 0003084D 1	Old Earth Space Helmet
player.additem 000781F8 1	Open Graviplas Helmet
player.additem 0016E0C3 1	Operative Helmet
player.additem 0013F97B 1	Peacemaker Helmet
player.additem 00066822 1	Pirate Assault Space Helmet
player.additem 00066827 1	Pirate Charge Space Helmet
player.additem 00066829 1	Pirate Corsair Space Helmet
player.additem 0006682B 1	Pirate Sniper Space Helmet
player.additem 001E2AC1 1	Ranger Space Helmet
player.additem 0037A34F 1	Ryujin Guard Helmet
player.additem 00165718 1	Security Guard Helmet
player.additem 00169F58 1	Shocktrooper Space Helmet
player.additem 0016E0BD 1	Space Trucker Space Helmet
player.additem 00003E8F 1	Star Roamer Space Helmet
player.additem 002F4B39 1	SY-920 Space Helmet
player.additem 00398107 1	SysDef Armored Space Helmet
player.additem 00398106 1	SysDef Space Helmet
player.additem 002AAF45 1	System Def Ace Space Helmet
player.additem 001466F9 1	Teal Graviplas Helmet
player.additem 001466FD 1	Teal Open Graviplas Helmet
player.additem 00166403 1	Trackers Alliance Space Helmet
player.additem 0014E44E 1	Trident Guard Helmet
player.additem 0016640F 1	UC Ace Pilot Space Helmet
player.additem 0025780B 1	UC Armored Space Helmet
player.additem 00257806 1	UC Marine Space Helmet
player.additem 000EF9B2 1	UC Sec Spaceriot Helmet
player.additem 0025E8D5 1	UC Security Helmet
player.additem 000EF9B1 1	UC Security Space Helmet
player.additem 0021A86B 1	UC Urbanwar Space Helmet
player.additem 00248C0E 1	UC Vanguard Space Helmet
player.additem 0016D3D1 1	Va'ruun Space Helmet
-------------------------------------------------------
#Helmet mods

Stat 1
.amod 000690b0  o2 boosted	      +20% oxygen
.amod 000690ae  o2 filter	      -25% oxygen consumption (doesnt work together with o2 boosted)

Stat 2
.amod 000690af  analyzer	      +10% dmg to scanned targets
.amod 002c43da  hacker		      +2 max auto attempts that can be banked while hacking
Stat 3
.amod 002c43db  sensor chip	      +20% acc while moving
.amod 002c43dc  headhunter	      +25% dmg on next attack after a headshot
-------------------------------------------------------
#Weapons - Note: The version(Modified or standard) is random just keep entering the code to get eather or.

Legendary and Unique weapons
player.additem 0014920B 1	Despondent Assassin - Rifle
player.additem 00329ABB 1	Eternity's Gate - Particle Beam Rifle
player.additem 0008D850 1	Keelhauler - Pistol
player.additem 00316416 1	Memento Mori - Pistol
player.additem 0008AF62 1	Revenant - Rifle
player.additem 001F02EF 1	Unmitigated Violence - Rifle

Epics
player.additem 000367C5 1	Davis Wilson's Rifle
player.additem 000E7ED1 1	Peacemaker - Rifle
player.additem 003CE4B1 1	Unfair Advantage - Pistol

Rares
player.additem 001EEE4F 1	Ambassador - Pistol
player.additem 0031FCBF 1	Ashta Tamer - Heavy
player.additem 0031F257 1	Experiment A-7 - Shotgun
player.additem 002E82A0 1	Feather - Rifle
player.additem 000019F5 1	Fiscal Quarter - Rifle
player.additem 0032046E 1	Fortune's Glory - Melee
player.additem 002E0729 1	Fury - Rifle
player.additem 0032046C 1	Gallow's Reach - Rifle
player.additem 0032046A 1	Heller's Cutter - Heavy
player.additem 002E3E83 1	Hunterwulf - Rifle
player.additem 001A52E5 1	Peacekeeper - Rifle
player.additem 0022A8E1 1	Power Beat - Rifle
player.additem 003CE4B0 1	Tempest - Rifle
player.additem 0000CAB0 1	The Mutineer - Pistol
player.additem 0031F25A 1	The Last Priest - Melee
player.additem 000019F7 1	Unrestrained Vegenence - Rifle
player.additem 0008AF5D 1	X-989 Microgun - Heavy

Base
player.additem 001BBF2A 1	Deadeye
player.additem 002F99FF 1	Ember - Pistol
player.additem 002BD871 1	Jake's Hangover Cure - Particle Beam Shotgun
player.additem 001BAA3C 1	Justifier
player.additem 001F27F5 1	Sir Livingstone's Pistol
player.additem 0008AF68 1	Solace - Pistol

Standard
player.additem 002BF65B 1 AA-99
player.additem 0026D965 1 Arc Welder
player.additem 0026D964 1 AutoRivet
player.additem 0026F181 1 Barrow Knife
player.additem 0004716C 1 Beowulf
player.additem 0026D963 1 Big Bang
player.additem 000547A3 1 Breach
player.additem 0026D96A 1 Bridger
player.additem 0026D961 1 Calibrated solstice
player.additem 0026D96B 1 Coachman
player.additem 00035A48 1 Combat Knife
player.additem 00016758 1 Cutter
player.additem 0018DE2C 1 Drum Beat
player.additem 002F413A 1 Discarded Sidestar
player.additem 0026D96E 1 Ecliptic Pistol
player.additem 000476C4 1 Eon
player.additem 0001BC4F 1 Equinox
player.additem 00028A02 1 Grendel
player.additem 000546CC 1 Hard Target
player.additem 00253A16 1 Kodama
player.additem 0021FEB4 1 Kraken
player.additem 0002D7F4 1 Lawgiver
player.additem 002984DF 1 Maelstrom
player.additem 0002EB3C 1 MagShear
player.additem 00023606 1 MagPulse
player.additem 0002EB42 1 MagShot
player.additem 0002EB45 1 MagSniper
player.additem 0026035E 1 MagStorm
player.additem 000546CD 1 Microgun
player.additem 0026D970 1 Negotiator
player.additem 0026D968 1 Novablast Disruptor
player.additem 0026D967 1 Novalight
player.additem 0026ED2A 1 Old Earth Assault Rifle
player.additem 0021BBCD 1 Old Earth Hunting Rifle
player.additem 0026D96C 1 Old Earth Pistol
player.additem 00278F74 1 Old Earth Shotgun
player.additem 0026D966 1 Osmium Dagger
player.additem 002773C8 1 Orion
player.additem 002953F8 1 Pacifier
player.additem 00040826 1 Rattler
player.additem 00000FD6 1 Razorback
player.additem 0002CB5F 1 Regulator
player.additem 0004F760 1 Rescue Axe
player.additem 0026D95E 1 Ripshank
player.additem 0026D960 1 Shotty
player.additem 0026D95D 1 Sidestar
player.additem 0026D8A3 1 Tanto
player.additem 0002EB36 1 Tombstone
player.additem 0026D8A5 1 UC Naval Cutlass
player.additem 0026D96D 1 Urban Eagle
player.additem 0026D8A0 1 VaRuun Inflictor
player.additem 0026D8A2 1 VaRuun Painblade
player.additem 0026D8A4 1 VaRuun Starshard
player.additem 0026D8A1 1 Wakiazashi
player.additem 0024561C 1 XM-2311

Grenades
player.additem 000115EF 1	Frag Grenade
player.additem 0026D89F 1	Impact Grenade
player.additem 0026F180 1	Incendiary Grenade
player.additem 0026D89E 1	Particle Grenade
player.additem 0026D89D 1	Shrapnel Grenade
-------------------------------------------------------
#Weapon modifiers - The specified modification will be installed on your reference weapon. An item's Reference ID can be obtained while in the Command Console(~) and using your mouse to click on the item dropped on the ground to reveal their Reference ID(It will look like this in the console 'WEAP " (FF01E117).

Example command: FF01E117.amod 000FF442

(reference weapon ID).amod (modification ID) - add mod
(reference weapon ID).rmod (modification ID) - remove mod

.amod 62896     Use this to upgrade any weapon.

Stat 1
.amod 000FF442 	Anti-Personnel - 10% damage against humans.
.amod 000FEA07 	Bashing - Deals double damage when gun bashing.
.amod 000F437E 	Berserker - Does more damage the less armor one has.
.amod 000F428E 	Cornered - Damage increases as health decreases.
.amod 001625EB 	Disassembler - +20% damage against robots.
.amod 000FFA3B 	Extended Magazine - Doubles the base magazine capacity.
.amod 0015DD18 	Exterminator - +30% damage against ailens.
.amod 000EA117 	Furious - Each consecutive hit deals more damage.
.amod 000F2013 	Instigating - Deals double damage to targets with full health.
.amod 000FAEAB  Oxygenated - Hold-breath time when aiming using a scoped weapon is increased.
.amod 000F7321 	Space-Adept - +30% damage while in space, and -15% damage while on a planet.

Stat 2
.amod 0008AB47  Corrosive - Randomly deals corrosive damage and reduces the targets’ armor over 6 seconds.
.amod 000F2E39  Crippling - Deals +30% damage on the next attack after hitting a target’s limbs.
.amod 000FC884 	Demoralizing - Small chance to demoralize a target.
.amod 000FA8D6 	Explosive - Randomly switches to explosive rounds.
.amod 000FC8A4 	Frenzy - Small chance to frenzy a target.
.amod 000F4557 	Shattering - Break through even the strongest armor.
.amod 000FFA3D 	Titanium Build - Make this weapon light as a feather.
.amod 0031C0C5  Elemental - Randomly deals Corrosive, Radiation, Poison, and Incendiary damage.

Stat 3
.amod 000FBD3C  Concussive - Small chance to knock down targets.
.amod 000EA0BA 	Handloading - Volatile rounds that pack a bigger punch but aren't as stable and can occassionaly fail.
.amod 00122F1C 	Hitman - +15% damage while aiming.
.amod 00002983  Incendiary - 10% chance to ignite.
.amod 0007D728  Incendiary - randomly deal incendiary damage.
.amod 000FEA49 	Lacerate - Randomly applies a bleed effect to the target.
.amod 000FFA3C 	Med Theft - Chance that humans drop extra Med Packs on death.
.amod 00319AEC 	Poison - Randomly deals poison damage and slows the target.
.amod 000EA13b  Radioactive - Randomly deals radioactive damage and demoralizes the target.
.amod 000FEA04 	Rapid - +25% increase in attack speed.
.amod 000E8D64 	Staggering - Small chance to stagger enemies.
.amod 0031C0C4 	Skip Shot - Every fourth shot fires two projectiles at once.
.amod 0031C0C6 	Telsa - Rounds will sometimes emit electricity that damages and slows nearby targets.
-------------------------------------------------------
#Ammo
player.additem 002B559C 100	.27 Caliber
player.additem 002B559A 100	.43 MI Array
player.additem 002B5599 100	.43 Ultramag
player.additem 002B5598 100	.45 Caliber ACP
player.additem 002B5597 100	.50 Caliber Caseless
player.additem 002B5596 100	.50 MI Array
player.additem 002BAE3F 100	1.5KV LZR Cartridges
player.additem 002B5595 100	11MM Caseless
player.additem 002B5594 100	12.5MM ST Rivet
player.additem 000547A1 100	12G Shotgun Shell
player.additem 002B4AFC 100	15X25 CLL Shotgun Shell
player.additem 0000E8EC 100	3KV LZR Cartridge
player.additem 002B5592 100	40MM XPL
player.additem 002B5590 100	6.5MM CT
player.additem 002B558F 100	6.5MM MI Array
player.additem 002B558E 100	7.5MM Whitehot
player.additem 002B558D 100	7.62x39MM
player.additem 0004AD3E 100	7.77MM Caseless
player.additem 002B559B 100	9x39MM
player.additem 002B4AFB 100	Caseless Shotgun Shell
player.additem 002B558B 100	Heavy Particle Fuse
player.additem 002B558A 100	Light Particle Fuse
-------------------------------------------------------
#Mission/Quest settings
To find the Quest ID for the quest you wish to investigate or edit, you'll need to make use of the help console command. Typing help into the console followed by a single word related to the quest will look up all associated items that include that phrase. You're looking for QUST entries, which denote a Quest. It's also possible to limit results to show Quest entries only:

help (name) 4 QUST

Main Quests: MQ
Companion Quests: COM_Quest(or the name of the companion)
UC Vanguard Quests: UC
Freestar Collective Quests: FC
Crimson Fleet Quests: CF
New Atlantis Quests: City_NA and City_NewAtlantis
Akila Quests: City_AC and City_Akila
Neon Quests: City_Neon
Cydonia Quests: City_CY
Space Quests: MS
sqt command: Current quest:(shows name of current quest)

Starts all main story and side missions(Note: Can cause crashes)
saq

Completes all main story and side missions(Note: Can cause crashes)
caqs

Show all your current quest targets
sqt

Instantly complete the specified quest
completequest [quest id]

Starts specified quest
startquest [quest id]

Stops specified quest
stopquest [quest id]

Resets specified quest
resetquest [quest id]

Shows all specified quest objectives - Note: not entering quest ID will show all quests
sqo [quest id]

Shows all specified quest stages
sqs [quest id]

Completes all specified quest objectives
completeallobjectives [quest id]

Move to specified quest target
movetoquesttarget [quest id]
-------------------------------------------------------
#All Main Mission IDs - Important Note for Into the Unknown Mission:
-Before using console commands to complete "Into the Unknown", be sure "Back to Vectera" and "The Empty Nest" are completed first as there is a known bug that can prevent the next mission from starting.
-It's also crucial that you do not equip or use your new Power until you have completed "Into the Unknown" with the "SetStage 000160A9 1010" command. Once the mission is finished, "All That Money Can Buy" will be triggered.
-Should you equip or use your Power before "Into the Unknown" is completed, there's a high chance the next mission will not trigger. If this is the case, you'll need to reload an old save to continue.

    SQS (QUEST ID)
    SQO (Quest ID)
    GetStage (QUEST ID)
    SetStage (QUEST ID) 
    StartQuest (Quest ID)
    CompleteQuest (QUEST ID)

00003448 	One Small Step	

    SetStage 00003448 10
    SetStage 00003448 160
    SetStage 00003448 210
    SetStage 00003448 250
    SetStage 00003448 300
    SetStage 00003448 310
    SetStage 000114CD 400
    SetStage 000114CD 600
    SetStage 00003448 1000
    SetStage 00003448 1800
    SetStage 00003448 2000
    SetStage 00003448 2100

000114CD 	The Old Neighborhood	

    SetStage 000114CD 10
    SetStage 000114CD 100
    SetStage 000114CD 200
    SetStage 000114CD 670
    SetStage 000114CD 820
    SetStage 000114CD 1100
    SetStage 000114CD 1130
    SetStage 000114CD 1150

0001638D 	Back to Vectera	

    SetStage 0001638D 5
    SetStage 0001638D 100
    SetStage 0001638D 110
    SetStage 0001638D 130
    SetStage 0001638D 205
    SetStage 0001638D 300
    SetStage 0001638D 1000

000114C9 	The Empty Nest	

    SetStage 000114C9 100
    SetStage 000114C9 330
    SetStage 000114C9 430
    SetStage 000114C9 600
    SetStage 000114C9 830
    SetStage 000114C9 1131

000160A9 	Into the Unknown	

    SetStage 000160A9 10
    SetStage 000160A9 20
    SetStage 000160A9 60
    SetStage 000160A9 220
    SetStage 000160A9 300
    SetStage 000160A9 305
    SetStage 000160A9 600
    SetStage 000160A9 1000
    SetStage 000160A9 1010

002C1C9B 	All That Money Can Buy	

    SetStage 002c1c9b 2000

00021BEF 	Starborn	

    SetStage 00021BEF 20
    SetStage 00021BEF 100
    SetStage 00021BEF 300
    SetStage 00021BEF 500
    SetStage 00021BEF 1000

00017CE8 	Further Into the Unknown	

    SetStage 00017CE8 10
    SetStage 00017CE8 20
    SetStage 00017CE8 30
    SetStage 00017CE8 40
    SetStage 00017CE8 100
    SetStage 00017CE8 110
    SetStage 00017CE8 1000

001B41D1 	Short Sighted	

    SetStage 001B41D1 10
    SetStage 001B41D1 20
    SetStage 001B41D1 100
    SetStage 001B41D1 1000

00017CE7 	No Sudden Moves	

    SetStage 00017CE7 10
    SetStage 00017CE7 20
    SetStage 00017CE7 30
    SetStage 00017CE7 50
    SetStage 00017CE7 60
    SetStage 00017CE7 80
    SetStage 00017CE7 235
    SetStage 00017CE7 236
    SetStage 00017CE7 260
    SetStage 00017CE7 280
    SetStage 00017CE7 310
    SetStage 00017CE7 500
    SetStage 00017CE7 1000

002C6D74 	High Price to Pay	

    SetStage 002C6D74 10
    SetStage 002C6D74 70
    SetStage 002C6D74 100
    SetStage 002C6D74 110
    SetStage 002C6D74 135
    SetStage 002C6D74 170
    SetStage 002C6D74 200
    SetStage 002C6D74 390
    SetStage 002C6D74 480
    SetStage 002C6D74 510
    SetStage 002C6D74 620
    SetStage 002C6D74 1000

002583F2 	Unity	

    SetStage 002583F2 0
    SetStage 002583F2 1
    SetStage 002583F2 10
    SetStage 002583F2 300
    SetStage 002583F2 400
    SetStage 002583F2 600
    SetStage 002583F2 670
    SetStage 002583F2 680
    SetStage 002583F2 681
    SetStage 002583F2 800
    SetStage 002583F2 900
    SetStage 002583F2 2000

002B1B8E 	In Their Footsteps	

    SetStage 002B1B8E 0
    SetStage 002B1B8E 10
    SetStage 002B1B8E 20
    SetStage 002B1B8E 30
    SetStage 002B1B8E 500
    SetStage 002B1B8E 520
    SetStage 002B1B8E 530
    SetStage 002B1B8E 910
    SetStage 002B1B8E 1000

002BACF9 	Missed Beyond Measure	

    SetStage 002BACF9 1
    SetStage 002BACF9 10
    SetStage 002BACF9 15
    SetStage 002BACF9 200
    SetStage 002BACF9 500
    SetStage 002BACF9 1000

002A8001 	Unearthed	

    SetStage 002A8001 10
    SetStage 002A8001 50
    SetStage 002A8001 130
    SetStage 002A8001 150
    SetStage 002A8001 160
    SetStage 002A8001 300
    SetStage 002A8001 400
    SetStage 002A8001 500
    SetStage 002A8001 900
    SetStage 002A8001 1000

00256B02 	Final Glimpses	

    SetStage 00256B02 10
    SetStage 00256B02 15
    SetStage 00256B02 20
    SetStage 00256B02 30
    SetStage 00256B02 35
    SetStage 00256B02 40

00257DE1 	Entangled	

    SetStage 00257DE1 1
    SetStage 00257DE1 105
    SetStage 00257DE1 120
    SetStage 00257DE1 150
    SetStage 00257DE1 500
    SetStage 00257DE1 570
    SetStage 00257DE1 600
    SetStage 00257DE1 730
    SetStage 00257DE1 1000

0018AE76 	Revelation	

    SetStage 0018AE76 10
    Select One:
    SetStage 0018AE76 20 - Hunter Enemy
    SetStage 0018AE76 21 - Emissary Enemy
    SetStage 0018AE76 22 - Emissary and Hunter Enemy
    SetStage 0018AE76 100
    SetStage 0018AE76 200
    SetStage 0018AE76 1000
    SetStage 0018AE76 2000

0024EF9C 	One Giant Leap	

    SetStage 0024EF9C 01
    SetStage 0024EF9C 02
    SetStage 0024EF9C 03
    SetStage 0024EF9C 10
    SetStage 0024EF9C 30
    SetStage 0024EF9C 50
    SetStage 0024EF9C 200
    SetStage 0024EF9C 205 - May also need to use "movetoqt 0024EF9C" command.
    SetStage 0024EF9C 300
    SetStage 0024EF9C 1000
-------------------------------------------------------
#Shipyard parts
Instructions:
Go to a Ship Services Technician
Open console (~)
Click on the NPC to see the reference ID
Enter any of these codes into the console while Ref ID is up
Go into ship builder and you should have the items

Basic:
addkeyword 1453aa
addkeyword 1453b4

Corpo:
addkeyword 271d1
addkeyword 1453c1
addkeyword 271d6
addkeyword 271c7
addkeyword 1453c0
addkeyword 271bf
addkeyword 1453bf
addkeyword 271cc
addkeyword 271d0
addkeyword 1453c4
addkeyword 271d5
addkeyword 271c5
addkeyword 1453c3
addkeyword 271be
addkeyword 1453c2
addkeyword 271cb
addkeyword 271cf
addkeyword 1453b9
addkeyword 271d4
addkeyword 271c2
addkeyword 1453b7
addkeyword 1453b8
addkeyword 271bb
addkeyword 1453ba
addkeyword 271ca
addkeyword 271ce
addkeyword 1453be
addkeyword 271d3
addkeyword 1453bb
addkeyword 271c1
addkeyword 1453bd
addkeyword 271bd
addkeyword 1453bc
addkeyword 271c9
addkeyword 271cd
addkeyword 1453c6
addkeyword 271d2
addkeyword 271c0
addkeyword 1453c5
addkeyword 271bc
addkeyword 1453c7
addkeyword 271c8

Deimos:
addkeyword 271cd
addkeyword 1453c6
addkeyword 271d2
addkeyword 271c0
addkeyword 1453c5
addkeyword 271bc
addkeyword 1453c7
addkeyword 271c8

Hope tech:
addkeyword 271ce
addkeyword 1453be
addkeyword 271d3
addkeyword 1453bb
addkeyword 271c1
addkeyword 1453bd
addkeyword 271bd
addkeyword 1453bc
addkeyword 271c9

Nova:
addkeyword 271cf
addkeyword 1453b9
addkeyword 271d4
addkeyword 271c2
addkeyword 1453b7
addkeyword 1453b8
addkeyword 271bb
addkeyword 1453ba
addkeyword 271ca

Pirate:
addkeyword 143ca0
addkeyword 10c4ab

Stroud:
addkeyword 271d0
addkeyword 1453c4
addkeyword 271d5
addkeyword 271c5
addkeyword 1453c3
addkeyword 271be
addkeyword 1453c2
addkeyword 271cb

Taiyo:
addkeyword 271d1
addkeyword 1453c1
addkeyword 271d6
addkeyword 271c7
addkeyword 1453c0
addkeyword 271bf
addkeyword 1453bf
addkeyword 271cc

Space station:
addkeyword 1d2072
-------------------------------------------------------
#Easy Lockpicking(Copy all and paste into console)

setgs uSecurityKeyMinSizeNovice 1
setgs uSecurityKeyMinSizeAverage 1
setgs uSecurityKeyMinSizeHard 1
setgs uSecurityKeyMinSizeVeryHard 1
setgs uSecurityKeyMaxSizeNovice 1
setgs uSecurityKeyMaxSizeAverage 1
setgs uSecurityKeyMaxSizeHard 1
setgs uSecurityKeyMaxSizeVeryHard 1
setgs uSecurityMaxKeysNovice 2
setgs uSecurityMaxKeysAverage 2
setgs uSecurityMaxKeysHard 2
setgs uSecurityMaxKeysVeryHard 2
setgs uSecurityMinKeysPerRingNovice 2
setgs uSecurityMinKeysPerRingAverage 2
setgs uSecurityMinKeysPerRingHard 2
setgs uSecurityMinKeysPerRingVeryHard 2
setgs uSecurityMaxKeysPerRingNovice 2
setgs uSecurityMaxKeysPerRingAverage 2
setgs uSecurityMaxKeysPerRingHard 2
setgs uSecurityMaxKeysPerRingVeryHard 2
setgs uSecurityPuzzleShapeCountNovice 1
setgs uSecurityPuzzleShapeCountAverage 1
setgs uSecurityPuzzleShapeCountHard 1
setgs uSecurityPuzzleShapeCountVeryHard 1
-------------------------------------------------------
#Spawn Enemies
Crimson Fleet:
player.placeatme 000BDA76 3		Crimson Fleet Crew
player.placeatme 00158938 3		Crimson Fleet Pirates
player.placeatme 000BDA7A 3		Crimson Fleet Pilots
player.placeatme 001336ED 3		Crimson Fleet Corsair
player.placeatme 001C224D 3		Crimson Fleet Marauder
player.placeatme 000BDA7C 3		Crimson Fleet Captain
player.placeatme 0000DB3A 3		Crimson Fleet Robot Model A
player.placeatme 000CA118 3		Crimson Fleet Robot Model S

Ecliptics:
player.placeatme 0018E458 3		Ecliptics
player.placeatme 00270280 3		Ecliptic Agent
player.placeatme 0027027E 3		Ecliptic Merc
player.placeatme 0027027F 3		Ecliptic Contradtor
player.placeatme 00270281 3		Ecliptic Operator
player.placeatme 00129584 3		Ecliptic Commandant
player.placeatme 00129585 3		Ecliptic Warmonger
player.placeatme 00129586 3		Ecliptic Executioner
player.placeatme 00129587 3		Ecliptic Specialist
player.placeatme 00184EF6 3		Ecliptic Robot Model S

Pirates:
player.placeatme 00010B2E 3		Pirates
player.placeatme 00010B38 3		Pirate Brigano
player.placeatme 00009CED 3		Pirate Freebooter
player.placeatme 00009CEE 3		Pirate Marauder
player.placeatme 00009CEF 3		Pirate Rover
player.placeatme 0012D02E 3		Pirate Legend
player.placeatme 0012D02F 3		Pirate Captain
player.placeatme 0012D030 3		Pirate Flayer
player.placeatme 0012D031 3		Pirate Cutthroat
player.placeatme 0012D032 3		Pirate Reaver
player.placeatme 0012D033 3		Pirate Plunderer
player.placeatme 0023591B 3		Pirate Leader

Spacers:
player.placeatme 00270255 3		Spacers
player.placeatme 00270254 3		Spacer Punk
player.placeatme 00270253 3		Spacer Troublemaker
player.placeatme 00270252 3		Spacer Scum
player.placeatme 0013A216 3		Spacer Captain
player.placeatme 00129580 3		Spacer Beast
player.placeatme 00129581 3		Spacer Savage
player.placeatme 00129582 3		Spacer Predator
player.placeatme 00129583 3		Spacer Vulture
player.placeatme 0012957E 3		Spacer Myth
player.placeatme 0012957F 3		Spacer Titan

Va`Runn:
player.placeatme 0027871E 3		Va`Runn Zealot
player.placeatme 0026FDB5 3		Va`Runn Robot Model A
player.placeatme 00297DD7 3		Va`Runn Robot Model S
-------------------------------------------------------
#Plushies

player.additem 81C 1       Cuddloasaur
player.additem 829 1       Xenosnuggle
player.additem 883 1       Starpal
player.additem 12DFFC 1    Parsecpooch
player.additem 12DFFD 1    Galacticat
player.additem 1401ee 1    My friend wilby(Green)
player.additem 17af77 1    My friend wilby(Blue)
player.additem 17af7c 1    My friend wilby(Red)
player.additem 17af7e 1    My friend wilby(Orange)
-------------------------------------------------------
#Magazines

Mining Monthly 
player.placeatme 20B4AC
player.placeatme 20B4AD
player.placeatme 20B4AE
player.placeatme 20B4AF
player.placeatme 20B4B0
player.placeatme 20B4B1
player.placeatme 20B4B2
player.placeatme 20B4B3
player.placeatme 20B4B4
player.placeatme 20B4B5

Peak Performance
player.placeatme 202D9A
player.placeatme 202D9B
player.placeatme 202D9C
player.placeatme 202D9D
player.placeatme 202D9E

Grunt Issue
player.placeatme 21B048
player.placeatme 21B049
player.placeatme 21B04A
player.placeatme 21B04B
player.placeatme 21B04C
player.placeatme 21B04D
player.placeatme 21B04E
player.placeatme 21B04F
player.placeatme 21B050
player.placeatme 21D05A

Nova Galactic Manuals
player.placeatme 2009AD
player.placeatme 2009AE
player.placeatme 2009AF
player.placeatme 2009B0
player.placeatme 2009B1
player.placeatme 2009B2
player.placeatme 2009B3
player.placeatme 2009B4
player.placeatme 2009B5
player.placeatme 2009B6

Constellation Guide
player.placeatme 208E8D
player.placeatme 208E8E
player.placeatme 208E8F
player.placeatme 208E90
player.placeatme 208E91

Freestar Captain's Log
player.placeatme 201BD3
player.placeatme 201BD4
player.placeatme 201BD5
player.placeatme 201BD6
player.placeatme 201BD7

Gunslinger's Guide
player.placeatme 20BB2C
player.placeatme 20BB2D
player.placeatme 20BB2E
player.placeatme 20BB2F
player.placeatme 20BB30

Combatech
player.placeatme 21293B
player.placeatme 21293C
player.placeatme 21293D
player.placeatme 21293E
player.placeatme 212940

UC Defense
player.placeatme 209FB6
player.placeatme 209FB7
player.placeatme 209FB8
player.placeatme 209FB9
player.placeatme 209FBA

Vanguard Space
player.placeatme 2009D4
player.placeatme 2009D5
player.placeatme 2009D6
player.placeatme 2009D7
player.placeatme 2009D8

Va'Ruun Scripture
player.placeatme 20A91B
player.placeatme 20A91C
player.placeatme 20A91D
player.placeatme 20A91E
player.placeatme 20A91F
player.placeatme 20A920
player.placeatme 20A921
player.placeatme 20A922
player.placeatme 20A923
player.placeatme 20A924

Cyber Runner's Cypher
player.placeatme 208D8A
player.placeatme 208D8B
player.placeatme 208D8C
player.placeatme 208D8D
player.placeatme 208D8E

Neon Nights
player.placeatme 200A84
player.placeatme 200A85
player.placeatme 200A86
player.placeatme 200A87
player.placeatme 200A88

The New Atlantian
player.placeatme 1FF722
player.placeatme 1FF723
player.placeatme 1FF724
player.placeatme 1FF725
player.placeatme 1FF726

Solomon's Adventures
player.placeatme 208D85
player.placeatme 208D86
player.placeatme 208D87
player.placeatme 208D88
player.placeatme 208D89

Tracker's Primer
player.placeatme 209097
player.placeatme 209098
player.placeatme 209099
player.placeatme 20909A
player.placeatme 20909B

Kryx's Journal Entrie
player.placeatme 20908F
player.placeatme 209090
player.placeatme 209091
player.placeatme 209092
player.placeatme 209093
-------------------------------------------------------
#Artifacts

player.placeatme 00216f9b  Alpha
player.placeatme 00216f99  Beta
player.placeatme 00216f98  Chi
player.placeatme 00216f97  Delta
player.placeatme 00216f96  Epsilon
player.placeatme 00216f95  Eta
player.placeatme 00216f94  Gamma
player.placeatme 00216f93  Iota
player.placeatme 00216f92  Kappa
player.placeatme 00216f91  Lambda
player.placeatme 00216f90  Mu
player.placeatme 00216f8f  Nu
player.placeatme 00216f8e  Omega
player.placeatme 00216f8d  Omicron
player.placeatme 00216f8c  Phi
player.placeatme 00216f8b  Pi
player.placeatme 00216f8a  Psi
player.placeatme 00216f89  Rho
player.placeatme 00216f88  Sigma
player.placeatme 00216f87  Tau
player.placeatme 00216f86  Theta
player.placeatme 00216f9c  Upsilon
player.placeatme 00216f85  Xi
player.placeatme 00216f9a  Zeta