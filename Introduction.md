# INTRODUCTION

After the kernel is loaded into the RAM, the GRand Unified Bootloader (GRUB) turns over the execution to the kernel.[5]  The kernel first initializes memory and set up memory allocation tables. It initializes all I/O devices including the hard drives and mounts the root filesystem (/) in read-only mode. The rest of the filesystems are mounted later. The initialization process starts as the kernel initializes hardware as well as kernel data structures. Then kernel command line is saved and Hard-drive information is retrieved from the Basic Input Output System (BIOS).[6]  After the retrieval is done, memory size is determined through the BIOS. Then hardware is prepared to move to the protected mode. (Protected mode is the normal memory mode that the system runs in). The “Protected Mode Enabled” bit is set in the Machine Status Word and the protected mode is turned on. Page tables are initialized which are part of virtual memory support and Paging is enabled by setting the PG bit in control register 0 and after the virtual memory is turned on, Exception handlers are installed. If a programming error is detected, these routines get control and the timer interrupt is installed. After these installations, kernel detects the attached devices in the system & loads their drivers into RAM and mounts root filesystem into read-only memory mode. Finally, the ‘init’ process is initialized for further processing.[7] 

Now-a-days where industry is working towards the virtualization and cloud ,the boot time of an operating system dominates the performance of virtualization service.[8]  There exists various architectures to address the boot time for example Monolithic and Micro kernel architecture[9] .This study will briefly explain the architecture of monolithic and Microkernel kernel and will focus on the areas which are acting dominantly for the boot process.

A Monolithic kernel is an architecture where the entire operating system including the device drivers, file system, and the application IPC work in kernel space. The execution of the monolithic kernel is quite fast as the services are implemented under the same address space. Monolithic kernels are able to dynamically load and unload executable modules at runtime [10] .

As for the Microkernel Architecture it includes memory, process scheduling mechanisms and basic inter-process communication. Unlike monolithic kernel here, the user services and kernel services are implemented on different address space. The execution of a microkernel is quite slow in comparison to that of a monolithic kernel, but the microkernel is secure and they are very modular so if any changes to be made in the services it can be done without touching the kernel space as for in a monolithic kernel if a service fails then the entire system fails.[11] 

The moral of the story is that anybody who's deciding what kernel architecture to use needs to first decide what their ultimate goal is. Microkernel systems are (when properly implemented, of course) more secure, maintainable, and modular. However, they can be tough to architect properly, and may have performance overhead over a monolithic implementation. A monolithic kernel will be faster, but security will be harder to implement and it will be less modular and less easy to customize.[12]  As per the aforementioned discussion, there is a gap in booting process. In our research we will discuss applicability of different boot time reduction techniques with respect to traditional Linux systems and various measurement methodologies necessary to combine with reduction techniques in order to effectively optimize and measure the boot time.

## Current Scenario
*On Hardware Level:*

Flash memory is suitable for data storage because it has a volatility in which data can be written and erased and no refresh is needed. In particular, NOR flash memory is widely being used for booting and storage in Systems that do not require a high-speed interface. With the growth of the system market, a memory capable of Supporting high speed access, having large capacity, as well as being cost-effective due to service variety and high functionality has been requested. However, the conventional NOR flash memory does not fulfill such a request. Although conventional DRAM meets Such a request at present, it is a volatile memory and is not suitable for data storage.

*On Software Level:*

![Image of Software Level boot processes](https://raw.githubusercontent.com/Ashutoshcoder/operating-system/master/images/software-level.PNG)

**What change we will do to improve situation?**

In the meantime, since the NAND flash memory is easy to realize, has a large capacity, and is cost-effective compared with the NOR flash memory, it is widely used as a large capacity memory. Also, since the NAND flash memory is easy to fabricate and has a good integrity, its use as a booting memory has been proposed.

V-NAND or 3D V-NAND is a cell layer-stacking technology where multiple flash memory cell layers are stacked vertically and 3-dimensionally on a single NAND chip.
