# tvc
The tool for bugs detection in the process of tainted data propagation (based on DBI Intel PIN).

Requirements:
 1. Intel pin-2.13-65163-msvc10-windows (Windows compilation)
 2. Intel pin-2.13-65163-gcc.4.4.7-linux (Linux compilation)


This tool aimed to find bugs in the process of tainted data propagation in machine code.

<h3>Usage:</h3>

pin.exe -t tvc.dll -i <syscalls list> -o <log file> -no_dll <1|0> -- <target_app>

-i <syscalls list> - file that contains syscalls list which process tainted data in the following format:
   <syscall_name> <address of system call in the target app>
-o <log file> - file to write results
-no_dll - if 1 - tvc will not consider code in shared dll.
