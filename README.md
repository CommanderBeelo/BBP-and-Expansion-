# BBP-and-Expansion-
Steps for setting up your DayZ server with Expansion and Base Building Plus. We Will not be using Breaching Charge or the standalone Code lock mod, instead we will be using the Expansion options for both. 

## Step 1 - Install Expansion

If you have not already done so, install Expansion on your server. 

Their Wiki is here: https://github.com/salutesh/DayZ-Expansion-Scripts/wiki

Their Mission Files are Here: https://github.com/ExpansionModTeam/DayZ-Expansion-Missions

Add The CodeLock bridge mod by Lava, https://steamcommunity.com/sharedfiles/filedetails/?id=2746483592 this will allow you to use Expansion CodeLocks on BaseBuildingPlus.

## Step 2 - Configure Expansion

There are a couple of Expansion settings you will want to address before we get to far involved. The first one is in profiles/expansionmod/settings and that will be RaidSettings.json. Here you can set up your raid tools for safes and code locks, as we will be using Expansion Code locks for everything. I have included an example from my server

The other Settings we are going to look at are in mpmission/mapname/expansion/settings. We are going to open up BaseBuilding.json. You can set these up however you like except for ""CodelockAttachMode": 2,". you want this set to 2, so it will attach to everything with a codelock slot. All the other settings are up to you. I have included an example from my server as well. 

## Step 3 - Install BaseBuildingPlus

Install BBP, add the types to your economy core, set up their settings however you see fit, we will be skipping breaching charges for my tutorial here, so the config that the mod comes with will work for our scenario. I have again included my settings as an example from my server.

The BBP wiki - https://github.com/FelixForesight2020/BaseBuildingPlus/wiki

## Step 4 - Fix the Hologram placement issue 

There are two options, both work

Option 1 - use the hologram fix 1.19 mod on the workshop - https://steamcommunity.com/sharedfiles/filedetails/?id=2878310242

Option 2 - Use cfggameplay and enable ""disableIsCollidingBBoxCheck": 1," - https://community.bistudio.com/wiki/DayZ:Gameplay_Settings or read the mod descrption in option 1. 

I am using option 2 and have included my cfggameplay.json as an example. bear in mind I run a namalsk server, so temps and lighting may need adjusted for your use case.

## Step 4 - Add the bbp_vanilla_dmg pbo 

This step you may need to learn on youtube on how to pack up server mods. I have provided the code for the cpp, you just need to pack it up and add it to your server mod, or adjust as you see fit. 

I was going for 1 Satchel charger per Tier. You can adjust to your liking. You can find other damage pbos in the BaseBuildingPlus Discord.

## Discord Links

The Horror At Namalsk (My Discord) - https://discord.gg/TdhaZ6TtuT

Expansion Discord - https://discord.gg/rMZuS4F

BaseBuildingPlus - https://discord.com/invite/TuwgjqK
