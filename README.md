# Z3735F-linux
linux on Intel(R) Atom(TM) CPU Z3735F, Bay Trail


### A 64bit CPU forced working in a 32bit OS, what EFI matters?
CPU is supporting 64bit intruction sets, vendors sell products running 32bit OS, booted by a 32bit EFI.  
- no words (they say to reduce support costs)  
- all of this is free, just knowledge
- EFIshell.ia32 can load EFI applications  
- GRUB2 can be builted as a 32/64bit EFI application  
- Once you have GRUB2 you can boot a 64bit OS  

## GRUB2

grub2ia32.efi: PE32 executable (EFI application) Intel 80386 (stripped to external PDB), for MS Windows
