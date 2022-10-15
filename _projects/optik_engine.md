---
title: Optik Engine
layout: single
permalink: /projects/optik-engine/
---

Optik engine is a ray-casting game engine, the project is separated into two parts, renderer, and editor. The renderer part, as the name implies, handles the rendering of the game entities, and the editor lets the user create new game entities, define game maps and modify them afterward.

This project is done by a group of four people for our program development in the graphical environment course. While the scope of the project is way beyond what is asked of us, we decided that we would stick to this project, as one of us is extremely talented at programming and he already had the project planned out. Since the project is separated into two parts, we also separated into two groups working on our respective parts. 

My partner and I decided to work on the editor part. While this part is not as challenging as renderer, we had never worked on a project of this scale before, and it required us to do a lot of learning outside of the classroom. Here is a screenshot showcasing the editor ![editor](../assets/pic/optik/optik_editor.png)

After some discussion, we decided that my partner would mainly work on the front end, and I will be handling the back end. 
The major challenge I faced here is JSON files. We needed a way to save the current state of our work, including every entity created, map created, etc. Back then, I had never touched anything about JSON, actually, I don't even think I have heard about JSON then. After some learning, I got a hang of it, it is not as hard as I imagined it to be. Although the structure of our JSON file does get pretty complicated, as we needed entities, within entities we had signals, which are also JSON objects with complex structures. 

Besides saving the data, we also needed a way to read from the JSON files, by the time I implemented the load function, I was pretty comfortable with JSON already, while I still had some challenges, but they were nothing major. 

Overall, this has been a wonderful learning experience for all of us. To me personally, it was my first time programming something serious and working with really talented people to bring a project to reality, despite being a school project.

Credits to my teammates:
- Abderrahman Laoufi (Map & entity editor) <br>
  email: laoufiabder@gmail.com  <a href="https://github.com/Eerohne">github</a>
- Merouane Issad (Render) <br> email: merouaneissad@gmail.com
- Jeffrey Gan (Render)

Here are some pictures of the complete project:
![optik_game1](../assets/pic/optik/optik_game.PNG)
![optik_game2](../assets/pic/optik/optik_game2.PNG)
![optik_pres1](../assets/pic/optik/optik_presentation_1.PNG)
![optik_pres2](../assets/pic/optik/optik_presentation_2.PNG)
![optik_pres3](../assets/pic/optik/optik_presentation_3.PNG)
