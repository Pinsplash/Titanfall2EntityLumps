This repo contains all of the entity lump data in Titanfall 2's BSP's, from all of the individual `.ent` files and the `.bsp`'s themselves.

* `root/`
  * Combined entity data from all files related to a map.
  * `data/`
    * Lists of all classname, editorclass, script_flag, and spawnclass keyvalues found in a map.
    * `fullgame/`
      * Same as above, but across all maps in one list. This is not a complete list of all entities in Titanfall 2 because others don't exist inside BSP files, such as `player`.
      * Separate lists for single and multiplayer.

Explanation of terms:
* **Class Name**: What type of entity something is.
* **Editor Class**: Apparently, what type something would be referred to as in the map editor, instead of its class name. All entities with an editor class still have an underlying class name. Entity data for entities using an editor name looks only trivially different than entities that don't use an editor name, which implies that either VScript or the engine is what makes editor class entities into their own unique things.
* **Script Flag**: A boolean which is somehow referenced by an entity. This seems to only be used by triggers to set the boolean to true or false. Script flags seem to be used by code to decide when events happen.
* **Spawn Class**: Unknown. This may indicate a class name that an entity is meant to convert itself to after spawning.
