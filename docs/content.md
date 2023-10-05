# Content reference


## Character state
|Type|Enum|

The system comes with a state system that includes 4 states. This state is used by the Crawling Component so It won’t interfere with other movement states.

- **Crawling**: Is active when the player is already laying in the ground, ready to crawl/crawling.
- **Entering**: This state is active when the character is playing the entering sequence.
- **Exiting**: Same as “Entering” but when exiting.
- **Standing**: This state is active when the player is not in a Crawling System related state.


You could merge it with your own player state Enmu, but it should not be necessary, as the system is completly separated to other custom movements you could have.

## Door type
|Type|Enum|

Door is the name that the entrance and exit points of the route receive.

There are only 2 types of doors:
- **Front Door**
- **Back Door**

This is used to determine varios behaviors, like the distance to front/back doors to leave the route when crawling or if the *Back Door* can be used to enter the route again (in backwards direction)

## Movement direction
|Type|Enum|

This Enum is used to determine the current movement direction. It is used by the *Animation Blueprint* to run it on the right direction.

The possible values are:
- **Forward**: When the character is moving (or willing to move) forwards
- **Backward**: When the character is moving (or willing to move) backwards
- **None**: When the Character is not moving at all