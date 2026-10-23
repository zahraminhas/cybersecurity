
# Class 03 - CPU aur OS Basics & Memory Management, Linux, Windows

## 1. Introduction

Computer aik electronic machine hai jo data ko process karti hai aur information provide karti hai. Computer ko sahi tarah kaam karne ke liye CPU, Memory aur Operating System ki zaroorat hoti hai.

CPU computer ka main processing part hai. Operating System (OS) computer ke hardware aur software ko manage karta hai. Memory Management operating system ka aik important function hai jo RAM aur programs ki memory ko manage karta hai.

Linux aur Windows dono Operating Systems hain jo computer ko use karne mein madad dete hain.

## 2. CPU (Central Processing Unit)

### Definition

CPU stands for Central Processing Unit. It is the main processing unit of a computer that executes instructions and processes data.

CPU ko computer ka brain bhi kaha jata hai kyun ke yeh instructions execute karta hai aur calculations perform karta hai.

### Functions of CPU

- Instructions ko execute karna.
- Mathematical calculations perform karna.
- Logical decisions lena.
- Data ko process karna.
- Memory aur doosre hardware components ke sath communicate karna.

### Main Components of CPU

#### 1. ALU (Arithmetic Logic Unit)

ALU mathematical calculations aur logical operations perform karta hai.

Examples:
- Addition: 10 + 5
- Subtraction: 10 - 5
- Comparison: 10 > 5
- Logical operations: AND, OR, NOT

#### 2. CU (Control Unit)

Control Unit computer ke doosre components ko control aur coordinate karta hai.

Yeh instructions ko samajhne aur un par amal karne ke process ko manage karta hai.

#### 3. Registers

Registers CPU ke andar mojood bohat fast aur choti memory locations hoti hain. Yeh processing ke waqt temporary data aur instructions store karti hain.

### CPU Cores

Core CPU ka aik processing unit hota hai.

- Single-Core: Aik processing core hota hai.
- Dual-Core: Do processing cores hote hain.
- Quad-Core: Chaar processing cores hote hain.
- Octa-Core: Aath processing cores hote hain.

Zyada cores aik waqt mein multiple tasks ko process karne mein madad de sakte hain, lekin performance software aur CPU ki doosri specifications par bhi depend karti hai.

### Clock Speed

Clock speed batati hai ke CPU kitni tezi se clock cycles perform karta hai. Isay aam tor par GHz mein measure kiya jata hai.

Example:
Agar CPU ki clock speed 3.5 GHz hai, to iska matlab hai ke CPU clock takreeban 3.5 billion cycles per second chalti hai. Har cycle mein aik complete instruction zaroor execute nahi hoti.

## 3. Operating System (OS)

### Definition

An Operating System is system software that manages computer hardware, software resources, files, memory, and running processes.

Operating System aik aisa software hai jo user aur computer hardware ke darmiyan connection provide karta hai.

### Examples of Operating Systems

- Microsoft Windows
- Linux
- macOS
- Android
- iOS

### Functions of Operating System

#### 1. Process Management

OS running programs aur processes ko manage karta hai.

Example:
Aap browser, music player aur Word aik sath open karte hain. OS in sab ke processes ko manage karta hai.

#### 2. Memory Management

OS RAM ko programs ke darmiyan allocate aur manage karta hai.

Example:
Aap browser aur VS Code open karte hain. OS dono programs ko required memory provide karne ki koshish karta hai.

#### 3. File Management

OS files aur folders ko create, save, copy, move aur delete karne ki facility deta hai.

Example:
Documents folder mein assignment save karna.

#### 4. Device Management

OS keyboard, mouse, printer, monitor aur storage devices ko manage karta hai.

#### 5. Security Management

OS user accounts, permissions aur doosre security controls ke zariye system ko protect karne mein madad deta hai.

#### 6. User Interface

OS user ko computer ke sath interact karne ke liye interface deta hai.

Do common types hain:

- GUI (Graphical User Interface): Windows, icons aur menus ke zariye computer use karna.
- CLI (Command-Line Interface): Commands type karke computer ko instructions dena.

## 4. Memory Management

### Definition

Memory Management is the process of allocating, tracking, and freeing computer memory for programs and processes.

Memory Management mein OS decide karta hai ke kis program ko kitni memory deni hai aur jab memory ki zaroorat na rahe to usay kaise release karna hai.

### Types of Computer Memory

#### 1. RAM (Random Access Memory)

RAM temporary memory hai jahan running programs aur unka data store hota hai.

Important points:
- RAM volatile memory hai.
- Computer band hone par RAM ka data aam tor par khatam ho jata hai.
- Zyada RAM multiple applications chalane mein madad kar sakti hai.

Example:
Jab aap browser open karte hain, to uska running data RAM mein load hota hai.

#### 2. ROM (Read-Only Memory)

ROM non-volatile memory hoti hai jo power off hone ke baad bhi data retain karti hai.

Iska istemal firmware aur system ko start karne se related instructions store karne ke liye ho sakta hai.

#### 3. Cache Memory

Cache bohat fast memory hoti hai jo CPU ke qareeb ya CPU ke andar hoti hai.

Yeh frequently used data aur instructions ko store kar sakti hai, taake CPU unhein jaldi access kar sake.

#### 4. Secondary Storage

Secondary storage data ko long-term store karne ke liye use hoti hai.

Examples:
- HDD (Hard Disk Drive)
- SSD (Solid State Drive)
- USB Flash Drive

RAM aur secondary storage mein farq yeh hai ke RAM running tasks ke liye temporary working space hai, jab ke SSD aur HDD files ko long-term save karte hain.

## 5. How Memory Management Works

Jab aap koi application open karte hain, to aam tor par yeh steps hote hain:

1. Application ki required files storage se read ki jati hain.
2. Program aur uska required data RAM mein load hota hai.
3. OS process ke liye memory allocate karta hai.
4. CPU instructions execute karta hai.
5. Jab application band hoti hai, to OS us process ki memory ko release kar sakta hai.

Example:
Aap Google Chrome open karte hain. Chrome ka code aur data RAM mein load hota hai. OS uske processes aur memory ko manage karta hai.

## 6. Virtual Memory

### Definition

Virtual Memory is a memory management technique that uses storage space to extend the available memory for running programs.

Agar RAM par pressure ho, to OS storage par kuch data ko temporarily move kar sakta hai.

Windows mein isay aam tor par paging file kaha jata hai, jab ke Linux mein swap space use ho sakti hai.

Important points:
- Virtual memory RAM ka exact replacement nahi hai.
- Storage RAM se aam tor par slow hoti hai.
- Bohat zyada swapping se computer slow ho sakta hai.

Example:
Agar computer ki RAM kam ho aur multiple applications open hon, to system storage ko additional memory support ke liye use kar sakta hai.

## 7. Paging and Swapping

### Paging

Paging mein virtual memory ko fixed-size blocks mein divide kiya jata hai jinhein pages kaha jata hai. Physical memory ko frames mein divide kiya jata hai.

OS pages ko available physical memory frames ke sath map karta hai.

### Swapping

Swapping ka lafz aam tor par memory pressure ke waqt data ya processes ke kuch hisson ko RAM aur storage ke darmiyan move karne ke liye use hota hai.

Modern operating systems aksar individual memory pages ko move karte hain, na ke hamesha poore process ko.

## 8. Linux Operating System

### Definition

Linux is an open-source operating system kernel used in many operating systems, servers, cloud platforms, and embedded devices.

Linux kernel par based operating systems ko aam tor par Linux distributions ya distros kaha jata hai.

### Examples of Linux Distributions

- Ubuntu
- Debian
- Fedora
- Kali Linux
- Red Hat Enterprise Linux (RHEL)

### Features of Linux

- Open-source software ecosystem.
- Command-line interface ki strong support.
- Multi-user support.
- Multitasking.
- File permissions aur ownership.
- Servers aur cloud environments mein common use.

### Common Linux Commands

#### 1. `pwd`

Current working directory ka path show karta hai.

Example:

```bash
pwd
```

#### 2. `ls`

Current directory ki files aur folders list karta hai.

```bash
ls
```

#### 3. `cd`

Directory change karne ke liye use hota hai.

```bash
cd Documents
```

Parent directory mein jane ke liye:

```bash
cd ..
```

#### 4. `mkdir`

Naya folder banata hai.

```bash
mkdir MyFolder
```

#### 5. `touch`

Aam tor par nayi empty file create karne ke liye use hota hai.

```bash
touch notes.txt
```

#### 6. `cat`

Text file ka content display karta hai.

```bash
cat notes.txt
```

#### 7. `free -h`

Memory usage ko readable format mein show karta hai.

```bash
free -h
```

#### 8. `top`

Running processes aur system resource usage ko real time mein monitor karta hai.

```bash
top
```

#### 9. `ps`

Running processes ki information show karta hai.

```bash
ps
```

Zyada detailed process list ke liye:

```bash
ps aux
```

#### 10. `sudo`

Agar user ko permission ho, to command ko elevated privileges ke sath run karne ke liye use hota hai.

```bash
sudo apt update
```

`sudo` ko sirf trusted commands ke sath use karna chahiye.

## 9. Windows Operating System

### Definition

Microsoft Windows is a graphical operating system developed by Microsoft for personal computers and other supported devices.

Windows users ko graphical interface ke zariye applications, files, settings aur hardware use karne deta hai.

### Features of Windows

- User-friendly graphical interface.
- Files aur folders manage karne ki facility.
- Multiple applications run karna.
- User accounts aur permissions.
- Hardware aur device support.
- Built-in security features.

### Important Windows Tools

#### 1. Task Manager

Task Manager running applications, processes, CPU usage, memory usage aur doosre resources monitor karta hai.

Open karne ka shortcut:

```text
Ctrl + Shift + Esc
```

#### 2. File Explorer

Files aur folders browse aur manage karne ke liye use hota hai.

Shortcut:

```text
Windows + E
```

#### 3. Command Prompt (CMD)

Windows mein commands run karne ke liye command-line tool hai.

Example:

```cmd
dir
```

Current directory ki files aur folders list karta hai.

#### 4. PowerShell

PowerShell aik command-line shell aur scripting environment hai jo system administration aur automation ke liye use hota hai.

Example:

```powershell
Get-Process
```

Running processes ki list show karta hai.

#### 5. System Information

System Information computer ke hardware aur software environment ki details show karta hai.

Run dialog mein yeh command likh sakte hain:

```text
msinfo32
```

#### 6. Resource Monitor

CPU, memory, disk aur network resource usage ki detailed information dekhne mein madad deta hai.

Run dialog mein:

```text
resmon
```

## 10. Linux vs Windows

| Feature | Linux | Windows |
|---|---|---|
| Developer | Different communities and organizations maintain distributions | Microsoft |
| Interface | GUI aur CLI dono | GUI ke sath CMD aur PowerShell |
| Source code | Linux kernel open-source hai | Windows generally proprietary hai |
| Common use | Servers, cloud, development, security labs | Personal computers, offices, gaming |
| Software installation | Package managers aur other methods | Installers, Microsoft Store aur package tools |
| Customization | Distribution ke mutabiq bohat flexible | Available settings aur editions par depend |
| Permissions | Users, groups aur file permissions | User accounts, ACLs aur security permissions |
| Commands | `ls`, `pwd`, `ps` | `dir`, `Get-Process` |

Dono operating systems powerful hain. Behtar choice user ki requirements, software compatibility aur work environment par depend karti hai.

## 11. CPU, OS and Memory Management Relationship

CPU, OS aur memory aik doosre ke sath mil kar kaam karte hain.

Example: Aap Windows par browser open karte hain.

1. Operating System application ko start karta hai.
2. OS application ke liye process create karta hai.
3. OS required memory allocate karta hai.
4. CPU application ki instructions execute karta hai.
5. OS memory aur doosre resources ko manage karta rehta hai.

Is tarah CPU processing karta hai, OS resources ko manage karta hai aur memory running programs ko data aur instructions provide karti hai.

## 12. Important Differences

### RAM vs ROM

| RAM | ROM |
|---|---|
| Volatile memory | Non-volatile memory |
| Running programs ke liye working memory | Firmware aur persistent instructions ke liye use ho sakti hai |
| Power off par data retain nahi hota | Power off par data retain hota hai |

### RAM vs Virtual Memory

| RAM | Virtual Memory |
|---|---|
| Physical memory hardware hai | Memory management technique hai |
| Aam tor par storage se faster hai | Storage space ko memory support ke liye use kar sakti hai |
| Running data ke liye primary working memory | RAM pressure ko handle karne mein madad karti hai |

### Process vs Program

**Program:** Instructions ya software files ka set hota hai.

**Process:** Jab program execute hota hai to uski running instance ko process kaha jata hai.

Example:
Browser ki installed application program hai. Jab aap browser open karte hain to uski running instance process hoti hai.

## 13. Practical Examples

### Example 1: Check Memory in Linux

Terminal open karein aur yeh command run karein:

```bash
free -h
```

Is se total, used aur available memory ka overview milta hai.

### Example 2: Check Processes in Linux

```bash
ps aux
```

Yeh running processes ki list aur unki resource information show karta hai.

### Example 3: Check Processes in Windows

PowerShell open karke yeh command run karein:

```powershell
Get-Process
```

Is se running processes ki list milti hai.

### Example 4: Check CPU and Memory in Windows

1. `Ctrl + Shift + Esc` press karein.
2. Task Manager open hoga.
3. Performance tab par click karein.
4. CPU aur Memory usage check karein.

## 14. Security Best Practices

- Operating System ko updated rakhein.
- Strong password ya supported sign-in security use karein.
- Daily tasks ke liye administrator/root account use karne se bachein.
- Unknown commands ko bina samjhe run na karein.
- Unknown software install karne se pehle uski reliability check karein.
- Important data ka backup rakhein.
- Linux mein `sudo` aur Windows mein administrator privileges sirf zaroorat par use karein.

## 15. Important Questions and Answers

### Q1. What is CPU?

CPU computer ka main processing unit hai jo instructions execute aur data process karta hai.

### Q2. What is an Operating System?

Operating System system software hai jo hardware, software, files, memory aur processes ko manage karta hai.

### Q3. What is Memory Management?

Memory Management woh process hai jisme OS programs ko memory allocate karta hai, memory usage track karta hai aur zaroorat khatam hone par memory release karta hai.

### Q4. What is RAM?

RAM temporary volatile memory hai jo running programs aur data ko store karti hai.

### Q5. What is Virtual Memory?

Virtual Memory aik technique hai jo storage space ko memory support ke liye use kar sakti hai jab RAM par pressure ho.

### Q6. What is Linux?

Linux kernel par based operating systems servers, computers, cloud platforms aur development mein use hote hain.

### Q7. What is Windows?

Windows Microsoft ka operating system hai jo personal computers aur supported devices par use hota hai.

### Q8. What is the difference between a program and a process?

Program instructions aur software files ka set hai, jab ke process us program ki running instance hai.

### Q9. Which Linux command shows memory information?

`free -h` memory usage ka overview show karta hai.

### Q10. Which Windows tool displays CPU and memory usage?

Task Manager CPU aur memory usage display karta hai.

## 16. Conclusion

CPU instructions execute karta hai aur data process karta hai. Operating System computer ke hardware aur software resources ko manage karta hai. Memory Management programs ko required memory provide karne aur resources ko efficiently use karne mein madad karti hai.

Linux aur Windows dono important operating systems hain. Linux command-line learning, servers aur cloud environments mein common hai, jab ke Windows personal computers aur office environments mein widely used hai.

In concepts ko samajhna computer fundamentals, networking, cybersecurity aur cloud computing ke liye bohat zaroori hai.
