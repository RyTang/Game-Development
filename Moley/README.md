# Moley

[Moley Starting Picture]()

Project Timeline( Jan 2021 - Current) 

Updates will made along the way. Tune in from time to time if you want to.

Hi, welcome to the Moley Project. Under this all are all different aspects of the game that I thought was worth mentioning. Feel free to go through any of the parts of the project you might be interested in.

## Table of Contents:
1. [Motive behind Game](#reasoning-behind-the-game)
1. [Player Controls](#player-controls)
1. [How Map Generation Works](#map-generation)




## Reasoning Behind the Game


## Player Controls


## Map Generation

<p align="center">

<img src="https://github.com/RyTang/Game-Development/blob/main/Moley/Images/4x4Layout.JPG" width="500" height="500"/>

</p>


So currently the game follows a very similar construct to Spelunky. Each level is divided into 4x4 cube size rooms (That's 16 rooms if you needed help counting). Each room has a current dimension of 10x10 blocks. The Level Generation controller begins with one of the topmost Rooms being randomly selected as the starting room, this is marked as where the player will begin. Then at that spot a random room template will be selected and spawned. After spawning, it'll then randomly choose one of the adjacent rooms to move to and built another room with connecting entrances. It'll repeats the steps with each having a chance to go one row downwards, if it hits the side of the map border or an already built room it'll built downwards instead. This will continue until it reaches one of the bottommost rooms and that will be marked as the final room, where the exit will then spawn.  Then any of the 16 rooms that aren't currently filled will select a random room template to spawn, these rooms do not need to connect to the original rooms as they are just used to fill up the remaining space. This is also when the Level Generation Control might spawn Special rooms (currently not added in the game yet) in the map.

So carrying on, after each room have been decided. Each block on the map will then generate according to the rooms selected. Each block will have a chance to spawn a special block depending on their individual chances. (I'll have to adjust parts of this to ensure that it scales with game difficulty). Furthermore monsters will also have a chance to spawn in each room. 
