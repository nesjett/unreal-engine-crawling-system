## Does it use one skeletal mesh or more?
The system uses 1 skeletal mesh out of the box, for the arms while crawling. It uses the Epic skeleton as base. Adding another skeletal mesh for the walking state (normal state) it’s really simple. Also you can combine and use one skeletal mesh for everything (if you have the right animations and basic knowledge of animation blueprints.

## Does the system work for rolled grounds?
The best conditions for the system are flat grounds. Although, It may work with some up/down inclinations (not too big) and with some rolled grounds (not too much).
If you want to meet “harder situations” or more specific ones, you should be able to tweak the system with easy.

## Does the included IK system fit every scenario?
Of course not, as stated earlier, the system tries to be as general as possible, that means that it comes with examples and preconfiguration for the wide variety of games that may need it, but also provides good starting points for developing deeper and more specific gameplays.

## What happens with stairs?
The system is not aiming for complex ground shapes, the IK system that comes out of the box is a very basic example, developed for flat or semi-flat grounds. For specific scenarios you will have to develop your own IK system, but the routing and path following will work as expected for moving the player.

## In the video I don't see effects, is it easy to add particles and sounds to different kind of events in the gameplay?
Yes, adding effects should be easy as you can handle states and interaction events.
