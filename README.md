# A Hello World Program Written In X86 64 Bit NASM Assembly
### 🐧 Only Works On Linux
```assembly
section .data
msg db "Hello World", 0xA
len equ $ - msg
section .text
global _start
_start:
mov rax,1
mov rdi,1
lea rsi,[rel msg]
mov rdx,len
syscall
mov rax,60
mov rdi,0
syscall
```
💻 Details

1. Uses x86 CPU Architecture (64-bit)

2. Written in NASM Assembly
3. Demonstrates Linux syscalls (write and exit)
## 💿 To Run
## Make Sure You Have NASM And ld Installed
```zsh
nasm -f elf64 hello.asm -o hello.o
ld hello.o -o hello
./hello
```

