L|SUPPORT ON|https://discord.com/channels/685799359308365851/685799359765676064|.discord-icon|

## Does it use one skeletal mesh or more?

The system uses 1 skeletal mesh out of the box, for the arms when crawling. It uses the Epic skeleton as base. 

Adding another skeletal mesh for the walking state (normal state) it’s really simple. 

Also you could combine and use one skeletal mesh for everything (see the [Integration with ALS](./setup/integrating-als-v4.md) for a detailed guid)

## Is the animation provided production ready?

The animation is production ready as long as you use the provided rig, and you are happy with how it looks.

Retargetting it to other skeletons might not produce a good efect, but that depends on the target rig.

## Is it performant for a production game?

Probably. Being performant is somehow subjective. 

The package tries not using tick events except when it is strictly necessary, and does not do heavy procecssing, which should be more than enough for most games.

Having said that, you game might require higher levels of optimization or more specific ways to work. For those cases, you can reach out on the :simple-discord: [Discord support channel](https://discord.com/channels/685799359308365851/685799359765676064) to ask for guidance.

## Can I have different Characters with different properties?

Yes! You can add the crawling movement component to each character that you want to give the hability to crawl. There, you can set different parameters, like speed, backwards movement, etc.

## Does the system work for rolled/twisted grounds?

The best conditions for the system are flat grounds. 

Having said that, It should work with up/down hills and with some rolled/twisted grounds (not too rolled).

If you want to have “stronger situations” or more specific ones, you should be able to tweak the system with easy, but that will require blueprint programming knowledge on your side.

## Does the included IK system fit every scenario?

Definetly not. 

As stated earlier, the system tries to be as general as possible, which means that it comes with examples and preconfigurations for a wide variety of games that may need it. 

It also provides a good starting point for developing a deeper and more specific gameplay experience.

## What happens with stairs?

The system is not aiming for complex ground shapes.

The IK system that comes out of the box is a very basic example, developed for flat or semi-flat grounds. 

For specific scenarios you will have to develop your own IK system, but the routing and path following will still work as expected for moving the player along the route, as well as aligning it to the ground.


## Can I add particles or sounds to different kind of events in the gameplay?

Yes! The *Crawling Movement* component provides various ways to get notified of events and state changes in your Character.

Adding effects should be as easy as listening for those events and playing the effect you want!

