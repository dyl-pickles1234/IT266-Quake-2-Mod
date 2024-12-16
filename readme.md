# Quake 2 Mod
This is a mod for NJIT's IT266 Game Mod Development course. This code is a Quake 2 mod for my final assignment submission (Fall 2024).
## Celeste in 3D
This mod consists of world interactables, various collectibles and powerups, custom enemies, all new movement mechanics, and a speedrun mode, all inspired by the 2D platformer Celeste.
### Features
- World interactables
  - spikes
  - all platforms only move on dash
  - Springboards
  - Bubbles
- Collectibles/powerups
  - strawberries
  - dash crystal
  - double dash for short time
  - Feather
  - Freeze crystal
- Modified enemy types
  - dash monster
  - Badeline (chasing enemy)
  - A boss you need to dash into to do damage
  - Enemy that summons spikes below you
- Speedrun mode
  - Collect all spawned strawberries
  - In deathmatch map 1
  - Saves fastest time to file
- 5 movement abilities
  - Dash
  - Walljump
  - Wallclimb
  - Wavedash
  - Fast fall

## How To Play
Run Quake 2. If using my shortcut, skip to the next step. Press the `~` key to open the console, then type `set game mod`.

Start a new game, load a save, or use the `map` command to load a specific map.

You may need to bind a couple new controls to get all the features out of this mod. The new commands are `dash` and `+climb`.

> I recommend `bind f dash` and `bind ctrl +climb`

Use your `dash` bind to dash, `+climb` bind to grab onto walls, jump bind to perform a walljump, and crouch bind to fastfall. Check in-game help (`celestehelp`) to have this (and more) info while playing.

### Help info:
Try `celestehelp <category>` for more specific help on each group of features (`<category>` can be movement, objects, items, enemies, or speedrun).

#### Movement (player movement mechanics)
The dash! A simple boost along the direction you're looking in for a short time. You only get one, but it replenishes when you stand on the ground or touch some other objects (check out the items section).

Wallclimbing allows you to grip onto a nearby wall you're looking at while holding the climb key. You can use your regular movement keys to crawl up and around the wall you're attached to. Careful, climbing a wall takes up stamina, and if you run out, you can't grab walls! Stamina can be restored by some of the same ways you regain your dashes.

Working off of that, you can press your jump key to perform a walljump, which boosts you upwards and away from the wall you were just climbing. Jumping also takes up a good amount of your stamina, so you can't just walljump anywhere.

Wavedashing is a technique that allows a player to gain lots of speed quickly. By dashing diagonally forward and down into a floor, you can press jump just before touching the ground to get a boost and carry your dash momentum.

Fastfalling is good for getting to the ground quickly. Hold the crouch key to fall faster than you normally would.

> The controls for these mechanics are customizable. You can bind `dash` and `+climb` to any key you'd like, the walljump is based on your regular jump key, and fast fall is based on your crouch key.

#### Objects (world interactables)
Spikes kill! If a player touches a spike, they will die and have to respawn. Spikes spawned via command will be dangerous immediately, but spikes summoned by a custom enemy are a bit different (check out the enemies section).

Moving platforms are no longer activated by a player stepping on them. Instead, a player must use a dash to activate all platforms in the map. They also move much faster.

Springboards bounce the player into the air when touched, and also resets stamina and replenishes your dashes.

Dash buubbles capture the player inside of them for a half second, allowing you to look around while stuck in place. After the short delay is over, you are launched in the direction you are looking with reset stamina and replenished dashes.

> Spikes, springboards, and dash bubbles can be spawned via the console by typing `spawn func_<spike | spring | dash_bubble>`.

#### Items (collectibles/powerups)
Dash crystals allow you to regain 1 dash when you touch them. If you grab one midair, you have an opportunity to dash again. It also resets stamina, and respawns a short time after you pick it up.

Double dash crystals allow you to temporarily dash twice in the air before needing to replenish. This lasts a short time, and when it wears off, you'll only be able to dash once. These also reset stamina and respawn a few seconds after the effect wears off.

The feather allows you to continuously move in the directions you're looking in for a short time. It is slower than a dash, but lasts longer and can give you much more control. Again, it resets stamina and respawns after it wears off.

Freeze crystals stop enemies and pause the world for a short time after you collect one. You can still deal damage and navigate around.

Strawberries are a collectible item for fun points, but come into play more during the speedrun mode. In general, strawberries are bonuses to see how many you can collect.

> These items can be spawned via the console by typing `spawn item_<dash_crystal | double_dash_crystal | feather | freeze_crystal | strawberry>`.

#### Enemies (modifed/custom enemy types)
Dash monsters (flyer) only move periodically, turning to face the player for a half second before dashing quickly towards them. They rest for a short time before repeating. A player can bounce on a dash monster's head and immobalize it for 5 seconds.  If they touch you, you die.

The chase monster (also called Badeline) ((also also called chick)) mimics the player's movement, lagging behind by only a few seconds. If they touch you, you die.

A boss fight exists, replacing the Quake boss2 with one that is invulnerable to gun/explosive/all other damage and can only be defeated by dashing directly into it 5 times. The player is launched backwards each hit.

The summoner (gunner) enemy has no gun, but instead spawns dangerous spikes under the player's feet, but these spikes have a small cooldown. They appear first as a warning, then become deadly a second later.

> These enemies can be spawned via the console by typing `spawn monster_<flyer | chick | boss2 | gunner>`.

#### Speedrun mode (in deathmatch map 1)
Strawberries are strewn about in predetermined locations around the map. Go as fast as you can to collect all 13 and you will be presented with your final time.

If it's a new record, it gets saved to a file and is persistent between game launches. If it's not a new record, try again! It won't be saved.

> This map can be accessed via the console by typing `map q2dm1`.
