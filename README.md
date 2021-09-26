# recoverUnitySkillsFast
 CURRENTLY UNDERWORK !
 
 In case you stopped Unity, that you lost your competences and want to get back in the game really fast 

Be sure that Unity will be the good engine for your game. There's different engines for different kinds of games, find yours. Altough, Unity is very polyvalent and great.

We'll go through all steps, let's go !

---------------------------------------
**A) INSTALLING, SETTING UP AND LINKING**
---------------------------------------
Which Script Editor ?
>Visual Studio Code alias VSCode. 

Why ? (you can ignore)
I tried :
    - Visual Studio (purple version) : no folder explorer tab and not comfy as VS Code
    - Atom : no
    - JetBrains : you need to buy a liscense and it's really for people who will like the look which is very special, and the autocomplete which is not for me, creates functions which no lign return when opening with brackets, not good for readability.
    - VS Code : Fast, folder explorer, really useful shortcuts, well made tabs for opened scripts...

---------------------------------------

1. Install VSCode :
    - https://code.visualstudio.com/download

2. Install dotnet : https://dotnet.microsoft.com

3. Remove the "[x] references" count over each variable you make
    - Go in settings in the top down left corner -) Settings
    - type CodeLens and uncheck the Editor and DiffEditor

3. Add extensions in the 5th tab in the left panel.
    - C#
    - Debugger For Unity by Unity Technologies

    (debug for autocomplete and adds stuff)
    - Unity Code Snippets (by Kleber Silva) 
    - Unity Tools (by Tobiah Zarlez)

4. Download Unity : https://unity.com (you'll have to create an account)

5. Make a new 2D Project named as your name's game or "unity-learning" (to access the parameters, and we won't lose time recreating one).

4. Set VSCode as external tool in Unity
    - Top tab bar : Edit/Preferences/External Tools
    - External Script Editor -) set to VSCode

You're good to go ! 

---------------------------------------
**B) WORKING WITH UNITY FOR 2D**
---------------------------------------
DEFINITIONS :

UI = Interface part of a game, containing buttons, information like a healthbar or text about the current mission.
1. You'll have your interface default shaped. You could use many configurations, but shape it like me :

Il you remove or want to add windows, there's a tab "Windows" in the top tab bar.

2. What are those windows :

    - Hierarchy (left): 
    contains all of the in-game elements, that we call "GameObjects". Placing an element lower than an other if they are on the same layer, the one at the bottom will be on the top of the other one in the game/scene view.

    - Scene View (in the tabs in the middle left): 
    where you work on your game, see your GameObjects, create or resize,do a lot of stuff. Where the creativity takes place !

    - Game View (middle right): 
    where you test the game, play.

    - Project (bottom-left corner): 
    game files. Keep them ordered, like folders "Scripts, Sprites, Anim", but don't make too munch subfolders.

    - Console (mid-bottom): 
    where your code errors / debug.log messages show off. 
    
    The Debug.Log function in coding is useful to debug data or string telling "this part worked, trying the following things : " to fing where the bug comes from.

    - Inspector (right): 
    Where you can see details about a GameObject, or any kind of file in the Project window. You just need to click on the object and the Inspector shows data. You can then modify the data, add components to it like a collider or a script.

    - Animator (in the tabs in the middle left): 
    each animation contained in an Animator on the gameobject will appear as a block, and you 'll be able to create/del links, add conditions and more !

    - Asset Store (in the tabs in the middle left): 
    download free/buyable ressources on a public store

    - Package Manager (in the tabs in the middle left): 
    Download stuff more like UnityEngine utilities, like the 2D Tilemaps package. You can also update UnityUtilities in this thing.

    - Tile Palette (in the tabs in the right part with the inspector): 
    Many games use tilepalettes. This consist of palettes containing each sprite of the game, and that you place together in a grid to make a map, like this :

    the tilepalette makes you able to open palettes (use them).

3. The right click
The right click makes you able to create things : GameObjects, ParticleEffects, UI like Buttons... By right clicking in the Project window or the Hierarchy, you can see each things sorted in sections.

4. The basic components of a GameObject :
    - Rigidbody 2D : This component handles physics. For example, you can't apply gravity or collision without it. It's "Body Type" is the main parameter, and has three types :
        - Kinematic Rigidbody 2D : Object not affected by gravity or forces : designed to move under simulation, under very explicit user control. 
        - Dynamic Rigidbody 2D : object affected by gravity and forces.
        - Static : welp, static.
    - Colliders : makes your object collide with other ones. Can be used for physics effects, doing something on collision... There's 3 main types :
        - Box Collider 2D
        - Capsule Collider 2D
        - Circle Collider 2D

5. Practice time ! Now that we learnt about the basics of the engine, we can already try to create something. Let's make a character and its movement system ! I'll guide you :
    1. Import the sprite given in this repo or your own sprite visuals for the player we'll create. You drag it into the "Project" window.

    2. Now, we'll learn IMPORTING : When importing, we have to modify parameters to our sprite. It's by default quality-downgraded with filters that, for 3d sprites, ruins 2d ones.
        - Click on your import.
        - You can modify "Pixels Per Unit" to modify its default size in-game. I prefer letting it to 100 so it doesn't make a mess of different values.
        - Set "Filter Mode" to "Point(no filter)". (makes blurry)
        - Set "Compression" to "None".

        If you're importing a big sprite / spritesheet and still having graphical cleaness issues, it can be due to the max size and resize algorithm :
            - "Max Size" : set a corresponding size.
            - If still doesn't fix :"Resize Algortithm" : Bilinear.
    
6. To add an element in your scene, drag it into the hierarchy.

7. Once done, click on it and look in the inspector. We are going to add to it the basics to create a player character.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
    TIME LOOSERS :
    - ANIMATOR AND GAMEOBJ : Can't move anymore !
        in the animator, if you make an animation, that contains position keys (x,y,z axis), the object that hold this won't be able to move. People searched for days, weeks, and the fast fix is to not add position keys.

    COOL RESSOURCES :
    - visual effects : https://assetstore.unity.com/packages/vfx/shaders/fullscreen-camera-effects/realistic-glitches-lite-107974