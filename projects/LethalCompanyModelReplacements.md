---
layout: project
type: project
image: img/micromouse/micromouse-square.jpg
title: "LethalCompanyModelReplacements"
date: 2024
published: true
labels:
  - Blender
  - Unity
  - Lethal Company
summary: "I learned to use various community-built tools and model editing programs to create mods for the video game 'Lethal Company'."
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

Lethal Company is a 4-player cooperative video game that I play with friends. The game has a rich modding community which is constantly adding new content to the game and developing new methods to add even more features to the game. In January of 2024, the first releases of the tool "ModelReplacement API" was made public by its developer BunyaPineTree (see link below). The tool allowed modders to swap out the players' in-game character models with custom models, but this process required (and still does) a lot of work in numerous modelling softwares.

In order to create model replacements, I had to teach myself how to use each of the numerous, upcoming pieces of community-developed tools and applications. The project almost always begins with the application "Blender," which is used in conjunction with various proprietary tools, to convert models and their materials to 
For this project, I was the lead programmer who was responsible for programming the various capabilities of the mouse.  I started by programming the basics, such as sensor polling and motor actuation using interrupts.  From there, I then programmed the basic PD controls for the motors of the mouse.  The PD control the drive so that the mouse would stay centered while traversing the maze and keep the mouse driving straight.  I also programmed basic algorithms used to solve the maze such as a right wall hugger and a left wall hugger algorithm.  From there I worked on a flood-fill algorithm to help the mouse track where it is in the maze, and to map the route it takes.  We finished with the fastest mouse who finished the maze within our college.

Here is some code that illustrates how we read values from the line sensors:

```cpp
byte ADCRead(byte ch)
{
    word value;
    ADC1SC1 = ch;
    while (ADC1SC1_COCO != 1)
    {   // wait until ADC conversion is completed   
    }
    return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
}
```

You can learn more at the [UH Micromouse News Announcement](https://manoa.hawaii.edu/news/article.php?aId=2857)
