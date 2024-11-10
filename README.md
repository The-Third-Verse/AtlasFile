How to use Updated Atlas File

1. Download Atlas.Lua file to installationdir\game\data\lua\autoconfig\custom
2. Open your Seat, Programming Board, or any other LUA controller
3. Add a new library -> onStart
4. Paste the following code into it:
```
 package.preload['atlas'] = (function()
     local atlas = require("autoconf/custom/atlas")
     return atlas
 end)
```

Explanation: 
When Lua requires a file from a folder, it first checks if the file has already been loaded by the script. It does this by looking into ```package.preload['file_name']```, which is a table that can be modified. In this case, we are adding our custom atlas file to that table, allowing Lua to load your custom version instead of the default one provided by NQ.
 
