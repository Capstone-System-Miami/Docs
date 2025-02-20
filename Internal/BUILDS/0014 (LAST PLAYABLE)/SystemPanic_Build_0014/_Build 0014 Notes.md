# Build 0014 Notes 02.20.2025 (External)

## Neighborhood Updates

### Intersection Prefabs

- Added more intersection prefabs.
- Haven't come across any intersections still using the broken tile sprites (appear as pink squares).
    - There are ways to check this, but in the interest of having a playable build to present, we haven't done so thoroughly.
- Still have not fixed every dungeon entrance to visually communicate that it is such.

### Bug Fixes
- Fixed collider issues on some intersections.

### Active Bugs
- Player spawns inside an inescapable collider
  - Intersection with a black and yellow parking barrier.
  - Intersection with a large tree surrounded by bushes.
  - If this happens you can just quit and restart the application until we have fully functional in-game menus with "Start Over".
  - Plan: allow intersections to define spawn points for the player, so each can ensure that the player starts in a valid location.

## Dungeon Updates

### More prefabs
- More prefabs in the pools

### COMBAT OVERHAUL HAS BEEN IMPLEMENTED
- Biggest change for the user is that movement pathing is now realtime as the cursor moves around
    - Movement now behaves more similarly to taking Actions.
    - Player can select a path, then explore the board with their cursor
        - Count tiles
        - Read descriptions of their Actions
        - NOT IMPLEMENTED: Hover over enemies to see their current status (health, stats, conditions)
        - Either select a new path or confirm when they're satisfied with their decision.
- Changes for development
    - Combatants run on State Machines
    - Allows for clarity in development
    - Self-contained behavior definition within states
    - Will streamline bug fixing
    - Will streamline implementation of changes
    - Will streamline CombatAction balancing generally
    - Will streamline UI hookups

### UI - Pop-ups
- Pop-ups in the player’s Loadout offer descriptions of each Action

### UI - Prompts
- Updated Input / Turn State Prompts in the lower right corner inform the player of their options for progressing through the rest of their turn.

### Enemies
- We are happy to introduce the first non-placeholder enemy, a lil Slime guy!
- Our slime friend serves as the first enemy which implements animations
    - Idle state
    - Animation for its CombatAction "Acid Spit"
- The application of the CombatAction is out of sync with the timing of the animation
    - The animation loops, rather than exiting upon completion.
    - We plan to refine the CombatAction system to execute upon completion of the animation.

### Bug Fixes
- Fixed an issue with one grassy dungeon, wherein enemies could spawn outside the game board, causing an unplayable game state.
- Fixed an issue with a cafe-type dungeon wherein chairs around a counter were rendering in front of combatants.
- Fixed rendering issue with arrows, which were sporadically rendering underneath tile overlays during movement pathing.
- Fixed rendering issue with Enemies, which were rendering behind the player even when they were positioned further forward on the game board.

### Active Bugs
- Player can open their loadout and click a CombatAction while they are deciding on a path to move to.
    - Plan: Visually indicate that they cannot select a CombatAction until they have confirmed that they do not want to move anymore for the remainder of the turn.
- Deselecting/Unequipping a CombatAction does not unhighlight the button in the player's Loadout.
    - Only unhighlights if another action is selected directly.
    - Plan: This is uninvestigated. Need to determine the cause.

### Obstacles
- Art is done
- C# interfaces exist for implementing
- Still being scripted
