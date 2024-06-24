```asm
;Turret64-dev2 assembly
section .data:
byte info          "Name:      il1egalmelon", 10,
                   "Discord:   il1egalmelon", 10,
                   "OS:        Linux Mint", 10,
                   "Kernel:    Linux 5.15.0-88", 10,
                   "DE:        Cinnamon", 10,
                   "Location:  Canada, USA", 10,
                   "Languages: Chinese, English, French", 10,
                   "PGR langs: C, C++, C#, x86 assembly", 10,
                   "Projects:  Turret arch, TTE, N++", 10, 0

section .code:
global main

%define PRINT_STR 0x10
%define STRING_MODE 0x13
main:
                   enter
                   stapr:immaddr $sectdat, [$gr0 + #(0x01 * 8)]    ;gets data section start address, store in $gr1 via memory map
                   %%fullstop

                   lea:imm7 [$gr0 + $gr1 * 1 + #(0x00 * 1)]        ;loads effective address of [info]
                   ldi #(info.size), $gr3                          ;gets string size
                   ldi #(STRING_MODE), $gr2                        ;gets bios print mode
                   %%fullstop

                   stapr:immaddr $leaprm, [$gr0 + #(0x04 * 8)]     ;stores the pointer for [info]
                   %%fullstop

                   int:bios #(PRINT_STR), $gr2, $gr3, $gr4         ;prints info via 0x10 (PRINT_STR)
                   leave
                   %%fullstop

                   zero:reg $gr0
                   return
                   %%fullstop
```
###

<h2 align="left">I code with</h2>

###

<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" height="40" alt="c logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg" height="40" alt="cplusplus logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg" height="40" alt="csharp logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" height="40" alt="java logo"  />
</div>

###

<h2 align="left">IDEs I use</h2>

###

<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/visualstudio/visualstudio-plain.svg" height="40" alt="visualstudio logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" height="40" alt="vscode logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=neovim" height="40" alt="neovim logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=idea" height="40" alt="intellijidea logo"  />
</div>

###
