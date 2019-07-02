# JNote

## About

JNote is an elegant notepad application designed for command line productivity.
It provides an effective interface to filter and select notes. The enabled mode
will dictate what happens to a note when it is chosen. The default mode is 
"edit", which opens notes in the $EDITOR of your choice (vi by default). 
Other modes include "delete", "echo", and "copy". JNote also supports note 
versioning and synchronization via git.

## Dependencies

- python3
- curses
- xclip or pbcopy (optional)
- git (optional)

## Installation

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

#### Enabling Copy Mode

An additional dependency is require to enable "copy" mode:

Linux (Ubuntu) - xclip:

    $ sudo apt install xclip

MacOS - pbcopy:

    $ sudo brew install pbcopy

### Git Integration

- git with ssh, ssh-add already done
#### Versioning Notes

#### Synchronizing Notes

