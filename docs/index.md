# Crawling System for Unreal Engine

::: youtube Nf-1ZlxaScM

🎉 The simplest yet porwerfull Crawling System for Unreal Engine 🎉

![Static Badge](https://img.shields.io/badge/Engine_version-4.23%2B%2C_5.0%2B-brightblue?style=for-the-badge&logo=unrealengine&color=lightblue)
![Static Badge](https://img.shields.io/badge/Copies_sold-100%2B-brightblue?style=for-the-badge&color=brightgreen)



The **Crawling System** for Unreal Engine is a framework that will empower you with a crawling system like the one seen in “Dead Space” or “Erie” games, allowing you to easily make paths that the player can “enter” and follow while crawling in the ground.  

This systems DO NOT allow to crawl freely on the game, but to follow a spline based path forward (or backwards) with some nice animations.

::: youtube 22P4r7rWidc



## Key features
- Spline based routes
- First & Third person character examples + AI
- Compatible with ALS (Advanced Locomotion System v4)
- Simple IK hand placement setup (hands adapt to the ground height)
- Examples for all
- Ground detection for first person arms
- Option to rotate by ground detection or spline point rotation
- Visual debugging options
- Double or single direction routes
- Per instance exit limit distance (distance to the end for the player to "take off", for both sides independently)
- Per instance exit location (Where the player will move automatically when exiting)
- Auto interaction when approaching the entrance/exit
- Forward and backwards movement (backwards movement can be disabled per route)
- Configurable speed (independent for moving forward/backward)
- Camera shake on movement (is not an actual camera shake but rotation applied based on bone rotation, so you can control it from within the animation)
- Arm/Body animations can't be stopped half the way (animation always ensures both hands are on ground)
- Arms/Body are orientated to the direction of the spline, letting you create routes of any kind
- Camera limits

## Package content

!!! note

    Since Unreal Engine version 4.27, the Crawling System is a component based package, making it easy to integrate into any existing project by simply using interfaces and components.



![Package content](./images/cs-package-content.jpg){ loading=lazy }

## Technical considerations

TODO: Describe the technical implementation and things to take into account. (performance etc)
