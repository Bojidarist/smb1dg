# Super Mario Bros 1 Disassembly Guide

## Compile the 6502 assembler

```bash
gcc asm6/asm6.c -o asm
./asm -h
```

## Use the assembler to create a .nes file

```bash
./asm -q smb.asm smb.nes smb.lst
```

# Credits

- [A Comprehensive Super Mario Bros. Disassembly ](https://gist.github.com/1wErt3r/4048722)

- [Edited assembly file and patches by jakiki6](https://github.com/jakiki6/smb1-disasm/)

- [A small fork of Loopy's 6502 assembler by parasyte](https://github.com/parasyte/asm6)
