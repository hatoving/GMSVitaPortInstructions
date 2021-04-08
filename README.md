# Game Maker Studio PS Vita Port Instructions
That is the longest name I've ever heard.


Hi! You must be here to play the games I ported on your Vita.
Follow this guide then.

## Step One: Getting the files
In order for the game you want to play to work properly, you'll need the game files.

### Android ports
Go ahead, pay and download the game you want to play on your Vita (example: Fran Bow) in form of a `.apk` file.
Next, extract said `.apk` file.

#### Normal APK
If the game doesn't have `.obb` file with it, then you can proceed.
Go to APK File -> assets and get the file called `game.droid` and all of its assets in the assets folder with it. 
Put them in a safe folder where you can come back to (I'll reference it as Patch Folder).

#### OBB File
If the game does have a `.obb` with it, you won't find the `game.droid` file in the APK.
Instead, it will be located in the `.obb` file. Find said `.obb` file and go to it's assets folder.
Get the file called `game.droid` file and all of its assets in the assets folder with it.
Put them in a Patch Folder.

### PC ports
Nothing fancy, go to game's directory and get the `data.win` file and all of its assets in the game directory.

##### Note, some games I port may have a marking on them, example: GAMENAME_Device. This is important because Game Maker names the `data.win` file differently specific to other devices. Another example: Windows: `data.win`, Mac OS: `game.ios`, Linux: `game.unx`, Android: `game.droid` and so on.

## Step Two: Patching the files
Now it's time to patch the files. Go back here to the repo and go to the Releases page. Pick the game you want to play on your Vita and save the `.zip` file (not the source code) to your Patch Folder.

Extract the `.zip` file and delete the `.zip` file afterwards.
Now, go to the DeltaPatcher folder and execute `DeltaPatcher.exe`

##### Note, DeltaPatcher is a patching tool for `.xdelta` files.

After you opened the `.exe` file, you will see a GUI. Select the "Original file" as the OG `data.win`/`game.droid` file and the "XDelta patch" as the `.xdelta` file for your game form the `.zip` file. Wait a few seconds and presto! The `data.win`/`game.droid` file has been patched for your PS Vita.

## Step Three: Replacing the files
It's time! Now it's only a matter of time to actually play the game.

Go to the game's directory page on your Vita in ux0:app/GAMEID/games.

##### Note, you can find the port's game ID by looking at the `INFO.txt` file from .zip file.

Now, grab the patched file and put it in the game direcory through FTP or USB.

## Step Four: There is no Step Four.
Congrats! Now, you can launch the game and play it! Have fun!

-@hatoving
