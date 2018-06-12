# 42 Academy+Plus - filler

A 42 (school) project that required us to create a player program to compete against other students on the famous (or not) Filler board. The principle is simple: two players take on each other on a board, and take turns placing the piece that the master of the game (supplied in the form of a Ruby executable) gives them, earning points. The game stops as soon as a piece can no longer be placed. Little playful project!

For more details regarding the project see 'ft_printf - Subject(EN).pdf'

## How to use

Using a terminal from within the /filler directory:
- run `make` to generate the **filler** binary
- open the `resources` folder to find the binary that runs the game as `filler_vm`
- `maps` and `players` contain maps that you can play on and a set of players you can play against (your player was required to win against all of them in order to receive the maximum grade for the project)
- to start a game use the following command:
  - `./filler_vm -f *path_to_a_map* -p1 ./*path_to_a_player* -p2 ./*path_to_another_player*`
- use the binary you created as path to one of the two players and play against any of the other provided players (or against yourself)

./filler_vm will output every turn of the game in your terminal which might be difficult to watch due to the speed data is spewed on the screen with. To fix that the project required us to create a **graphics visualizer** as a bonus.

## Terminal output:

```
$>./filler_vm -f map -p1 user1 -p2 user2
# -------------- VM  version 1.1 ------------- #
#                                              #
# 42 / filler VM Developped by: Hcao - Abanlin #
#                                              #
# -------------------------------------------- #
launched user1
$$$ exec p1 : [user1]
launched user2
$$$ exec p2 : [user2]
Plateau 14 30:
012345678901234567890123456789
000 ..............................
001 ..............................
002 ..............................
003 ..............................
004 ......X.......................
005 ..............................
006 ..............................
007 ..........................O...
008 ..............................
009 ..............................
010 ..............................
011 ..............................
012 ..............................
013 ..............................
Piece 3 6:
.****.
**....
*.....
<got (O): [7 24]
Plateau 14 30:
012345678901234567890123456789
000 ..............................
001 ..............................
002 ..............................
003 ..............................
004 ......X.......................
005 ..............................
006 ..............................
007 .........................oooo.
008 ........................oo....
009 ........................o.....
010 ..............................
011 ..............................
012 ..............................
013 ..............................
Piece 3 8:
......*.
......**
.......*
<got (X): [4 0]
Plateau 14 30:
012345678901234567890123456789
000 ..............................
001 ..............................
002 ..............................
003 ..............................
004 ......x.......................
005 ......xx......................
006 .......x......................
007 .........................OOOO.
008 ........................OO....
009 ........................O.....
010 ..............................
011 ..............................
012 ..............................
013 ..............................
[...]
== O fin: 168
== X fin: 175
```
# Graphics visualizer

In order to create a graphics visualizer that is capable of visualizing a filler match I've used School 42's minilibx that is also provided inside this repository.

## How to use

Using a terminal from within the /filler/visualizer directory:
- run `make -C minilibx_macos` to create the library **libmlx.a** (or skip this step and use the library provided inside minilibx_macos directory)
- run `make` to generate the **visualizer** binary
- rerun the filler game using the following commnd:
  - `./filler_vm -f *path_to_a_map* -p1 ./*path_to_a_player* -p2 ./*path_to_another_player* | ./*path_to_visualizer*`
  
## Visualizer demo:

![demo](https://github.com/Gabriel-Em/42_AcademyPlus---filler---/blob/master/filler/resources/demo.gif)
