# 1. Shops

  - Keep?
    - Work:
      - Fix UI
      - Close window button
      - Don't implement equipment mods
      - Get rid of Quest System
    - Pros:
      - 
    - Cons:
      - No NPCs
  - Trash?
    - Work:
      - Disintegrate Currency
        - From Character Menu UI
        - From Inventory
        - From Dungeon Rewards
    - Pros:
    - Cons:


# 2. Bosses (5)

  - List Shuffled at game start
  - Reward for each boss is an Equipment Mod Gem
    - Distinct enough to create emergence through boss order
    - This is where we could have shit like
      - Immovable
      - Undamageable for first `n` turns
      - etc
  - Work:
    - `IntersectionManager`
      - Find furthest intersection
        - From player spawn?
        - From Center of neighborhood?
        - Search which directions?
    - Create Boss Dungeon Preset
      - Only preset that has chance of providing equipment mods (but the chance is 100%)
      - Replace `furthestIntersection.someDungeonEntrance.dungeonPreset` with the `IntersectionManager.MGR.CurrentBoss`
    - Modify Dungeon script
      - Either write BossDungeon
      - Or add an `EnemyCombatant boss` to existing `Dungeon`
    - Modify TurnManager script
      - `EnemyCombatant boss`
      - getter/setter + logic
      - `(if boss == null) { }` logic


# 3. Equipment Mods

  - 5 Slots
    - Obtained by beating bosses.
  - Work:
    - Remove Equipment Mods tab from Inventory UI


# 4. Implement Oskar UI

  - Borders
  - Buttons
    - Import settings:
      - 32 or 64 ppu (can't remember)
      - Borders: 8px on all sides
    - Image settings
      - Tiled
    - Remove `SelectableSprite` from abstract BetterButton (only if we're using the Oskar sprites + animations below)
    - Animation
      - Animation states
        - up
        - transitionDown
        - down
        - transitionUp
      - Can be hooked up via UnityEvents on `{{WhicheverDerivative}} : BetterButton`

  - Icons?


# 5. Animations

  - Enemies
  - Characters
    - Need to be spaced out appropriately.
    - 2 frames per second?  This is what we have for idles right now.
    - Assign programmers to this?
  - CombatActions
    - Are all CombatActions already sorted to appropriate `CharacterClassType`?
    - `StandardAnimSetSO` and `StandardAnimSet` both need an additional `AnimationOverrideController whateverGeneralCombatAtionController` for each `GeneralAbilitySO : NewAbilitySO`, `GeneralAbility : NewAbility`, `ConsumableSO`, and `Consumable`
    ```GeneralAbility : NewAbility`
    {
      // {Existing Code...}

      public override AnimationOverrideController GetOverrideController(Combatant user)
      {
        return user.StandardAnimSet.whateverGeneralCombatActionController;
      }
      // {Existing Code...}

    }

      ```
      
# 6. Music

  - Find Johnny sf List and send to Prof
  - Talk to Andrew about audio system
