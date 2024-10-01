Prerequisites:
To build and run BadrGeesa, you will need a Linux environment. You can use native Linux, a virtual machine, or the Windows Subsystem for Linux (WSL) to set it up.

Ensure you have the following tools installed in your Linux environment:

QEMU: For emulating the operating system.
GCC Cross-Compiler: To build the kernel (i.e., i686-elf-gcc for i386 architecture).
NASM: The assembler for compiling assembly files.
Steps to Boot PeachOS:
Set Up Your Environment (Linux or WSL):

1- On Ubuntu/Debian-based distributions, you can install the required packages using:
sudo apt update
sudo apt install qemu nasm build-essential


2- Clone the Repository:

3-Build the Kernel: Run the following command to compile the kernel and other components:
./build.sh


4-qemu-system-i386 -kernel build/kernel.bin


5- In a separate terminal, start GDB and connect to QEMU:
gdb
target remote localhost:1234

src: Kernel, bootloader, memory management, and filesystem code.
/programs: Contains example programs.
/build.sh: Script to automate the build process.


Note:
This project requires a Linux-based environment to build and run successfully. For Windows users, WSL (Windows Subsystem for Linux) or a virtual machine running Linux can be used to set up the necessary environment.
