# Build 0013 Notes 02.05.2025 (External)

## General / QOL Updates

- THERE IS A QUIT BUTTON NOW. WE ARE SORRY. ':D
- Updated the text on some buttons to indicate their purpose (i.e. just development tools, where they will end up, etc).

## Neighborhood Updates

### Intersection Prefabs

- Added more new Intersections to the Neighborhood Generator pools.
  - More in the works.
- Removed some old placeholder intersections.
  - Culled some of the more broken or buggy ones.
  - Still don't have enough new ones to remove all of them
  - Sorting layer issues / incorrect overlap will still be present in this version.
- BUG: One intersection in particular spawns the player into a parking barrier that is inescapable.
  - If this happens you can just quit and restart the application until we have fully functional in-game menus.

### Lighting

- Changed `Intensity` of global light.  `0.5` -> `0.6`
- Improves the feel of Neighborhood traversal
- Because the new intersections are fairly well-lit, we don't want to drown the map in light, but we are still finding a balance.

## Dungeon Updates

- UI improvements / testing.
- We know it's not all the way there.
- We are well aware that there is hardly enough information to make it through a combat encounter at the moment. We are taking our time to make sure that "making it through a combat encounter" is something that is actually possible before shifting focus to tweaks.<br>

<br>

# Build 0012 Notes 02.03.2025 (Internal)

## Neighborhood Updates

### Intersection Prefabs

- Added 4 new Intersections to the Neighborhood Generator pools.
  - Improved lighting, design and feel for these new intersections.
  - Many more are in the works.
- Didn't remove any. This means
  - Sorting layer issues / incorrect overlap will still be present in this version.
  - Some transitions and connections between intersections will feel awkward / incohesive.

### Lighting

- Lighting in the new intersectins vastly improves the feel of Neighborhood traversal.

## Dungeon Updates

- We have some now!!! :P
- No longer only Whitebox grids for combat.
- Sizes vary based on Difficulty level
  - Diffculty indicated by the light that glows when the player gets close to a Dungeon Entrance.
  - **Easy** | 11x11
  - **Med**  | 13x13
  - **Hard** | 15x15