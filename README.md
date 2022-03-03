![banner](https://user-images.githubusercontent.com/9807602/156608653-227fd8e0-3b0f-42ca-85b9-89d7d81542a0.png)
Welcome to Object Scatter Documentaton, a tool for the Unity game engine.
The main goal is to provide a simple solution to organically place props on your scene to speed up the level design process.

## Features:

- Spawns multiple prefabs over a bezier path area
- Randomize position, scale and rotation
- Offset the instances positions, rotations and scales
- Spread the instances with Poisson Disc Sampling, Evenly or Randomly
- Includes sample scenes with multiple examples
- Project the instances on a grid or on top of colliders

![editor screenshot new](https://user-images.githubusercontent.com/9807602/156601132-37d0443d-f088-4e79-8535-0c07323955a8.PNG)

You can buy Object Scatter on the Asset Store [here](https://u3d.as/2kJE).

## Simple and Straightforward
Object Scatter is easy to use and uses only a couple of scripts to do the work for you. With only a couple of clicks you can place a lot of objects in your scene with collision filtering and using randomization properties. You can easily create pathways using simple gizmos that you can use to compose your scenario.

## Also for Artists Only
You don’t know how to program and it’s only using a nice visual scripting plugin to make your game? Don’t worry! You don’t need any programming knowledge to use Object Scatter.

## Getting Started
Go to the Samples folder and inside the Scenes folder you can explore the demos available.

![image](https://user-images.githubusercontent.com/9807602/156606095-975da580-9f45-498f-9460-6c3527a0f225.png)

Inside those scenes there will be one or multiple objects with a scatter script attached to them.

![image](https://user-images.githubusercontent.com/9807602/156606383-1ee9b7ee-78a0-4cad-84d1-260369a32fe7.png)

You can inspect each one of these scenes and initial scatters to see what are the basics that the tool can do.
It spawns objects throughout a custom bezier curve area that you can modify by selecting the scatter object.

![image](https://user-images.githubusercontent.com/9807602/156621568-55665e3b-a3ab-4228-bdbb-d04b4dbd47aa.png)

## Settings
All of the settings are very self explanatory on each section of the inspector. Here is an inspect on what each one of the sections are:

### Setup
Controls the spread and projection of the items. 

You can make items spreaded **evenly**, **randomly** or using **Poisson Disc Sampling** algorithm and choose to project them into **grid**, **colliders** below the scatter path or a **mesh**. 
In this section you can also control the *intensity* ``(random mode)``, the *margins* ``(even mode)`` of the [items](#items) and the *radius* ``(Poisson Disc Sampling mode)`` field that defines how much items are spawned on the screen based on the size of each item.

If you are using **random/even** with *alongside distribution* of the path, it will show an **interval** property that defines how long is the space between items spawned alongside the path. The radius property defines how much items are spawned on the screen based on the size of each item and the intensity field is hidden when using this spread mode because the radius acts in it’s place.

![image](https://user-images.githubusercontent.com/9807602/156626008-6f5ab0c5-c5ab-42a6-9d0d-df1dd9863127.png)

### Collision Contact Interaction
This only appears if your projection is on colliders. 
You can choose that layers to ignore and avoid when raycasting.
Also if the items should follow collision normals and rotate based on it.

![image](https://user-images.githubusercontent.com/9807602/156626360-455bd874-8ddd-4a8b-bc1e-74742aedcb5a.png)

### Offset Transform
Here you can add an offset to all the items transforms. These values will offset the chosen position of the item.

![image](https://user-images.githubusercontent.com/9807602/156626780-c4abc2c2-a38c-430f-ae96-9fe639a3ede1.png)

### Randomization Transform
These fields will be used to randomize the items transforms, each one of them has a Min and Max vector so you can define the randomization properly. The scatter will randomize a value to the item’s position, scale or rotation between the min and max number for each axis. A boolean on each of fields at the right side can be checked to use a single Vector value for position, rotation or scale, this is useful on scale for example when you just want a random number between 1 and 2 for example on all axis, you can check the boolean on the scale field.
**IMPORTANT NOTE**: The `Scale randomization` will override any scaling on the prefab's object (except the childs of this object).

![image](https://user-images.githubusercontent.com/9807602/156626852-6ec543cc-966b-4ba0-ba9f-6d61cc1cf324.png)

### Items
On this section you can control which prefabs are you going to use. 

![image](https://user-images.githubusercontent.com/9807602/156626902-a0e7fbb8-e7a2-4130-b627-eb90bdf2530e.png)

Here you can setup the items you want and also mark to bake it into one single mesh per material.

![image](https://user-images.githubusercontent.com/9807602/156627026-e69123ef-72b6-4807-9a46-55c50e6ab0c4.png)

It generates objects with a baked mesh based on the prefab's material.

So make sure the prefab being used here on items has a `MeshFilter` **AND** a `MeshRenderer` at the root of it.
For now **I'm not supporting** baking multiple meshes that are child of the root prefab being added to the items list.

### Exclusions
There is only one list on this section that represents the Object Scatter Paths that are being used as exclusions on your Object Scatter. 

![image](https://user-images.githubusercontent.com/9807602/156622723-7ba1d388-9997-40a4-9230-1cdf2331e864.png)

The Object Scatter has a path for itself, but these childs are simple Object Scatter Path objects that will help you exclude any object intersecting these paths. 
They are automatically added to the Object Scatter (the parent object) and also removed when deleted/removed. 
You can also freely manipulate them with the gizmos once you select them.

On some examples these Object Scatter objects have an exclusion path. 

![image](https://user-images.githubusercontent.com/9807602/156622464-815b9132-98f0-4a55-96fc-fbd5e3c31462.png)

## Check out the wiki
If you need more info on how to use the tool check out the [project wiki](https://github.com/elvismd/object_scatter_docs/wiki).
If you have any problems you can contact me at **contact@elvismd.com**.

##

I hope you can find this asset useful for your level design and can speed up the process of your scene composition. 
Please don’t forget to leave a review on the Asset Store to support the Object Scatter tool.

Thank you!
