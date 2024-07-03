![image](https://github.com/V01CE07/super_os/assets/114878496/af394a03-4aa4-4495-81f7-904a99af915c)
# super_os

KDE NEON or Ubuntu

download gcc, nasm, qemu
open the file folder in the terminal

let's build the project

1. nasm -f elf32 kernel.asm -o kasm.o
2. gcc -m32 -c kernel.c -o kc.o
3. gcc -fno-stack-protector -m32 -c kernel.c -o kc.o
4. ld -m elf_i386 -T link.ld -o kernel kasm.o kc.o
5. qemu-system-i386 -kernel kernel

reference - https://github.com/thedenisnikulin/os-project
