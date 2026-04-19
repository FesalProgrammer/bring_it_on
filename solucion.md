Bring It On

Create a file called song.txt and put there half the text of your favorite song.
Make a commit called "add first half of my favorite song" and send it to the server.
Make sure github has a song.txt file with the lyrics.

This new task is performed immediately after the previous one (I Can Win).

1. Add a .gitignore file to the project and configure it to hide files with the extension .db, .log and directories with the names target or bin.

*.db
*.log
target/
bin/

2. Create a feature branch and add two commits to it
git -b feature

3. Merge the feature branch in master
- Switch to master: git checkout master
- Merge feature: git merge feature

4. Return to feature and create the arrows.txt file with the following contents:
 - Switch to feature: git checkout feature
- Create arrows.txt with:
     ```
     The ship glides gently on the waves
     As day turns into night
     ```
git add arrows.txt
git commit -m "Add arrows.txt with ship poem"


5. Go to master. Create the arrows.txt file there and add the following text:
- Switch to master: git checkout master
- Create the arrows.txt file
- Add
"
One thousand burning arrows
Fill the starlit sky
"
- git add arrows.txt 
- When the conflict in arrows.txt appears, edit arrows.txt so it contains all 4 lines in this order:
     ```
     The ship glides gently on the waves
     As day turns into night
     One thousand burning arrows
     Fill the starlit sky

     ```
- Edita el conflicto en el editor git que el programa sugiere. de entre las dos opciones selecciona "Combine incoming + current", en la parte baja el editor se muestran las lineas propuestas, edita a manualamente y cuando quede como quieres lo cierras y continuas con los siguientes pasos:
- git add arrows.txt
- git commit -m "Merge feature into master, resolve arrows.txt conflict with all lines"


- git commit -m "Add arrows.txt with arrows poem"



6. Merge feature in master resolving the conflict: save all 4 lines in arrows.txt file in the order they were added in steps 4 and 5.
