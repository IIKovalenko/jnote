# JNote

## About

JNote is an elegant notepad application designed for command line productivity.
It provides an effective interface to filter and select notes. The enabled mode
will dictate what happens to a note when it is chosen. The default mode is 
"edit", which opens notes in the $EDITOR of your choice (vi by default). 
Other modes include "delete", "echo", and "copy". JNote also supports note 
versioning and synchronization via git.

<img src="https://i.imgur.com/fO8ZKp1.gif" alt="JNote Demo" width="100%">


## Dependencies

- Python 3
- Python 3 Curses Module
- Git
- xclip or pbcopy (optional)

## Install

    $ git clone http://github.com/nickmpaz/jnote.git && sudo ln -s $(pwd)/jnote/jnote /usr/local/bin/

## Uninstall

    $ jnote --uninstall && sudo rm /usr/local/bin/jnote

## Usage

Start JNote:

    $ jnote

Exit JNote:

    [ctrl + C]

### Selecting Notes

Notes are shown in the bottom section of the JNote window. Filter the available 
notes simply by typing.

Controls:

- [TAB] - autocomplete based on available notes
- [DEL] - clear filter
- [RET] - choose currently selected note
- [↑] [↓] - change current selection

### Changing Modes

Modes are shown at the top section of the JNote window. They control what happens 
to a note when it is chosen.

Controls:

- [←] [→] - change modes

Modes:

- Edit - open note in $EDITOR (vi by default)
- Delete - open prompt to delete note 
- Echo - print contents of note to console
- Copy - copy contents of note to clipboard

### Git Integration

- git with ssh, ssh-add already done

### Versioning Notes

Notes are automatically versioned using Git. To store them in a remote repository
use the command:

    $ jnote --init-remote [remote url]

This command will "initialize" the remote repository by forcefully pushing your
local notes.

### Synchronizing Notes

Once you have "initialized" a remote repository, it may be used to synchronize your
notes across multiple devices. On another device, install JNote and use the command:

    $ jnote --join-remote [remote url]

This command will overwrite your local notes with the contents of the remote repository.
Thereafter, any changes made on one of your devices will appear across all of them.

### Enabling Copy Mode

An additional dependency is require to enable "copy" mode. Once either xclip or pbcopy 
is installed, "copy" mode will automatically be enabled.

Linux (Ubuntu) - xclip:

    $ sudo apt install xclip

MacOS - pbcopy:

    $ sudo brew install pbcopy