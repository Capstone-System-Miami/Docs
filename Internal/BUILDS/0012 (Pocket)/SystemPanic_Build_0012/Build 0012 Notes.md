# Build 0012 Notes

## Neighborhood Updates
### Intersection Prefabs
- Added 4 new Intersections to the Neighborhood Generator pools.
  - Improved lighting, design and feel for these new intersections.
  - Many more are in the works.
- Didn't remove any. This means
  - Sorting layer issues / incorrect overlap will still be present in this version.
  - Some transitions and connections between intersections will feel awkward / incohesive.
### Lighting
- Changed `Intensity` of global light.  `0.5` -> `1`
- Improves the feel of Neighborhood traversal.

## Dungeon Updates
- We have some now!!! :P
- No longer only Whitebox grids for combat.
- Sizes vary based on Difficulty level
  - Diffculty indicated by the light that glows when the player gets close to a Dungeon Entrance.
  - **Easy** | 11x11
  - **Med**  | 13x13
  - **Hard** | 15x15