# OS
KDE NEON or Ubuntu

download gcc, nasm, qemu open the file folder in the terminal

let's build the project

nasm -f elf32 kernel.asm -o kasm.o
gcc -m32 -c kernel.c -o kc.o
gcc -fno-stack-protector -m32 -c kernel.c -o kc.o
ld -m elf_i386 -T link.ld -o kernel kasm.o kc.o
qemu-system-i386 -kernel kernel
reference - https://github.com/thedenisnikulin/os-project
