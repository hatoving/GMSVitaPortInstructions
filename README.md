# Please don't use this guide anymore.
# Consider using YoYoLoader to play any GameMaker games.

# GameMaker Studio PS Vita Port Instructions

Hi! You must be here to play the games I ported on your Vita.
Follow this guide then.

NOTE: If you want to request a game, please either make a issue and add the "request" label on it or contect me on Twitter.
      @hatoving
      
Credits to m1s3ry and Grossleymoo for making this possible!

WARNING!!!
These instructions will be obsolete, kind of. From now on, I will make batch files that patch the files themselves rather than yourself, similar to how m1s3ry does it.

## Step One: Getting the files
In order for the game you want to play to work properly, you'll need the game files.

### Android ports
Go ahead, pay and download the game you want to play on your Vita (example: Fran Bow).

#### Game without `OBB`
If the game doesn't have a `.obb` file to make the game work on Android, then you can proceed.

Go to `Your Phone Storage/Android/com.gamename.company/assets` and copy-paste all files in it in a in a safe folder where you can come back to (I'll reference it as a Patch Folder).

##### Note, the `com.gamename.company` is the "App ID" of your game. You can find that in the app's Play Store URL after 'id'.

![image](https://user-images.githubusercontent.com/64536760/114278434-27192880-9a30-11eb-9f9e-7fdf8cc1311e.png)

#### Game with `OBB`
If the game does have a `.obb` file, you won't find anything in the assets folder.
Instead, all assets will be located in the `.obb` file. 
Find said `.obb` file in `Your Phone Storage/Android/obb/com.gamename.company` and extract it. Then, go its assets folder.
Copy-Paste all files from the `.obb` file and put them in a Patch Folder.

### PC ports
Nothing fancy, go to game's directory and copy and paste all of the game's assets.

##### Note, some games I port may have a marking on them, example: GAMENAME_Device. This is important because Game Maker names the `data.win` file differently specific to other devices. Another example: Windows: `data.win`, Mac OS: `game.ios`, Linux: `game.unx`, Android: `game.droid` and so on.

## Step Two: Patching the files
Now it's time to patch the files. 

### Older patches
First, get the `data.win`/`game.droid` file and rename it to `game.win`. 
Then, go back here to the repo and go to the Releases page. Pick the game you want to play on your Vita and save the `.zip` file (not the source code) to your Patch Folder.

Extract the `.zip` file and delete the `.zip` file afterwards.
Now, go to the DeltaPatcher folder and execute `DeltaPatcher.exe`.

##### Note, DeltaPatcher is a patching tool for `.xdelta` files. The program is for Windows only sadly, so if you're using Mac or Linux, try to launch it with Wine.

After you opened the `.exe` file, you will see a GUI. Select the "Original file" as the `game.win` file you renamed and the "XDelta patch" as the `.xdelta` from the `.zip` file you extracted. Wait a few seconds and presto! The `game.win` file has been patched for your PS Vita.

### Newer patches
Unzip the `.zip` you downloaded from the Releases page in the Patch Folder.
Copy the game assets including the `game.win` file in the `PatchedFiles/games` folder.

Execute the batch file from the `.zip`and let it do its job.

## Step Three: Installing the game and replacing the files
It's time! Now it's only a matter of time to actually play the game.

First, install the VPK included in the Releases page or in the `.zip` file you downloaded for the game trough VitaShell.
Go to the game's directory page on your Vita in `ux0:app/GAMEID`.

##### Note, you can find the port's game ID by looking at the `INFO.txt` file from .zip file you extracted.

### Older patches
Now, grab the patched `game.win` and its contents from the Patch folder and put it in `ux0:app/GAMEID/games` through FTP or USB.
### Newer patches
Just copy everything from the folder in the .zip file (`.zip file/PatchedFiles/ganes`) and paste it into `ux0:app/GAMEID/games`.

## Step Four: There is no Step Four.
Congrats! Now, you can launch the game and play it! Have fun!

-@hatoving
