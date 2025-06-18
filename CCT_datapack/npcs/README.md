# Making NPCs
Now we'll create our own NPC

Here is an example of an NPC. Think of NPC's as like a folder of assets, where you can apply different things to them such as dialogues and behaviours.
```
{
  "resourceIdentifier": "cobblemon:global_skins",
  "hitbox": "player",
  "canDespawn": false,
  "isMovable": false,
  "isInvulnerable": true,
  "isLeashable": false,
  "allowProjectileHits": false,
  "names": [
    "Tester Tommy"
  ],
  "ai": [
    {
      "type": "apply_behaviours",
      "presets": [
        "cobblemon:core"
      ]
    }
  ]
}
```

To begin, we first need to specify the ``resourceIdentifier`` of the NPC. This tell the game client where to look for the skin. To configure this, you will need to make sure you have set up your [Resource Pack](https://github.com/TempusMMORPG/Cobblemon_Creation_Toolkit/tree/main/CCT_resourcepack).

For our example, we have all humanoid skin variations(resolvers) saved in one global file named ``global_skins``. If you choose to do this method, you will need to edit the npc in-game, and type in the aspect name for the npc like this:

![skin_set](https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExcDh0NzdjZjVnYjY2d2lkeTB1dzZmeml0dnVxbWw2ZnQ0NGx6emQ4aiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/I8wpWhH8wCYew3m9Cu/giphy.gif)

Alternatively, you can create your own variations(resolvers) for each individual npc, which would then apply the skin as soon as that NPC is spawned in. [See More](https://gitlab.com/cable-mc/cobblemon/-/tree/main/common/src/main/kotlin/com/cobblemon/mod/common/api/npc#npc-variation)

# NPC Fields
Below are some of the most common fields you can add to an NPC with various use cases:

| **Field**   | **Description** |
| :---------------- | :------ |
| hitbox        |   Sets the hitbox for an NPC. Default "player" also accepts values such as ``"hitbox": { "width": 1.0, "height": 1.0}`` |
| canDespawn           |   ``true/false`` - enables or disables despawning of the NPC, in most cases you will want this set to false   |
| isMovable    |  ``true/false`` - enables or disables movement of the NPC via pushing, fishing rods and other methods, recommended to set this to ``true``  |
| isInvulnerable |  ``true/false`` - enables or disables the ability for the NPC to take damage, recommended to set this to ``true``   |
| allowProjectileHits |  ``true/false`` - enables or disables the ability for the NPC to be hit by projectiles, recommended to set this to ``true``   |
| names |  field where you can add a single or list of names, these names will be randomly applied when the NPC is spawned.   |
| ai | defines ai (and behaviour) types that can be applied to the NPC. [See more](https://gitlab.com/cable-mc/cobblemon/-/blob/main/common/src/main/kotlin/com/cobblemon/mod/common/api/ai/config/README.md) |

To find out more about CobbledNPCs [click here](https://gitlab.com/cable-mc/cobblemon/-/tree/main/common/src/main/kotlin/com/cobblemon/mod/common/api/npc#cobbled-npcs)
