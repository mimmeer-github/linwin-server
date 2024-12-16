# LinWin Server

>[!NOTE]
>This is documentation for ***how to get info*** from the servers.
>
>If you want the actual project go here: [mimmeer-github/LinWin](https://github.com/mimmeer-github/LinWin)

This is where many LinWin files are, this currently hold the following:

- MAN command text files

## Coming up
Soon to come to this repo:

- LinWin compiled executables
- APT files

## Folder Structure

```
linwin-server
├── LICENCE
├── README.MD
├── MAN
│   └── [COMMAND].txt
└── APT
    └── [SOFTWARE-NAME]
        ├── metadata.meta
        └── version
            └── [VERSION]
                ├── license
                ├── version-meta.meta
                └── install.linwin
```

### Example - APT - Files

There are 3 types of a LinWin package:
- WINGET -- You supply the WinGet package ID (can be for MS-Store for just for WinGet: e.g Scratch 3, MS-Store: `9PFGJ25JL6X3`, WinGet: `MITMediaLab.Scratch.3`).
- LINUX -- You supply the APT package name.
- CUSTOM -- You must supply the URL for a Windows EXE/BATCH and the switches for uninstallation and installation (both silent).

Example software: Scratch 3

install.linwin (Windows/WSL):
```
-/ LinWin Install info \-
-/ This is a comment \-

PACKAGE-NAME: MITMediaLab.Scratch.3
```

install.linwin (Custom):
```
-/ LinWin Install info \-
-/ This is a comment \-

PACKAGE-URL: https://downloads.scratch.mit.edu/desktop/Scratch%20Setup.exe
ARGS: /allusers /S
UNINST-URL: https://downloads.scratch.mit.edu/desktop/Scratch%20Setup.exe
UNINST-ARGS: /S
```

metadata.meta:
```
-/ User Display info \-

NAME: Scratch 3
LATEST-VERSION: 3.29.1

-/ LinWin info \-

TYPE: WINGET
-/ Could also be "LINUX" or "CUSTOM" \-
```

version-meta.meta:
```
VERSION-PACKAGE: 3.29.1
RELEASE-DATE: 27/2/2022
```

### Example - APT - Folders

```
linwin-server/apt
└── metadata.meta
    └── 3.29.1
        ├── install.winlin
        └── version-meta.meta
```

### Example - MAN - File

Example Command: Help

help.txt:
```
HELP
====
Displays a list of LinWin / Linux commands and shows Windows alternatives.

EXAMPLES
========
help
```

### Example - MAN - Folders

```
linwin-server/man
├── help.txt
├── apt.txt
└── linwin-config.txt
```
