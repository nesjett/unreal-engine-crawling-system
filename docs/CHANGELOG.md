
# 3.0.0 - Unreal Engine 5.3 support
## Feat
- Unreal Engine 5.3+ support.
- Improve hand IK placement and rotation.
- Refactor of the CrawlingMovement component.
- Created global helper functions in library blueprint, listed under the "Crawling System" category.
- Added an AI example that follows the player inside and outside of routes.
- Cleanup CS_FirstPersonCharacter: Moved debugging inputs to CS_PlayerController.
- Made CS_FirstPersonCharacter camera rotate by using the native "controller pitch and yaw" instead of using custom relative rotations.
- Debug widget (Player UI) now works with any Actor that implements the CS_Debug_Interface.
- Added a debugging widget to Actors that implement the CrawlingMovement component to visually see information when debug option is ON.
- Created interface for debugging, pawn and route actors. This provides easier ways to execute/request logic in custom Actors.
- Added automated functional tests for CrawlingMovement basics.
- Add better comments to methods and nodes
- Cleanup end of route checks + removed unused functions
- CrawlingMovement component private methods have been converted to protected to facilitate customization by inheritance.
- Event dispatchers have been setup in the CrawlingMovement to make it easier to react to different events.

## Fix
- Debug widget performance improved and refactored.
- Fixed an issue when getting out of routes was moving the character to 0,0,0 coordinates in UE5.0+
- Take world ref up vector to look for ground, instead of the spline point up vector. (Can be overriden)