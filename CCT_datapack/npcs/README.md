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
  "presets": [
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

Alternatively, you can create your own variations(resolvers) for each individual npc, which would then apply the skin as soon as that NPC is spawned in. 
