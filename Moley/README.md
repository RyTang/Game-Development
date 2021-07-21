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

**This is Nerd Talk Territory if you're interested in the general gist of how Map Generation works in this game**

<p align="center">

<img src="https://github.com/RyTang/Game-Development/blob/main/Moley/Images/4x4Layout.JPG" width="500" height="500"/>

<b>General 4x4 Layout of the Game's Map</b>
</p>



So currently the game follows a very similar construct to Spelunky. Each level is divided into 4x4 cube size rooms (That's 16 rooms if you needed help counting). Each room has a current dimension of 10x10 blocks. 
There is a controller that takes care of the whole level generation. It starts by randomly selecting one of the topmost rooms as the starting room; this is where the player will begin. The controller has access to several room templates of varying entrances. It will then randomly choose one as the starting room, furthermore, it will then randomly choose a direction from left, right and down to move to. It will then move in that direction. It'll then repeat this process trying to build a connecting path to one of the bottommost rooms, which will be declared as the exit room. The exit will spawn in this room. Along the way, if the controller happens to bump to the boundaries or an existing rooms it'll move downwards instead. There are other factors that are considered but they won't be mentioned here, as it can get quite messy. After the pathway is constructed, the controller then signals to the blocks of rooms unfilled to go choose a random from the templates without regards to whether or not the paths are connecting. This is also when the controller might decide to spawn Special rooms (currently not added in the game yet) in the map.

So carrying on, after each room have been decided. Each block on the map will then be allowed change according to their surroundings. Each block will then a chance to spawn a special block depending on their individual chances. Furthermore monsters will also have a chance to spawn in each room depending on location or room they're in. 

Below are illustrations of how it might look:

<p align="center">

<img src="https://github.com/RyTang/Game-Development/blob/main/Moley/Images/Path_Generation.JPG" width="500" height="500"/>

</p>

<p align="center">
<b>Path Generated</b>
</p>

<p align="center">

<img src="https://github.com/RyTang/Game-Development/blob/main/Moley/Images/CompletedMap.JPG" width="500" height="500"/>

</p>

<p align="center">
<b>Fully Completed Map Generation</b>
</p>
