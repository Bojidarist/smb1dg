# Super Mario Bros 1 Disassembly Guide

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

# Credits

- [A Comprehensive Super Mario Bros. Disassembly ](https://gist.github.com/1wErt3r/4048722)

- [Edited assembly file and patches by jakiki6](https://github.com/jakiki6/smb1-disasm/)

- [A small fork of Loopy's 6502 assembler by parasyte](https://github.com/parasyte/asm6)

- [6502 Assembly](https://en.wikibooks.org/wiki/6502_Assembly)

- [FCEUX NES Emulator](https://fceux.com/web/home.html)
