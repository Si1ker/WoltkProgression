# Patch 3.0

### Summary:
- New continent: Northrend
- New dungeons: Violet Hold - Utgarde Pinnacle - Utgarde Keep - The Nexus - The Oculus - The Culling of Stratholme - Halls of Stone - Halls of Lightning - Gundrak - Drak'Tharon Keep - Azjol-Nerub - Ahn'kahet
- Max level incresed to 80
- New class: Death Knights
- New Raids: Naxxaramas - Eye of Eternity - Obsidian Sanctum - Obsidian Sanctum - Vault of Archavon: Archavon
- New arenas: Dalaran Arena - The Circle of Valor
- Arena Season 5: Savage - Hateful - Deadly

### Steps:

1 - Apply the changes as shown in [SapphironPortal](https://github.com/Si1ker/WoltkProgression/tree/main/patch%203.0/SapphironPortal)

2 - Place [keep-out-argent](https://github.com/Si1ker/WoltkProgression/tree/main/patch%203.0/keep-out-argent) under the ```modules``` folder of your core source folder

3 - Apply [set version](https://github.com/Si1ker/WoltkProgression/blob/0de5dcc6809d9aeb92ab1e750bf763a863820c00/patch%203.0/set%20version.sql) into your world table

4 - Under your [worldserver.conf.](https://github.com/azerothcore/azerothcore-wotlk/blob/81301c67d95a1e51bd269e8f4a49f373ecefeb42/src/server/worldserver/worldserver.conf.dist) perform the following changes:

a - Change [Arena.ArenaSeason.ID](https://github.com/azerothcore/azerothcore-wotlk/blob/master/src/server/worldserver/worldserver.conf.dist#L3019) to ```Arena.ArenaSeason.ID = 5```

b - Change [DungeonFinder.OptionsMask](https://github.com/azerothcore/azerothcore-wotlk/blob/master/src/server/worldserver/worldserver.conf.dist#L1544) to ```DungeonFinder.OptionsMask = 0```

c - Change [MinDualSpecLevel](https://github.com/azerothcore/azerothcore-wotlk/blob/master/src/server/worldserver/worldserver.conf.dist#L1117) to ```MinDualSpecLevel = 81```


5 - Re-run Cmake, compile and start your server

