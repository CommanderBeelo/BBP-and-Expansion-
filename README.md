# BBP-and-Expansion-
Steps for setting up your DayZ server with Expansion and Base Building Plus. We Will not be using Breaching Charge or the standalone Code lock mod, instead we will be using the Expansion options for both. I do not see anthing stopping you from using either mod, it just adds more configuration complexity having 3 or 4 different settings files for raiding. I am lazy, and would rather have one spot to adjust things.

## Step 1 - Install Expansion

If you have not already done so, install Expansion on your server. I am running bundle. This same guide would work if you just have Expansion BaseBuilding. 

Their Wiki is here: https://github.com/salutesh/DayZ-Expansion-Scripts/wiki

Their Mission Files are Here: https://github.com/ExpansionModTeam/DayZ-Expansion-Missions

Add The CodeLock bridge mod by Lava, https://steamcommunity.com/sharedfiles/filedetails/?id=2746483592 this will allow you to use Expansion CodeLocks on BaseBuildingPlus.

## Step 2 - Configure Expansion

There are a couple of Expansion settings you will want to address before we get to far involved. The first one is in profiles/expansionmod/settings and that will be RaidSettings.json. Here you can set up your raid tools for safes and code locks, as we will be using Expansion Code locks for everything. I have included an example from my server

The other Settings we are going to look at are in mpmission/mapname/expansion/settings. We are going to open up BaseBuilding.json. You can set these up however you like except for ""CodelockAttachMode": 2,". you want this set to 2, so it will attach to everything with a codelock slot. All the other settings are up to you. I have included an example from my server as well. 

## Step 3 - Install BaseBuildingPlus

Install BBP, add the types to your economy core, set up their settings however you see fit, we will be skipping breaching charges for my tutorial here, so the config that the mod comes with will work for our scenario. I have again included my settings as an example from my server. You do not need to install the stand alone code lock mod. The bridge mod we installed in step 1 will fill BBPs dependency on CodeLock. 

The BBP wiki - https://gitlab.com/basebuildingplus/bbp-wiki/-/wikis/home

## Step 4 - Fix the Hologram placement issue 

There are two options, both work, do which ever you see fit. Option 2 gives you some other tuneability options on your sever. 

Option 1  - use the hologram fix 1.19 mod on the workshop - https://steamcommunity.com/sharedfiles/filedetails/?id=2878310242

Option 2 - Use cfggameplay and enable ""disableIsCollidingBBoxCheck": 1," - https://community.bistudio.com/wiki/DayZ:Gameplay_Settings or read the mod descrption in option 1. 

I am using option 2 and have included my cfggameplay.json as an example. bear in mind I run a namalsk server, so temps and lighting may need adjusted for your use case.

## Step 4 - Add the bbp_vanilla_dmg pbo 

This step you may need to learn on youtube on how to pack up server mods. I have provided the code for the cpp (obtained from the BBP Discord), you just need to pack it up and add it to your server mod, or adjust as you see fit. You can find this and other damage pbos in the BaseBuildingPlus Discord, such as vanilal dmaage to just doors only. 

I was going for 1 Satchel charger per Tier. You can adjust to your liking. 

## Step  - Expansion Market Category 

I have also included an Expansion Market file. This goes into profiles/Expansionmod/Market. You can then link the json to a trader in profiles/expansionmod/traders in the categories section. Note this file only includes the Workbench, Tools, and flair items, all other kits are not listed, as they can be crafted and theres no point in adding the kits to the trader if you're going to use the workbench, just craft the kits. Heres a quick video on the Expansion Market if you are not familiar - https://www.youtube.com/watch?v=q7sahJJMdDU

## Discord Links

The Horror At Namalsk (My Discord) - https://discord.gg/TdhaZ6TtuT

Expansion Discord - https://discord.gg/rMZuS4F

BaseBuildingPlus - https://discord.com/invite/TuwgjqK

# KNOWN ISSUES

Regaurdless of Expansion settings, you can place kits in other peoples territory's. It will only let you place the hologram, it will not let you build. To advoid people abusing this to trap people in holograms in their own bases, thurn hologram collision off in BBP settings. ""BBP_HologramHasCollision": 0,"
