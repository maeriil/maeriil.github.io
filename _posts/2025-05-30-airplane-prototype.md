---
title: "Top-down Airplane Shooter"
date: 2025-05-30
categories: [portfolio]
tags: [game, airplane]
---
### Overview
This was a simple game I created in the January 2025. The premise of the game is very simple; play as an airplane and shoot other planes. There are boms scattered around the map which when shot, will explode. There are few other orbs scattered in the map like Health Orb, Shield orb and etc., but at this moment, only the Health orbs are working. When shooting a bomb, it will deal an explosion which will continously decrease all players health within the radius and lasts for around two to three seconds.

![alt text](/assets/airplane-prototype-base.png)

### Major systems / Features
1. Airplane movement
2. Top Down Camera movement
3. Camera shake effect
4. Explosion effect
5. Hit detection with Projectiles

### Review
The game was created using Jecs and used roblox-ts. Looking back, the code for the game wasn't that great. There were many components that weren't normalized well, and I would definitely do it a bit different now compared to others.

For starters, the spawning orbs system is not really that great. It only randomly generates some on positions. We can make this much better by splitting the map into small chunks of grids, and spawning orbs on each grid using some percent chances.

The weather system was also pretty bad. While it does work, it doesn't look that great. Since building isn't my strong suit, I should have instead used blocky clouds rather than trying to use a cloud mesh. Finally the cloud movement and spawning was a bit weird. Currently it spawns them all from on specific starting location always, and it slides along the `Z` axis always. This isn't that great...

All in all though, I still it was a decently good learning experience. I still believe with right approach, this game has good potential. I do however think most games that doesn't use default roblox character doesn't do too great in ROBLOX. Maybe I am wrong, so I think I will pursue it later on.

The game link can be found [here, Airplane Prototype](https://www.roblox.com/games/73743307705652/Airplane-Prototype).
