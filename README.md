# raylabcodeexample

# Information:
 Simple fixed and base on default install for raylab dir.


# Working Version:
 * Raylab 2.5
 * VSCode 1.34.0

 # Fixed base on the links ref:
  * https://github.com/raysan5/raylib/commit/98fee844d1794465d5b327e60b85a5030a8bea62
  * https://github.com/raysan5/raylib/tree/master/projects/VSCode
  * https://github.com/raysan5/raylib/wiki/Using-raylib-in-VSCode
  * https://github.com/raysan5/raylib/issues/818
  
  
# Notes changes:
 * mingw32 > mingw for folder.
  
  
task.json
```
"command": "C:/raylib/mingw32/bin/mingw32-make.exe",

"command": "C:/raylib/mingw/bin/mingw32-make.exe",
```

lanuch.json
```
"program": "${workspaceFolder}/${fileBasenameNoExtension}.exe",

"program": "${workspaceFolder}/game.exe",
```

Makefile
```
ifeq ($(OS),Windows_NT)
	PLATFORM_OS=WINDOWS
	export PATH := C:/raylib/mingw/bin:$(PATH)
else
```
This is added for mingw32-make to build game.exe