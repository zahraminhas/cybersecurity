
# Class 04 - Kernel, Process, Thread aur CLI Commands

## 1. Introduction

Computer Operating System (OS) ke different components hotay hain jo computer ko properly work karne mein help karte hain. Kernel, Process, Thread aur CLI Commands operating system ke important concepts hain.

In concepts ko samajhna Linux, Windows, Networking aur Cybersecurity seekhne ke liye bohat zaroori hai.

## 2. Kernel

### Definition

The kernel is the core part of an operating system that manages hardware and system resources and provides communication between hardware and software.

### Urdu Explanation

Kernel operating system ka central part hota hai. Ye hardware aur software ke darmiyan communication karwata hai.

Jab koi application CPU, RAM, hard disk ya kisi doosray hardware ko use karna chahti hai, to kernel us request ko manage karta hai.

### Functions of Kernel

1. **Memory Management:** RAM ko different programs ke darmiyan manage karta hai.
2. **Process Management:** Processes ko create, schedule aur terminate karne mein help karta hai.
3. **Device Management:** Keyboard, mouse, printer aur disk jaisay devices ko manage karta hai.
4. **CPU Management:** Processes ko CPU time provide karne mein help karta hai.
5. **Security and Protection:** Processes aur system resources ke access ko control karta hai.
6. **System Calls:** Applications ko operating system ki services use karne ka tareeqa deta hai.

### Example

Jab aap computer par browser open karti hain, to browser ko CPU aur memory ki zaroorat hoti hai. Kernel in resources ko manage karne mein help karta hai.

### Types of Kernel

- **Monolithic Kernel:** Bohat si operating system services kernel space mein run karti hain. Example: Linux kernel.
- **Microkernel:** Kernel mein sirf essential services rakhi jati hain, jabke kai doosri services user space mein run karti hain.
- **Hybrid Kernel:** Monolithic aur microkernel designs ke concepts combine karta hai. Example: Windows NT family ka kernel design.

### Important Point

Kernel aur Operating System ek hi cheez nahi hain. Kernel OS ka core part hai, jabke operating system mein kernel ke ilawa system utilities aur doosray components bhi hotay hain.

## 3. Process

### Definition

A process is a program in execution.

### Urdu Explanation

Process kisi program ki running state ko kehte hain. Jab hum kisi program ko run karte hain, to operating system us ke liye process create karta hai.

Process ko apni resources aur information ki zaroorat hoti hai, jaise memory, process ID aur execution state.

### Program vs Process

- **Program:** Instructions ya code jo storage mein save hota hai.
- **Process:** Jab woh program execute ho raha hota hai.

### Real-Life Example

Aap ke computer mein Google Chrome install hai. Jab Chrome band hota hai, us ka program disk par save hota hai. Jab aap Chrome open karti hain, to us ke execution ke liye process ya processes chal sakte hain.

### Components of a Process

1. **PID (Process ID):** Process ki unique identification number.
2. **Memory:** Process ka code aur data rakhne ke liye memory.
3. **CPU State:** Process ki current execution information.
4. **Resources:** Files aur doosray resources jinhein process use kar sakta hai.

### Process States

- **New:** Process create ho raha hota hai.
- **Ready:** Process CPU par run hone ke liye ready hota hai.
- **Running:** Process CPU par execute ho raha hota hai.
- **Waiting/Blocked:** Process kisi event ya resource ka wait kar raha hota hai.
- **Terminated:** Process finish ho chuka hota hai.

### Process Management

Operating system processes ko create, schedule aur terminate karta hai. CPU scheduler decide karta hai ke kis ready process ko CPU time milna chahiye.

### Example

Jab aap browser, music player aur text editor ek sath chalati hain, to operating system in applications ke processes ko manage karta hai.

## 4. Thread

### Definition

A thread is the smallest unit of execution that can be scheduled to run within a process.

### Urdu Explanation

Thread process ke andar execution ka aik path hota hai. Aik process mein aik ya multiple threads ho sakte hain.

Aik hi process ke threads aam tor par us process ki memory aur resources share karte hain, lekin har thread ki apni execution state aur stack hoti hai.

### Example

Aik web browser mein:
- Aik thread user interface ko responsive rakhne mein help kar sakta hai.
- Doosra thread kisi task ko background mein perform kar sakta hai.
- Doosra thread data process karne mein help kar sakta hai.

Ye sirf samajhne ke liye example hai; real applications mein threads ka design different ho sakta hai.

### Advantages of Threads

1. **Responsiveness:** Application user ke actions ka response de sakti hai.
2. **Resource Sharing:** Threads aik process ke resources share kar sakte hain.
3. **Concurrency:** Multiple tasks ki progress manage ki ja sakti hai.
4. **Efficiency:** Kuch tasks ko multiple threads mein divide karna useful ho sakta hai.

### Challenges of Threads

- **Race Condition:** Jab multiple threads shared data ko unsafe tareeqay se access karte hain.
- **Deadlock:** Jab threads ya processes aik doosray ke resources ka wait karte reh jate hain.
- **Synchronization:** Shared resources ko safely access karne ke liye coordination ki zaroorat hoti hai.

## 5. Process vs Thread

| Feature | Process | Thread |
|---|---|---|
| Meaning | Running program | Process ke andar execution path |
| Memory | Apna separate virtual address space aam tor par hota hai | Same process ki memory share karta hai |
| Resources | Apne resources rakhta hai | Process ke resources share karta hai |
| Communication | IPC ki zaroorat ho sakti hai | Shared memory ke zariye communication ho sakti hai |
| Creation | Aam tor par zyada overhead | Aam tor par kam overhead |
| Failure | Aik process ka failure doosray se isolated ho sakta hai | Aik thread ka serious failure poore process ko affect kar sakta hai |

## 6. CLI (Command-Line Interface)

### Definition

A Command-Line Interface (CLI) is a text-based interface that allows users to interact with a computer by entering commands.

### Urdu Explanation

CLI aik aisa interface hai jahan hum mouse se icons par click karne ke bajaye commands type karke computer ko instructions dete hain.

Linux mein Terminal aur Windows mein Command Prompt (CMD) aur PowerShell CLI ki examples hain.

### Advantages of CLI

1. Commands ke zariye tasks quickly perform kiye ja sakte hain.
2. Files aur folders manage kiye ja sakte hain.
3. System information check ki ja sakti hai.
4. Repetitive tasks automate kiye ja sakte hain.
5. Cybersecurity aur system administration mein CLI bohat useful hai.

## 7. Basic Linux CLI Commands

### 1. pwd

**Purpose:** Current working directory show karta hai.

```bash
pwd
```

Example output:

```text
/home/student
```

Explanation: Is se pata chalta hai ke aap is waqt kis directory mein hain.

### 2. ls

**Purpose:** Current directory ki files aur folders show karta hai.

```bash
ls
```

Hidden files samet detailed listing ke liye:

```bash
ls -la
```

### 3. cd

**Purpose:** Directory change karne ke liye use hoti hai.

```bash
cd Documents
```

Parent directory mein wapas jane ke liye:

```bash
cd ..
```

Home directory mein jane ke liye:

```bash
cd ~
```

### 4. mkdir

**Purpose:** Naya folder create karta hai.

```bash
mkdir MyFolder
```

### 5. touch

**Purpose:** Nayi empty file create karne ke liye use hota hai.

```bash
touch notes.txt
```

Agar file pehle se mojood ho, to `touch` us ke timestamps update kar sakta hai.

### 6. cat

**Purpose:** File ka content display karta hai.

```bash
cat notes.txt
```

### 7. cp

**Purpose:** File ya folder copy karta hai.

```bash
cp notes.txt backup.txt
```

### 8. mv

**Purpose:** File move ya rename karta hai.

File rename karne ki example:

```bash
mv notes.txt newnotes.txt
```

### 9. rm

**Purpose:** File delete karta hai.

```bash
rm notes.txt
```

**Warning:** `rm` se delete ki gayi file aam tor par normal Recycle Bin mein nahi jati. Command run karne se pehle file ka naam check karein.

### 10. clear

**Purpose:** Terminal screen clear karta hai.

```bash
clear
```

### 11. whoami

**Purpose:** Current logged-in user ka username show karta hai.

```bash
whoami
```

### 12. id

**Purpose:** Current user ki UID, GID aur group information show karta hai.

```bash
id
```

### 13. ps

**Purpose:** Processes ki information show karta hai.

```bash
ps
```

Zyada processes dekhne ke liye:

```bash
ps aux
```

### 14. top

**Purpose:** Running processes aur system resource usage ko real time mein monitor karta hai.

```bash
top
```

Aam tor par `q` press karne se `top` se exit kiya ja sakta hai.

### 15. kill

**Purpose:** Process ko signal send karta hai.

```bash
kill PID
```

Yahan `PID` ki jagah actual process ID likhein.

Example:

```bash
kill 1234
```

Ye command PID 1234 ko default signal bhejti hai. Process terminate hona guaranteed nahi hota, aur permissions bhi matter karti hain.

### 16. man

**Purpose:** Command ka manual read karne ke liye use hota hai.

```bash
man ls
```

Manual se exit karne ke liye `q` press karein.

### 17. df -h

**Purpose:** Filesystems ki disk space usage readable format mein show karta hai.

```bash
df -h
```

### 18. free -h

**Purpose:** RAM aur swap memory ki usage show karta hai.

```bash
free -h
```

## 8. Windows CLI Commands

Windows Command Prompt mein ye commands use ki ja sakti hain.

### 1. dir

Files aur folders ki list show karta hai.

```cmd
dir
```

### 2. cd

Current directory change karta hai.

```cmd
cd Documents
```

### 3. mkdir

Naya folder create karta hai.

```cmd
mkdir MyFolder
```

### 4. cls

Command Prompt ki screen clear karta hai.

```cmd
cls
```

### 5. tasklist

Running processes aur unki information show karta hai.

```cmd
tasklist
```

### 6. taskkill

Kisi process ko terminate karne ke liye use hota hai.

```cmd
taskkill /PID 1234
```

Example mein `1234` ko actual PID se replace karein. Is command ko use karte waqt ehtiyat karein.

### 7. ipconfig

Network configuration aur IP address ki information show karta hai.

```cmd
ipconfig
```

Detailed network configuration ke liye:

```cmd
ipconfig /all
```

## 9. Important Difference: GUI vs CLI

**GUI (Graphical User Interface):**
- Icons, windows aur menus use karta hai.
- Mouse aur keyboard se operate kiya ja sakta hai.
- Example: Windows Desktop.

**CLI (Command-Line Interface):**
- Text commands use karta hai.
- Commands aur un ke options samajhna zaroori hota hai.
- Example: Linux Terminal aur Windows CMD.

## 10. Kernel, Process, Thread aur CLI ka Relationship

1. User CLI mein command enter karta hai.
2. Shell command ko interpret karta hai.
3. Command ke mutabiq program execute ho sakta hai.
4. Operating system process aur threads ko manage karta hai.
5. Kernel CPU, memory aur hardware resources manage karne mein help karta hai.
6. Command ka output terminal par display hota hai.

**Example:** Jab aap Linux terminal mein `ls` likhti hain, shell command ko execute karne mein help karta hai aur system directory ki files ki listing show karta hai.

## 11. Quick Revision

- **Kernel:** Operating system ka core part.
- **Process:** Program in execution.
- **Thread:** Process ke andar execution ka path.
- **CLI:** Commands ke zariye computer use karne ka interface.
- **PID:** Process ki identification number.
- **RAM:** Temporary working memory.
- **CPU Scheduler:** Decide karta hai ke ready processes ko CPU time kaise milega.
- **pwd:** Current directory show karta hai.
- **ls:** Files aur folders show karta hai.
- **ps:** Process information show karta hai.
- **top:** Processes aur resource usage monitor karta hai.
- **whoami:** Current username show karta hai.

## 12. Conclusion

Kernel, Process, Thread aur CLI operating system ke important concepts hain. Kernel hardware resources manage karta hai, process running program hota hai, thread process ke andar execution path hota hai, aur CLI commands ke zariye computer ko control karne ka tareeqa hai.

In concepts aur commands ki practice se Linux, Windows, system administration aur cybersecurity ki understanding improve hoti hai.
