The kernel is a program that constitutes the central core of a computer operating system. It has complete control over everything that occurs in the system.

A kernel can be contrasted with a shell (such as bash, csh or ksh in Unix-like operating systems), which is the outermost part of an operating system and a program that interacts with user commands. The kernel itself does not interact directly with the user, but rather interacts with the shell and other programs as well as with the hardware devices on the system, including the processor (also called the central processing unit or CPU), memory and disk drives.

The kernel is the first part of the operating system to load into memory during booting (i.e., system startup), and it remains there for the entire duration of the computer session because its services are required continuously. Thus it is important for it to be as small as possible while still providing all the essential services needed by the other parts of the operating system and by the various application programs.

Because of its critical nature, the kernel code is usually loaded into a protected area of memory, which prevents it from being overwritten by other, less frequently used parts of the operating system or by application programs. The kernel performs its tasks, such as executing processes and handling interrupts, in kernel space, whereas everything a user normally does, such as writing text in a text editor or running programs in a GUI (graphical user interface), is done in user space. This separation is made in order to prevent user data and kernel data from interfering with each other and thereby diminishing performance or causing the system to become unstable (and possibly crashing).

When a computer crashes, it actually means the kernel has crashed. If only a single program has crashed but the rest of the system remains in operation, then the kernel itself has not crashed. A crash is the situation in which a program, either a user application or a part of the operating system, stops performing its expected function(s) and responding to other parts of the system. The program might appear to the user to freeze. If such program is a critical to the operation of the kernel, the entire computer could stall or shut down.

The kernel provides basic services for all other parts of the operating system, typically including memory management, process management, file management and I/O (input/output) management (i.e., accessing the peripheral devices). These services are requested by other parts of the operating system or by application programs through a specified set of program interfaces referred to as system calls.

Process management, possibly the most obvious aspect of a kernel to the user, is the part of the kernel that ensures that each process obtains its turn to run on the processor and that the individual processes do not interfere with each other by writing to their areas of memory. A process, also referred to as a task, can be defined as an executing (i.e., running) instance of a program.

The contents of a kernel vary considerably according to the operating system, but they typically include (1) a scheduler, which determines how the various processes share the kernel's processing time (including in what order), (2) a supervisor, which grants use of the computer to each process when it is scheduled, (3) an interrupt handler, which handles all requests from the various hardware devices (such as disk drives and the keyboard) that compete for the kernel's services and (4) a memory manager, which allocates the system's address spaces (i.e., locations in memory) among all users of the kernel's services.