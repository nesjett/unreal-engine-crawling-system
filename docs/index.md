# Crawling System for Unreal Engine

The **Crawling System** for Unreal Engine is a framework that will empower you with a crawling system like the one seen in “Dead Space” or “Erie” games, allowing you to easily make paths that the player can “enter” and follow while crawling in the ground.  

This systems DO NOT allow to crawl freely on the game, but to follow a spline based path forward (or backwards) with some nice animations.

::: youtube Nf-1ZlxaScM

::: youtube 22P4r7rWidc

## Key features
- *Spline based* routes: The user can only move along a spline path. 
- **Ground detection** for correct player positioning: No need to worry about pixel-perfect placement of your spline path.
- **Basic hand IK** placement for accurate ground positioning: Character hands can align (up to a point) with the ground to make it look better on uneven floors.
- *Double or single* direction routes
- Per instance **exit limits**: Configure how far from the exit the player must be in order of exiting the crawl mode.
- *Auto interaction to enter/exit* route on proximity
- **Forward and backwards** movement: Configure if you want to allow player to move backwards while inside the crawling mode or not.
- **Configurable movement speed** (independent for *forward & backwards*)
- Camera movement animations: Example on how to coordinate camera movements with the brace animations.
- **Camera limits** when crawling: Avoids rotating the camera backwards.
- Arm animations when crawling: Arm animations will never stop mid-air. If the player stops pressing the movement key, the animation will finish.
- Arms orientation depending on ground direction (thanks to ground detection)

