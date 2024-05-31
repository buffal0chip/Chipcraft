# Chipcraft Resource Pack Repo
This repo is here so that we can update the server resource pack as we play. Below are tutorials on how to modify the resource pack. Please follow the directions closely so that nothing gets messed up. Please do not edit anything that is not in the directions below.

Upon pushing the changes, it may take around 10 minutes for the resource pack to update on the server. After that just leave and rejoin the server and the changes should be applied. In order for anyone to see the changes they must individually leave and rejoin the server.

# Blockbench
Blockbench is a program (that can be run from a web browser) that allows you to easily create custom models for Minecraft. If you want to make a custom model for any of the following tutorials you will want to use a "java block/item" model. From there there are plenty of tutorials online or you can ask me. However, making a custom model is not  necessary for most of the options.

[Blockbench](https://www.blockbench.net/)

# Custom Weapons and Tools
## 1. Add texture:
First we must add a texture for the new item:

-Follow this file path to the item folder.

    assets/minecraft/textures/item

-Click the "Add File" button in the top left corner then select "upload files". Then drag and drop a .png file that will act as the texture for your custom tool or weapon.

## 2. Add model:
Second we must add a model for the texture to be placed on:

-Follow this file path to the item folder.

    assets/minecraft/model/item

-Click the "Add File" button in the top left corner then select "upload files". Then drag and drop a .json file that will act as the model for your custom tool or weapon.

-The following is an example of a basic .json format item model. If you replace the word "example" with the texture you uploaded into the item folder it will be a basic item with that texture. Or you can import a custom model from Blockbench.
```json
{
	"parent": "minecraft:item/generated",
	"textures": {
	  "layer0": "minecraft:item/example"
	}
} 
```

## 3. Add custom model data:
Lastly we must edit the .json model file for the actual vanilla item we want to add the custom texture/model to:

-Follow this file path to the item folder then click on the item that you want to add the custom texture/model to.

    assets/minecraft/model/item

-For this example we will use the netherite sword. Below is the .json file for a netherite sword with one custom model data override.
```json
{
  "parent": "minecraft:item/handheld",
  "textures": {
    "layer0": "minecraft:item/netherite_sword"
  },
  "overrides": [
    {
      "predicate": {"custom_model_data": 1},
      "model": "item/example"
    }
  ]
}
```
-The custom model data is how you add multiple different textures/models to a single item. In order to do so you must add a new override to the items .json file such as the following. Copy and paste the following and change the custom model data number to be one higher. Then change the word "example" to the name of your .json item model. All the overrides must also be separated by commas.
```json
    {
      "predicate": {"custom_model_data": 1},
      "model": "item/example"
    }
```

# Custom Hats

# Custom Sounds
