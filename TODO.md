DONE:
key mechanics:
* game ends when moves are depleted
* time turners
  * managing state
    * player location
    * item and animal locations
    * inventory and points
    * fov
* items
* camera
  * `fixedToCamera` UI text

TODO:
key mechanics:
* story elements
  * make the lose text more lose-y (you move on to the next planet)
* visual inventory
* fov and resetting its state
* win condition
* bugs:
  * when you travel in time, if you land on an item, you should claim it


          winMsg = this.game.add.bitmapText(game.width / 2, game.height / 2, 'minecraftia', "Victory!\nPress Space or Click to Continue.", 24);
          winMsg.tint = 0x00ff00;
          winMsg.anchor.setTo(0.5);
          winMsg.fixedToCamera = true;


sound effects
loading graphic (at least remove current one)
remove level code
time travel item and specimens
state (for time turner)
change the page name
favicon
camera follow

fov
kenney fonts
time turner animation
player

1
  animal
    possibly too cute
  archive -> roguelike
    tiny plants and backgrounds
  background
    some trees and cacti
  game icons
    star and medals
  jumper
    some cute (not too cute) animals and some small plants
  onscreen controls
    for mobile
  platform -> base
    some cute animals (and alien heads)
    springy platform and lever that could work for time turner
    numbers
  platform -> building
    clock for time turner
  platform -> extra animations
    several cute animals (not too cute)
  ice pack
    backgrounds, one snowy tree
  mushroom pack
  request pack
    some sparkles that might be nice for time turner animation
  platformer pack redux
    possibly some animals not in other packs
  roguelike
    tiny backgrounds
  rpg
    backgrounds, trees
  shooting gallery
    ducks
    oddly, the backgrounds could work
  voxel pack
    maybe the best backgrounds
    a couple animals
2 -> 2D
  abstract platformer -> other
    bunch of plants
  fish plant
    fish and plants
  foliage
    plants
  platformer pack nautical
    aquatic plants & wildlife
  RTS Sci-fi
    a couple plants
  Sokoban pack
    marioish sprite character
  Topdown shooter
    top-down sprite dudes
  tower defense
    backgrounds
3 -> 2D
  animal pack redux
    possibly too-cute animals
  interface
    inventory slots, achievement banners, minimap
  pattern pack
    combine with backgrounds to texture them
  ranks pack
    ranks
  rpg block pack
    a few trees
  voxel expansion pack
    some plants and backgrounds
    shield that might work as a time turner


if you find a time travel object, you can go back n moves and restart from that point (basically it needs to always hold a copy of the game state from n moves ago (but obviously you don't get to keep the time travel object, if you had it n moves ago))


add all actors to the actorList (or similar) and never remove them
store the position and id of each actor at each save point
upon restore, loop through the actorList and place any that is in the array of position/id for the save point
  (see play.loadActors for how to place)
