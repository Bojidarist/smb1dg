# Super Mario Bros 1 Disassembly Guide

## Table of Contents
- [Super Mario Bros 1 Disassembly Guide](#super-mario-bros-1-disassembly-guide)
  - [Table of Contents](#table-of-contents)
  - [Cloning the repository](#cloning-the-repository)
  - [Compile the 6502 assembler](#compile-the-6502-assembler)
  - [Use the assembler to create a .nes file](#use-the-assembler-to-create-a-nes-file)
  - [Apply a patch](#apply-a-patch)
  - [Creating a patch](#creating-a-patch)
  - [Utilities](#utilities)
    - [Level Editors (some can edit palletes and text)](#level-editors-some-can-edit-palletes-and-text)
    - [Tile editors](#tile-editors)
    - [Sound](#sound)
    - [More Information](#more-information)
- [Credits](#credits)

## Cloning the repository

```bash
git clone --recurse-submodules https://github.com/Bojidarist/smb1dg.git
```

## Compile the 6502 assembler

```bash
gcc asm6/asm6.c -o asm
./asm -h
```

## Use the assembler to create a .nes file

```bash
./asm -q smb.asm smb.nes smb.lst
fceux smb.nes # FCEUX is a NES emulator
```

## Apply a patch

```bash
patch smb.asm patches/nodeath.patch
```

## Creating a patch

1. Create a copy of smb.asm (for example smb.asm.bk)
2. Edit smb.asm
3. Run ``git diff smb.asm smb.asm.bk > patches/my_patch_name.patch``

## Utilities

### Level Editors (some can edit palletes and text)
  - [GreatEd](http://www.romhacking.net/utilities/1468/)

  - [SMB Utility](http://www.romhacking.net/utilities/178/)

### Tile editors
  - [JimMarshall35's Online Tile Editor](https://jimmarshall35.github.io/)

  - [Tile Layer Pro](https://www.romhacking.net/utilities/108/)

### Sound
I was not able to find a good program to edit the music/sfx. The music data starts from line **16025** in the assembly file. There is also a description on the format.  
[SMB Music Support Tool](http://www.romhacking.net/utilities/1512/) can be used in combination with [Super Mario Bros. Music Hacking Guide](https://www.romhacking.net/documents/630/).

### More Information
Check out [romhacking.net](https://www.romhacking.net/games/709/)

# Credits

- [A Comprehensive Super Mario Bros. Disassembly ](https://gist.github.com/1wErt3r/4048722)

- [Edited assembly file and patches by jakiki6](https://github.com/jakiki6/smb1-disasm/)

- [A small fork of Loopy's 6502 assembler by parasyte](https://github.com/parasyte/asm6)

- [6502 Assembly](https://en.wikibooks.org/wiki/6502_Assembly)

- [FCEUX NES Emulator](https://fceux.com/web/home.html)

- [romhacking.net](https://www.romhacking.net/games/709/)

- [GreatEd](http://www.romhacking.net/utilities/1468/)

- [SMB Utility](http://www.romhacking.net/utilities/178/)

- [JimMarshall35's Online Tile Editor](https://jimmarshall35.github.io/)

- [Tile Layer Pro](https://www.romhacking.net/utilities/108/)

- [SMB Music Support Tool](http://www.romhacking.net/utilities/1512/)

- [Super Mario Bros. Music Hacking Guide](https://www.romhacking.net/documents/630/)
