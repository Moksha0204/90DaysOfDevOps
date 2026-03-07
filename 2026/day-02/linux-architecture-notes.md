# Day 02 – Linux Architecture, Processes, and systemd

## 1) The core components of Linux (kernel, user space, init/systemd)

Kernel
The kernel is the main part of Linux that controls all hardware and system resources.
It manages memory devices and processes so that everything runs smoothly.
The kernel is the core engine of the Linux system.

User Space
User space is the area where user applications tools and commands run.
It includes everything that a user interacts with like shells and programs.
User space works with the kernel whenever it needs system access.

Init or Systemd
Init or systemd is the first process that starts when the Linux system boots.
It starts and manages all essential services needed for the system to run.
Init or systemd brings the Linux system to life and keeps it running properly.


## 2) How processes are created & managed?

In Linux, a process is created using fork(), which makes a copy of the parent process.
The child process often uses exec() to run a new program.
The Linux kernel manages processes by giving them CPU time and switching between them.
Processes can send signals to communicate.
When a process finishes, the kernel removes it and frees its resources.


## 3) What systemd does and why it matters?

systemd is the init system in Linux that starts and manages all services when the system boots.
It controls how services start, stop, restart, and run in the background.
It also handles logging, service dependencies, and system resources.
It matters because it makes booting faster, service management easier, and the system more stable and reliable.


## 4) Explain Process States

Running (R): Process is currently using the CPU or ready to run.
Sleeping (S): Process is waiting for some event (like input, data, or I/O).
Stopped (T): Process is paused by a signal (like Ctrl+Z) or by a debugger.
Zombie (Z): Process has completed but is still in the process table because the parent hasn’t collected its exit status.

## 5) List 5 commands you would use daily

ls – Lists files and directories in the current location.
cd – Changes the current working directory.
pwd – Shows the full path of the current directory.
cp – Copies files or directories.
grep – Searches text or patterns inside files.
