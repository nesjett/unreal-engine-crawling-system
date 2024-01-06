# Crawling System for Unreal Engine

🎉 The simplest yet porwerfull Crawling System for Unreal Engine 🎉

![Static Badge](https://img.shields.io/badge/Engine_version-4.23%2B%2C_5.0%2B-brightblue?style=for-the-badge&logo=unrealengine&color=lightblue)
![Static Badge](https://img.shields.io/badge/Copies_sold-100%2B-brightblue?style=for-the-badge&color=brightgreen)
L|SUPPORT ON|https://discord.com/channels/685799359308365851/685799359765676064|.discord-icon|

The **Crawling System** for Unreal Engine is a framework that will empower you with a crawling system like the one seen in “Dead Space” or “Erie” games, allowing you to easily make paths that the player can “enter” and follow while crawling in the ground.  

This systems DO NOT allow to crawl freely on the game, but to follow a spline based path forward (or backwards) with some nice animations.

## Preview videos
::: youtube Nf-1ZlxaScM  


::: youtube 22P4r7rWidc



## Key features
- **Spline based** routes
- **Performant**
- Documentation + video & written tutorials
- First & Third person **character examples** + AI
- Compatible with ALS (Advanced Locomotion System v4)
- **IK hand placement** setup: Hands adapt to the ground height and rotation
- Examples and caveats provided.
- Optional **Ground detection**: No need to worry about pixel-perfec spline placement.
- **Debugging tools**
- Double or single **direction routes**
- Per instance **exit limit & location** configuration: Determine freely and independently where the character is going to take off of the route and where it is going to be located when character activates walking movement.
- Customizable behavior to enter the route, with examples provided.
- **Forward and backwards movement** (backwards movement can be disabled per route instance)
- Properties and route can be modified during runtime.
- **Configurable speed** per character: Independent for moving forward/backward
- Control camera shaking movement from bone animations when crawling.
- Arm/Body animations can't be stopped half the way: Animation always ensures **both hands are on ground**
- Configurable **Camera limits**

## Package content

!!! note

    Since Unreal Engine **version 4.27+**, the Crawling System is a component based package, making it easy to integrate into any existing project by simply using interfaces and components.
    you can find the **legacy package documentation** in the following document: [Legacy documentation page](https://redirect.epicgames.com/?redirectTo=http://bit.ly/ue4-crawling-sys-docs)



![Package content](./images/cs-package-content.jpg){ loading=lazy }

* **Debuggin** and setup elements: Game Mode, Player Controller, HUD, Widged with options.
* **Core route** Actor: Allows interacting with the route path.
* Example **routes**: 2 Actors implementing the route path with different features configured.
* Example **Characters**: 
    * 2 **Player characters** with input bindings.
    * 1 **AI character** with basic movement functionality.
* **Interfaces** (1): Allows implementing the system on existing Characters.
* **Enumerations** (3):
    * Character state: Crawling/Entering route/etc.
    * Door definition: Front/Back door.
    * Movement direction: Forward/Backwards.



## Technical considerations

The system **completly avoids using tick events** on the routes, so it is performant at any scale.

The animations for the first person Character arms can be used in production, but they are not optimal (the package focuses on functionality) which means that **the rig might fail for other skeletons**. It is also slightly adjusted on rotation and position inside the implementer blueprints.
