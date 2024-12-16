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

Example software: Scratch 3

install.linwin:
```
-/ LinWin Install info \-
-/ This is a comment \-

PACKAGE-NAME: MITMediaLab.Scratch.3
```

metadata.meta:
```
-/ User Display info \-

NAME: Scratch 3
LATEST-VERSION: 3.29.1
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
