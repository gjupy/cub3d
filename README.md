# cub3d
### My first RayCaster with the MLX42 lib.<br>
This project is inspired by the world-famous Wolfenstein 3D game, which was the first FPS ever. The goal was to make a dynamic view inside a maze.<br>

### from [@chris-bbrs](https://github.com/chris-bbrs) and [@gjupy](https://github.com/gjupy)<br>

## Our cub3d
### Requirements to run the game
only tested on **macOS Catalina (Version 10.15.7)**<br>
For all other OS it is not guaranteed to work.<br>
OpenGL and AppKit is required to run it.<br>
If you want to run it on Linux [here](https://harm-smits.github.io/42docs/libs/minilibx/getting_started.html#compilation-on-linux) is a tutorial that might help and [here](https://github.com/42Paris/minilibx-linux) is the required version of miniLibX, this is **not tested** with our cub3D.<br>
### How to cub3D
1. run `make` in the root of the directory
2. run `./cub3D maps/42.cub` in the root of the directory
3. move the character with `WASD`
4. turn the FOV left and right by pressing `arrow_left` and `arrow_right` or by moving the mouse right or left

### Map requirements
- decide which texture is displayed on which side
- `0` define walkable spaces
- `1` define walls
- `2` define doors
- the players position is displayed by:
  - `N` player is facing north (top of the 2D map)
  - `E` player is facing east (right side of the 2D map)
  - `S` player is facing south (bottom of the 2D map)
  - `W` player us facing west (left side of the 2D map)
- the map has to be enclosed by walls on all sides
- doors have to have walls on two opposite sides
- any other characters other than the ones above are forbidden
- if there is a ` `(space)&nbsp;inside the map it has to be enclosed by walls, as you can see [here](https://github.com/vytkuklys/42_cub3d/blob/main/maps/biggy.cub)
- only one player position is allowed
- you have to set all the textures that should be used as wall texture i.e.
  - `NO ./textures/path_to_the_north_texture/wall_text.png`
  - `SO ./textures/path_to_the_south_texture/wall_text.png`
  - `WE ./textures/path_to_the_west_texture/wall_text.png`
  - `EA ./textures/path_to_the_east_texture/wall_text.png`
- you have to set the ceiling color, i.e.:
  - `C 0, 183, 183`
- you have to set the floor color, i.e.:
  - `F 141, 1, 126`
