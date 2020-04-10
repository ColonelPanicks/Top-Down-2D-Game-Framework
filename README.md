# Top Down 2D Game Framework

This repository contains progress on creating a framework for a top down 2D game.

![](preview/20200410.gif)

## Features

Currently, this is just a brain dump of all the features/things I want to have working in here before actually trying to develop something with substance.

- [x] Full Movement
- [x] Collision System
- [x] Camera Movement (follow player)
- [ ] Scene Transitioning (doors to buildings, etc)
- [ ] NPCs/Conversation
- [ ] Inventory System (not looking forward to this, gonna be a biggie)
- [ ] Character Customisation
- [ ] Menu System
- [ ] Save States
- [ ] Anything Else I Bloody Well Feel Like Adding

## Thoughts/Things to Change

- The camera movement currently uses the bounds of a large Box Collider on the world, this feels clunky and leads to phantom collisions as anything inside the box is technically colliding with it. Change this to something else, perhaps intelligently working out the bounds of the sprites on the edge layer?
- Instead of manually setting the position to move players to for building/scene transitions, instead store some sort of global variable that has the "last used" door/movement location. This objects co-ordinates can then be used for spawning the player back to the original point.
- Due to the starting scene having a player in it, there's a duplication glitch when returning to the original map. This can be addressed by (after adding some sort of global controller above) having some check for an existing player and spawning in if not present (this should spawn a player on first load of the game and then never again as we simply move the game object around).

## Credit

### Assets

Character: ["Sharm's Tiny 16 Character Sprites - Expanded" by Sharm, withthelove and Evert](https://opengameart.org/content/tiny-16-expanded-character-sprites)

World Assets: ["Roguelike pack" by Kenney Vleugels for Kenney](https://www.kenney.nl/assets/roguelike-rpg-pack) 

### Tutorials/Assistance

This wouldn't have been possible for me to learn without the help of the incredible tutorial series by CouchFerret, [available here](https://www.youtube.com/playlist?list=PLM83Z6G5iM3k48356VU6e-oXWl_uwwq4F).

Also, big thanks to [DuckDuckGo](https://duckduckgo.com/) and the general existence of the Internet.
