# recoverUnitySkillsFast
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

5. Make a new empty project (to access the parameters)

4. Set VSCode as external tool in Unity
    - Top tab bar : Edit/Preferences/External Tools
    - External Script Editor -) set to VSCode

You're good to go ! 

---------------------------------------
**B) WORKING WITH UNITY**
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


    the tilepalette makes you able to view the palettes you created.

3. The right click
The right click makes you able to create things : GameObjects, ParticleEffects, UI like Buttons... By right clicking in the Project window or the Hierarchy, you can see each things sorted in sections.

    TIME LOOSERS :
    - ANIMATOR AND GAMEOBJ : Can't move anymore !
        in the animator, if you make an animation, that contains position keys (x,y,z axis), the object that hold this won't be able to move. People searched for days, weeks, and the fast fix is to not add position keys.
