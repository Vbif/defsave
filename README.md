# DefSave
A module to help you save / load config and player data in your Defold projects between sessions

## Installation
You can use DefSave in your own project by adding this project as a [Defold library dependency](http://www.defold.com/manuals/libraries/). Open your game.project file and in the dependencies field under project add:

	https://github.com/subsoap/defsave/archive/master.zip
  
Once added, you must require the main Lua module in scripts via

```
local defsave = require("defsave.defsave")
```

## Information

Don't include an extension in your file names. Use "config" over "config.dat" for example.

---

If you need to backup or clear your save data you can find it in:

Windows
%appdata%\Roaming\appname\filename

OS X
~/Library/Application Support/appname/filename

Linux (default path is slightly modified to be within .config user folder)
~/.config/appname/filename

iOS
/var/mobile/Containers/Data/Application/{app-uid?}/Library/Application Support/appname/filename

Android 
/data/data/com.packagename/files/filename

HTML5
/data/.appname/filename

The appname is based on the function for getting the path sys.get_save_file("appname", "filename") by default DefSave saves in the OS appropriate location and not next to the binary.