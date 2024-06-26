# Crawling System for Unreal Engine

🎉 The simplest yet porwerfull Crawling System for Unreal Engine 🎉

![Static Badge](https://img.shields.io/badge/Engine_version-4.23%2B%2C_5.2%2B-brightblue?style=for-the-badge&logo=unrealengine&color=lightblue)
![Static Badge](https://img.shields.io/badge/Copies_sold-100%2B-brightblue?style=for-the-badge&color=brightgreen)
L|SUPPORT ON|https://discord.com/channels/685799359308365851/685799359765676064|.discord-icon|

The **Crawling System** for Unreal Engine is a robust framework that empowers you with a sophisticated crawling system akin to those seen in games like “Dead Space” or “Erie.” It allows players to "enter" and follow predefined paths while crawling on the ground, using spline-based navigation.

This system does **not** support freeform crawling but instead guides the player along a spline-based path, both forward and backward, with smooth animations.

## Preview videos
::: youtube Nf-1ZlxaScM  


::: youtube 22P4r7rWidc



## Key Features

- **Spline-based Routes**
  - 🚀 **Performant:** Optimized for high performance.
  - **Debugging Tools:** Includes tools to help debug and refine your paths.
  - 💯 **Best Coding Practices:** Clean, modular, and maintainable code.

- **Integration**
  - **Versatile:** Easy integration with all character types—humanoids, animals, and aliens.
  - **Modular & Component-based:** Add components and interfaces effortlessly.
  - **Automated Functional Tests:** Ensures system reliability.

- **Examples & Compatibility**
  - 👓 **Documentation:** Comprehensive docs with video and written tutorials.
  - **Character Examples:** First and third-person character setups, including AI.
  - **ALS Compatible:** Works with Advanced Locomotion System v4.

- **IK Hand Placement**
  - Hands adapt to the ground's height and rotation for realistic interactions.

- **Route Configuration**
  - 🚦 **Directional Flexibility:** Single or double direction routes.
  - **Exit Limits & Locations:** Customize where and how characters exit the route.
  - **Speed Configuration:** Independent speed settings for forward and backward movement.
  - **Movement Control:** Forward and backward movement can be enabled or disabled per route and character, even at runtime.

- **Camera and Animation Control**
  - Control camera movement through bone animations while crawling.
  - 🧲 **Movement Animations:** Ensures both hands are on the ground before stopping.
  - 🎮 **Input Support:** Compatible with keyboard and controllers.
  - **Camera Limits:** Configurable camera movement restrictions.


## Philosophy
- It is designed to allow any kind of character customization, from biped humanoids to animals and monsters of different sizes, meshes and properties.
- Everything is modular and component based. Implementation into existing characters is easy by adding the right component and implementing interfaces.
- Debugging tools are provided and separated from the functional code. You can get rid of it (or add it to existing projects) easily.
- There is a set of functions (functions library) globally available that help on general tasks.
- Everything, from functions to components to variables, is grouped. Contextual menu to search for items will not show unexpected results from this package.
- Class functions are properly accessed (public, private or protected) depending on what they are for.
- Comments are provided in-code to help understand the reason of some nodes or choices, as well as to add info about the examples.


## Package content

!!! note

    Since Unreal Engine **version 4.27+**, the Crawling System is a component based package, making it easy to integrate into any existing project by simply using interfaces and components.
    you can find the **legacy package documentation** in the following document: [Legacy documentation page](https://redirect.epicgames.com/?redirectTo=http://bit.ly/ue4-crawling-sys-docs)



![Package content](./images/cs-package-content.jpg){ loading=lazy }

* **Debuggin** tools included: Info Widgets, iconography, etc.
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

The movement component **only** uses tick events when actively crawling, and only to move the character in the proper direction. The Route Components **DO NOT USE** tick events, so the number of instances will not impact on performance.

The animations for the first person Character arms can be used in production, but they are not optimal (the package focuses on functionality) which means that **the rig might not look good on other skeletons**. It is also slightly adjusted on rotation and position inside the implementer blueprints.
