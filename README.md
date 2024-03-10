```asm
;Turret64-dev1 assembly
section .text:
byte info          "Name:     il1egalmelon", 10,
                   "Discord:  il1egalmelon", 10,
                   "OS:       Linux Mint", 10,
                   "Kernel:   Linux 5.15.0-88", 10,
                   "DE:       Cinnamon", 10,
                   "Location: Canada, USA", 10,
                   "CPU:      Intel i9-11900k", 10,
                   "RAM:      64GiB", 10,
                   "GPU1:     Nvidia M6000 12GiB", 10,
                   "GPU1:     Nvidia M6000 12GiB", 10,
                   "Projects: Turret arch, TTE", 10, 0

section .code:
global main
main:
                   ;set up ILP header
                   nopsplit

                   ;print message
                   mov                    $xrsp, $gr00
                   ld                     &[info], $xrsp
                   ld                     0x10, $swap
                   call                   $swap
                   mov                    $gr00, $xrsp

                   ;clean up ILP header and return
                   pop                    $xrsp, $swap
                   movsprg                $swap, $$retadlink
                   nopsplit
                   ret
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
