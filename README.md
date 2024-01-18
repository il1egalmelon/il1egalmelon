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
                   "GPU0:     GTX 980 4GiB", 10,
                   "GPU1:     Tesla M10 32GiB", 10,
                   "Projects: Turret arch, TTE", 10, 0

section .code:
global main
main:
                   ;set up ILP header
                   nopsplit
                   macro.FlushAll()

                   ;print message
                   mov                    $xrsp, $gr00
                   ld                     &[info], $xrsp
                   ld                     0x10, $swap
                   call                   $swap
                   mov                    $gr00, $xrsp

                   ;clean up ILP header & return
                   nopsplit
                   bitwise.xor            $swap, $swap
                   ret
```
