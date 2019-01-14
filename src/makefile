all:	start main link

start: start.asm
	nasm -f elf64 -o start.o start.asm
main: main.c
	cc -Wall -O -fstrength-reduce -fomit-frame-pointer -finline-functions -nostdinc -fno-builtin -I./include -c -o main.o main.c

link:
	ld -T link.ld -o kernel.bin start.o main.o
clean:
	rm *.o *.bin
