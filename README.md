

**Course website:** http://security.cs.rpi.edu/courses/binexp-spring2015/

**Syllabus:** http://security.cs.rpi.edu/courses/binexp-spring2015/Syllabus.pdf


### Lecture Breakdown
Lecture | Title | Topics
------- | ----- | ------
01 | Syllabus and Review | Linux, C, x86
02 | Introduction to Reverse Engineering | Tools and the VM
03 | Extended Reverse Engineering | GDB & IDA
04 | Intro to Memory Corruption | ELF, the stack, calling conventions, buffer overflows
05 | Shellcoding / Code Injection | Writing shellcode, developing scenario relevant payloads
06 | Format String Vulnerabilities | Format strings, DTOR/GOT overwrites
07 | DEP and ROP | Data Execution Prevention, writing ROP chains, ret2libc
08 | Secure Systems and Game Console Exploitation | OpenBSD, SELinux, GRSEC, Game Console Exploitation
09 | Address Space Layout Randomization (ASLR) | Overview, info leaks, partial overwrites, ASLR closure
10 | Heap Exploitation | Heap structure and concepts, corruption, use after free
11 | Misc Concepts and Stack Cookies | Signed/unsignedness issues, uninitialized data, etc, bypassing stack cookies
12 | C++ Differences and Concepts | C++ basics, structures, vTables, exceptions
13 | Linux Kernel Exploitation | Kernel basics, kernel exploitation, mitigations (mmap_min_addr, kallsyms, SMEP/SMAP), bypassing mitigations
14 | Exploitation on 64bit, ARM, Windows | Exploitation differences on other architectures & platforms
15 | Automation & The Future of Exploitation | Fuzzing, taint analysis, dynamic instrumentation, SMT/SAT solvers

### Lab Breakdown
Lab | Topic | Corresponding Lectures
--- | ----- | ----------------------
[01](/src/lab01) | Reverse Engineering | 01-03
[02](/src/lab02) | Memory Corruption | 04
[03](/src/lab03) | Shellcoding | 05
[04](/src/lab04) | Format Strings | 06
[P1](/src/project1) | Project 1 | 01-06 (Comprehensive)
[05](/src/lab05) | DEP and ROP | 07
**XX** | **ASLR should always be enabled from this point on** | **See VM Information for details**
[06](/src/lab06) | ASLR | 09
[07](/src/lab07) | Heap | 10
[08](/src/lab08) | Misc and Stack Cookies | 11
[09](/src/lab09) | C++ | 12
[P2](/src/project2) | Project 2 | 01-12 (Comprehensive)
[10](/src/lab10) | Linux Kernel | 13

### Repository Breakdown
* [src/](/src) - Source code for labs
* [setup_wargame.sh](/setup_wargame.sh),[external_tools.sh](/external_tools.sh) - Install scripts to setup MBE on an Ubuntu 14.04 32-bit machine
* [MBE_release.tar.gz](https://github.com/RPISEC/MBE/releases/download/v1.1_release/MBE_release.tar.gz) - Binaries for labs and projects
* [MBE_lectures.tar.gz](https://github.com/RPISEC/MBE/releases/download/v1.1_release/MBE_lectures.tar.gz) - PDFs of all lecture slides
* [MBE_VM.vmdk.gz](https://github.com/RPISEC/MBE/releases/download/v1.1_release/MBE_VM.vmdk.gz) - A vmdk (disk image) of a VM that is already setup

* **ASLR must be enabled after completing the DEP/ROP lab, and stay enabled for the rest of the course**
  * Until reboot: ```# echo 2 > /proc/sys/kernel/randomize_va_space```
  * Persist reboot: ```# echo 'kernel.randomize_va_space = 2' > /etc/sysctl.d/01-disable-aslr.conf```

#### Where can I learn more?
Play more wargames:
* [SmashTheStack IO](http://io.smashthestack.org/)
* [Pwnable KR](http://pwnable.kr/)
* [OverTheWire](http://overthewire.org/wargames/)
* [Reversing KR](http://reversing.kr/)
* [W3Challs](http://w3challs.com/)

