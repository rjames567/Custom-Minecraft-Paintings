# Custom Minecraft Painting Pack
This contains a Minecraft resource pack and datapack to add additional custom paintings to the game.

## Installation
Move the the `custom-paintings-resource-pack` folder into `./minecraft/resourcepacks`, and add as normal. 
Move the `custom-paintings-data-pack` folder into `./minecraft/saves/<your-world>/datapacks` and re-enter the
world. *Note that running `/reload` is not sufficient to load the new pack*

## Adding new paintings
Adding new paintings is simple.

1. Add the new painting texture into
   `custom-paintings-resource-pack/assets/custom_paintings/textures/painting/<asset-name>.png`
3. Modify `custom-paintings-resource-pack/assets/custom_paintings/lang/en_us.json` and add:
   ```
   "painting.custom_paintings.<asset-name>.author": "<author-name>",
   "painting.custom_paintings.<asset-name>.title": "<painting-name>"
5. Modify `custom-paintings-data-pack/data/minecraft/tags/painting_variant/placeable.json` and add the
   following into the values list:
   ```
   "custom_paintings:<asset-name>"
7. Create new file `custom-paintings-data-pack/data/custom_paintings/painting_variant/<asset-name>.json`:
   ```
   {
     "asset_id": "custom_paintings:<asset-name>",
     "title": "<painting-name>",
     "height": <painting-height-in-blocks>,
     "width": <painting-width-in-blocks>
   }
9. Re-install both datapack and resource pack
