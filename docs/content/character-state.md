---
tags:
  - Enum
---

# Character state


The system comes with a state system that includes 4 states. This state is used by the Crawling Component so It won’t interfere with other movement states.

- **Crawling**: Is active when the player is already laying in the ground, ready to crawl/crawling.
- **Entering**: This state is active when the character is playing the entering sequence.
- **Exiting**: Same as “Entering” but when exiting.
- **Standing**: This state is active when the player is not in a Crawling System related state.


You could merge it with your own player state Enmu, but it should not be necessary, as the system is completly separated to other custom movements you could have.





