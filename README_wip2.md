
![banner](https://user-images.githubusercontent.com/9807602/156608653-227fd8e0-3b0f-42ca-85b9-89d7d81542a0.png)
Welcome to Object Scatter Documentaton, a tool for the Unity game engine.
The main goal is to provide a simple solution to organically place props on your scene to speed up the level design process.

## Features:

- Spawns multiple prefabs over a bezier path area
- Use multiple modifiers to project your prefabs and randomize/offset position, scale and rotation
- Spread the instances with modifiers for Poisson Disc Sampling, Even Spread or Random placing
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

![image](https://user-images.githubusercontent.com/9807602/189502875-07523cd0-5d30-4ad6-acac-8d61ad23960e.png)

You can inspect each one of these scenes and initial scatters to see what are the basics that the tool can do.
It spawns objects throughout a path area that you can modify by selecting the scatter object.

![image](https://user-images.githubusercontent.com/9807602/189502943-dd798b26-8318-4eea-802f-04d264d65c07.png)

These areas can be a custom bezier curve, or a primitive like quad and circle.

![image](https://user-images.githubusercontent.com/9807602/189503012-07114be5-6108-4331-9f62-23870ad2433f.png)

## Settings
All of the settings are very self explanatory on each section of the inspector. Here is an inspect on what each one of the sections are:

### Setup
Contains some options for baking the mesh, if it should auto update on selection and the mode of execution (runtime or editor or either).

![image](https://user-images.githubusercontent.com/9807602/189503205-05b433ea-8c52-46a4-bec8-ebffca19c6f2.png)

#### Baking
The items you setup in the next section are baked it into one single mesh per material.

![image](https://user-images.githubusercontent.com/9807602/189505117-b26b1430-9895-41da-bc56-d624b2f1d04b.png)

It generates objects with a baked mesh based on the prefab's material.
So **make sure the prefab being used here on items** has a `MeshFilter` **AND** a `MeshRenderer` at the **root** of it.
For now **I'm not supporting** baking multiple meshes that are child of the root prefab being added to the items list.

### Items
On this section you can control which prefabs are you going to use. 

![image](https://user-images.githubusercontent.com/9807602/189505002-c585b895-ce09-40c0-8c48-2f70012a33a5.png)

### Modifiers
Modifiers are the core of the placing. Here you have multiple options to project your prefabs onto the the area.

![image](https://user-images.githubusercontent.com/9807602/189504777-999a306e-1faf-493f-8d98-1bd9f2a0bf10.png)

You can make items spreaded **evenly**, **randomly**, using **Poisson Disc Sampling** algorithm, choose to project them into **grid**, **colliders** below the scatter path or even a **mesh**. 
Some of the modifiers that are currently included are:
- Even Spreading
- Poisson Disc Sampling Spreading
- Random Spreading
- Project On Colliders
- Project On Mesh
- Transform Offset
- Transform Randomization
- etc

![image](https://user-images.githubusercontent.com/9807602/189504879-b3627dd5-1d3c-440c-b9d3-f2a8a1aaa2af.png)

This **also** means you can create your own modifiers if you know how to code C#. 

### Exclusions
There is only one list on this section that represents the Object Scatter Paths that are being used as exclusions on your Object Scatter. 

![image](https://user-images.githubusercontent.com/9807602/189505246-e07c1719-794c-45cd-b2c2-366188746b1a.png)

The Object Scatter has a path for itself, but these childs are simple Object Scatter Path objects that will help you exclude any object intersecting these paths. 
They are automatically added to the Object Scatter (the parent object) and also removed when deleted/removed. 
You can also freely manipulate them with the gizmos once you select them.

On some examples these Object Scatter objects have an exclusion path. 

![image](https://user-images.githubusercontent.com/9807602/189505238-0a453eb5-ca10-4e2c-85cb-e58d42ed4691.png)

## Scene Editing
You only need a couple of commands to edit a bezier curve.
- Shift + Left Mouse Click on an existing bezier line to create a new point.
- Shift + Right Mouse Click on an existing point to remove it.
- Use the mouse to select/move the points on the bezier curve.

For more info on this [check this tutorial](https://github.com/elvismd/object_scatter_docs/wiki/Scene-View-Tools).

## Check out the wiki
Need more info on how to use the tool? Check out the [project wiki](https://github.com/elvismd/object_scatter_docs/wiki).

Also the [Quick Setup for Beginners](https://github.com/elvismd/object_scatter_docs/wiki/Quick-Setup-for-Beginners).

If you have any problems you can contact me at **contact@elvismd.com**.

##

I hope you can find this asset useful for your level design and can speed up the process of your scene composition. 
Please don’t forget to leave a review on the Asset Store to support the Object Scatter tool.

Thank you!
