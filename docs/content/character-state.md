---
tags:
  - Enum
---

# Character state


The system comes with a state system that includes 4 states. This state is used by the Crawling Component so It won’t interfere with other movement states.

- **Laid**: Is active when the player is already laying in the ground, ready to crawl.
- **Entering**: This state is active when the character is playing the entering sequence.
- **Exiting**: Same as “Entering” but when exiting.
- **Normal**: This state is active when the player is in normal situation (for example walking)


You could merge it with your own player state Enmu, but it should not be necessary, as the system is completly separated to other custom movements you could have.





