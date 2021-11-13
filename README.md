# restart


# Week 1

## Day 0 (No Class - Labour Day)
* No class today.

## Day 1 (Tuesday)
* Administration
* Details about the Internet / architecture
* Who are you?
* What is the cloud?
* Cloud vs On-Premises (On-Prem) and Hybrid
* Infrastructure as a Service (IaaS)
* Platform as a Service (PaaS)
* Software as a Service (SaaS)
* Operating System overview
* Version Control Basics & GitHub
* Using Discord
* Installing Python & Visual Studio Code

## Day 2 (Wednesday)
* Hardware & Brief history of computers
* CPU (Cores/Threads)
* RAM / Memory
* GPU (lots of cores)
* SSD/HDD
* Choosing components
* Cloud Pricing: [AWS Pricing Calculator](https://calculator.aws)

## Day 3 (Thursday)
* Operating Systems: History, UNIX family: Linux, BSD, MacOS, Android, iOS, Windows
* Virtualization, Virtual Machines, and AMIs (Amazon Machine Images)
* Databases: Relational (SQL) and Non-relational (NoSQL)
* Shared Responsibility Model Basics
* Object Storage (S3 / Simple Storage Service)
* x86 vs ARM (in light details)
* Ping, Traceroute
* EC2 Lab - Deploying a virtual machine

## Day 4 (Friday)
* Networking Basics (IPv4)
* Ports
* HTTP & Request/Response basics
* Firewalls
* Python interpreter & HTTP module
* EC2 Lab Continued - Connecting to it



# Week 2 Topics

## Core Topics


#

## Day 1
* Virtualbox & Virtual Machines
* Linux Kernel Overview
* [Shells](https://en.wikipedia.org/wiki/Unix_shell)
* [Directory Structure](https://linuxhandbook.com/linux-directory-structure/)
* Basic Commands: man, ls, cd, pwd, mkdir
* Using sudo
* Package Management (yum, apt, and others)


## Day 2
* More Basic Commands: touch, cat, more, less, head, tail, cp, rm, mv, rmdir, find
* Piping data with |
* Creating files with >
* Text Editors: vim basics, nano, and mention of gedit/visual studio
* Understanding output of --help and arguments from manpages.
* Contents of /sbin directory
* Symbolic Links
* [CommandLineFu.com](https://www.commandlinefu.com/commands/browse/sort-by-votes)


## Day 3
* Working with `jobs`: Ctrl-Z (suspend), `fg`, `bg`, `jobs`


# Week 3

## Day 1

### Core Topics
* Basics of using Bash
* Setting the PATH environment variable and how it works.
* Creating/removing aliases in Bash with the `alias` and `unalias` commands.
* Listing environment variables with `env` and setting them with `export`.
* Using `which` to get location of a commands.
* `echo`, 
* Accessing a variable e.g. `echo $HOME`
* Installing `git` & `fzf`
* Running scripts from `./`
* Making a file *executable* with `chmod +x`

### Supplementary Topics
* [Bash Cheat Sheet](https://github.com/LeCoupa/awesome-cheatsheets/blob/master/languages/bash.sh)
* [GitHub Topics - Bash](https://github.com/topics/bash)
* [Valve rm -rf bug](https://www.theregister.com/2015/01/17/scary_code_of_the_week_steam_cleans_linux_pcs/)


## Day 2

### Core Topics
* Reading and writing Bash/shell scripts.
* Running commands with `$( )` e.g. `$(whoami)`.
* File permissions with chmod using symbolic (u+x, g-rw, o+rwx, ug-x, etc.) or octal (700, 444, 111, etc.) notation.
* Conditionals with `if`, `elif`, and `else`.
* Persisting aliases and changes to `PATH` by editing `.bashrc`.
* Using `curl`.

### Supplementary Topics
* [DevHints.io Bash Cheat Sheet](https://devhints.io/bash)
* [Cheat.sh - Cheat Sheets](https://cht.sh/)
* [tldr - Better documentation for  commonly used apps](https://github.com/tldr-pages/tldr)


## Day 3

### Core Topics

* Base-10 (Decimal) Revision, Base-8 (Octal), Base-16 (Hexadecimal/Hex), and Base-2 (Binary)
* Converting between bases
* ASCII
* Networking Concepts: Modems, Routers, Switches
* Internet Protocol (IPv4 & IPv6)
* TCP & UDP (Connection vs Connectionless)
* IP Subnetting Basics (History & Classful Addressing)
* Signed vs Unsigned numbers
* Integer Overflows (and the Gangnam Style viewcount bug)

* Example of integer overflow (just for demonstration purposes, you don't need to know C for the course)
```c
#include <stdio.h>
#include <unistd.h>

int main() {
  //int counter = 0;  // Example of how the counter should work without an overflow.
  //unsigned char counter = 0; // 8-bit. Resets to 0 when it overflows above 256.
  char counter = 0;  // 8-bit. Overflows to -128 when it overflows.

  for (counter = 0; counter <= 300; counter++) {
    printf("Value: %d\n", counter);

    // Sleep for 50milliseconds.
    usleep(50 * 1000);
  }
}
```

### Supplementary Topics
* Software Bugs: Y2K, Knight Capital, 737 MAX, Mars Orbiter, 2038 Bug (Epochalypse)
* What packets look like in `tcpdump`.
* What files look like in a hex viewer (such as `xxd` or [hexyl](https://github.com/sharkdp/hexyl))
* Basics of how a disassembler works.



## Day 4

### Core Topics
*  Line Endings (LF aka 0x0a on Linux/MacOS, vs CRLF aka 0x0d0a on Windows)

```
00000000: 7468 6973 2069 730a 610a 7465 7374 0a74  this is.a.test.t
00000010: 6f0a 7365 650a 6966 0a6c 696e 6566 6565  o.see.if.linefee
00000020: 6473 0a61 7265 0a73 7469 6c6c 0a62 7567  ds.are.still.bug
00000030: 6765 640a 696e 0a6e 6f74 6570 6164 0a    ged.in.notepad.

vs

00000000: 7468 6973 0d0a 6973 0d0a 616e 6f74 6865  this..is..anothe
00000010: 720d 0a74 6573 740d 0a6f 660d 0a6e 6577  r..test..of..new
00000020: 6c69 6e65 0d0a 6368 6172 6163 7465 7273  line..characters
```



### Supplementary Topics
* [Computerphile - Unicode/UTF-8](https://www.youtube.com/watch?v=MijmeoH9LT4)
