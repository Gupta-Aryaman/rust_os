# A Minimal Rust Kernel
**Target Triple** - describes the CPU architecture, the vendor, the operating system, and the ABI. For example, x86_64-unknown-linux-gnu

**BIOS** posts (power on self test) and then loads bootloader into memory.

**Bootloader** has 3 jobs-
1) to determine the location of the kernel image on the disk and load it into memory
2) switch the CPU from the 16-bit real mode first to the 32-bit protected mode, and then to the 64-bit long mode, where 64-bit registers and the complete main memory are available
3) to query certain information (such as a memory map) from the BIOS and pass it to the OS kernel
