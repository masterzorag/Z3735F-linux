# Z3735F-linux
linux on [Intel(R) Atom(TM) CPU Z3735F](http://ark.intel.com/products/80274/Intel-Atom-Processor-Z3735F-2M-Cache-up-to-1_83-GHz), Bay Trail


### A 64bit CPU forced working in a 32bit OS, what EFI matters?
CPU is supporting 64bit intruction sets, vendors sell products running 32bit OS, booted by a 32bit EFI.  
- EFIshell.ia32 can load EFI applications  
- GRUB2 can be builted as a 32/64bit EFI application  
- Once you have GRUB2 you can boot a 64bit OS  

## GRUB
* Build our TARGET:
```
$ grub-mkimage -C xz -o grub2ia32.efi -O i386-efi -p /usr/lib/grub/i386-efi/*.mod
$ file grub2ia32.efi
grub2ia32.efi: PE32 executable (EFI application) Intel 80386 (stripped to external PDB), for MS Windows
```
* Move it to one HDD partition, in my case in C:\myefi  

## Loading GRUB
* Enter BIOS, lauch EFI shell
* Execute GRUB, by entering full PATH
