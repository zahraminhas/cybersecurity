
# Class 05 - Root vs User Level, Sudo, Logs aur Commands

## 1. Introduction

Linux Operating System mein users, permissions, sudo aur logs bohat important concepts hain. In ki help se hum system ko securely use kar sakte hain, administrative tasks perform kar sakte hain aur system mein hone wali activities ko monitor kar sakte hain.

Is class mein hum seekhein ge:

- Root User
- Normal User
- User Level aur Root Level
- Sudo Command
- File Permissions
- Linux Logs
- Important Linux Commands
- Practical Examples
- Security Best Practices

## 2. Root User

### Definition

The root user is the superuser account in Linux that has almost unrestricted administrative privileges over the system.

### Urdu Explanation

Root user Linux ka administrator account hota hai. Is ke paas system ki files, users, permissions, software aur doosri important settings ko manage karne ke extensive privileges hotay hain.

Root user ko system par bohat zyada control hasil hota hai. Isi liye root account ko carefully use karna chahiye.

### Root User ke Functions

1. New users create karna.
2. Users ko delete karna.
3. Software install aur remove karna.
4. System configuration change karna.
5. File permissions change karna.
6. System services manage karna.
7. Logs aur protected files access karna.

### Example

Linux mein root user ka username aam tor par `root` hota hai.

Root user ki identity check karne ke liye:

```bash
whoami
```

Agar current account root hai, to output aam tor par ye hoga:

```text
root
```

### Important Point

Root account powerful hota hai. Agar root privileges ke sath ghalat command run ho jaye, to important files delete ho sakti hain ya system damage ho sakta hai.

## 3. Normal User

### Definition

A normal user is an account that usually has limited permissions to access files, run applications and perform everyday tasks.

### Urdu Explanation

Normal user woh account hota hai jo daily computer use karne ke liye banaya jata hai. Is user ko apni files aur permitted applications access karne ki permission hoti hai.

Lekin normal user har system file ko modify nahi kar sakta.

### Normal User ke Functions

1. Files create aur edit karna.
2. Applications run karna.
3. Documents aur folders manage karna.
4. Internet use karna.
5. Apni allowed files access karna.
6. Terminal commands execute karna.

### Example

Agar aap Linux mein `student` naam ka account use kar rahi hain, to:

```bash
whoami
```

Output:

```text
student
```

Yahan `student` normal user ka example hai.

### Important Point

Normal user ko limited permissions dena system security ke liye useful hota hai.

## 4. Root User vs Normal User

| Feature | Root User | Normal User |
|---|---|---|
| Access | Extensive administrative access | Limited access |
| System files | Aksar modify kar sakta hai | Permission ke baghair modify nahi kar sakta |
| Software installation | Administrative permission ke sath kar sakta hai | Aam tor par elevated permission chahiye |
| User management | Users manage kar sakta hai | Aam tor par nahi |
| Risk | Ghalat command se system ko zyada nuqsan ho sakta hai | Aam tor par limited scope mein risk hota hai |
| Symbol in terminal | Aksar `#` prompt | Aksar `$` prompt |

Note: `#` aur `$` common terminal prompt conventions hain. Ye har system par guaranteed nahi hain.

## 5. User Level aur Root Level

### User Level

User level par commands normal user ki permissions ke mutabiq execute hoti hain.

Example:

```bash
mkdir myfolder
```

Ye command current directory mein folder create karti hai, agar user ke paas us directory mein write permission ho.

### Root Level

Root level par commands administrative privileges ke sath execute hoti hain.

Example:

```bash
sudo mkdir /opt/myfolder
```

Ye command `/opt` ke andar folder create karne ki koshish karti hai. Is ke liye authorized sudo access aur suitable system permissions zaroori hain.

### Difference

- User level: Limited permissions.
- Root level: Administrative permissions.
- User level: Daily tasks ke liye suitable.
- Root level: System administration ke liye zaroori ho sakta hai.

## 6. Sudo Command

### Definition

Sudo stands for "Superuser Do". It allows an authorized user to execute a command with elevated privileges according to the system's sudo policy.

### Urdu Explanation

`sudo` Linux ki aik important command hai. Is ki help se authorized normal user kisi command ko administrator privileges ke sath run kar sakta hai.

Is ka faida ye hai ke har waqt root account mein login rehne ki zaroorat nahi hoti.

### Sudo Command ka Syntax

```bash
sudo command
```

Yahan `command` ki jagah woh command likhi jati hai jise elevated privileges ki zaroorat ho.

### Example 1: Software Package Information Update

Ubuntu aur Debian based Linux mein:

```bash
sudo apt update
```

Ye package lists update karta hai. Ye command installed software ko khud se upgrade nahi karti.

### Example 2: System File Edit Karna

```bash
sudo nano /etc/hosts
```

Ye command system ki hosts file ko Nano editor mein open karne ki koshish karti hai.

File save karne se pehle changes ko carefully check karein.

### Example 3: Service Status Check Karna

```bash
sudo systemctl status ssh
```

Ye SSH service ka status check karta hai, agar service ka naam aur system configuration is command ke mutabiq hon.

### Sudo Password

Jab aap sudo command run karti hain, to system password mang sakta hai.

Password type karte waqt terminal par characters ya stars nazar na aana normal baat hai. Password type karke Enter press karein.

### Important Points

1. Sudo sirf authorized users use kar sakte hain.
2. Sudo password har configuration mein current user's password hota hai, root password zaroori nahi.
3. Sudo ke sath command run karne se pehle usay samajhna chahiye.
4. Har command ke sath sudo lagana zaroori nahi.
5. Sudo ke through run hone wali commands system mein important changes kar sakti hain.

## 7. File Permissions in Linux

### Definition

File permissions determine who can read, write or execute a file or directory.

### Urdu Explanation

Linux mein har file aur directory ki permissions hoti hain. Ye decide karti hain ke kaun file ko read, modify ya execute kar sakta hai.

### Three Main Permission Types

- **r (Read):** File ka content read karna.
- **w (Write):** File mein changes karna.
- **x (Execute):** File ko executable program ya script ke tor par run karna; directories mein enter/search karne ki permission bhi hoti hai.

### Three Permission Groups

- **u (User/Owner):** File ka owner.
- **g (Group):** File se associated group.
- **o (Others):** Baqi users.

### Permissions Check Karna

```bash
ls -l
```

Example output:

```text
-rw-r--r-- 1 student student 120 Oct 24 notes.txt
```

Is example mein owner read aur write kar sakta hai, jabke group aur others sirf read kar sakte hain.

### chmod Command

`chmod` file ya directory ki permissions change karne ke liye use hoti hai.

Example:

```bash
chmod 644 notes.txt
```

Is ka matlab:
- Owner: Read aur write.
- Group: Read only.
- Others: Read only.

Dusri example:

```bash
chmod u+x script.sh
```

Ye owner ko file execute karne ki permission add karti hai.

### chown Command

`chown` file ya directory ka owner change karne ke liye use hoti hai.

Example:

```bash
sudo chown student notes.txt
```

Ye command `notes.txt` ka owner `student` set karne ki koshish karti hai.

## 8. Linux Logs

### Definition

Logs are records of events and activities generated by an operating system, applications and services.

### Urdu Explanation

Logs system mein hone wali activities ka record hotay hain. In se pata lagaya ja sakta hai ke system mein kya hua, koi service kyun fail hui ya koi error kab aaya.

Logs troubleshooting, monitoring aur security investigation mein important role play karte hain.

### Logs ki Importance

1. System errors identify karna.
2. Login activities monitor karna.
3. Services ke issues troubleshoot karna.
4. Application errors samajhna.
5. Security-related events investigate karna.
6. System ki performance aur reliability improve karna.

### Common Types of Logs

- **System Logs:** Operating system ki activities.
- **Authentication Logs:** Login aur authentication events.
- **Application Logs:** Applications ki activities aur errors.
- **Kernel Logs:** Kernel se related messages.
- **Service Logs:** Kisi particular service ki activities.

### Common Log Directory

Linux mein aksar logs yahan milte hain:

```bash
/var/log
```

Logs ki files aur un ke names Linux distribution aur installed services ke mutabiq different ho sakte hain.

## 9. Logs Check Karne ki Commands

### 1. ls /var/log

Logs directory ki files aur folders show karta hai.

```bash
ls /var/log
```

### 2. journalctl

Systemd journal ke logs display karta hai.

```bash
journalctl
```

Latest log entries dekhne ke liye:

```bash
journalctl -n 50
```

Ye recent 50 journal entries display karta hai.

### 3. journalctl -b

Current boot se related journal entries display karta hai.

```bash
journalctl -b
```

### 4. dmesg

Kernel ke messages display karne ke liye use hota hai.

```bash
dmesg
```

System configuration ke mutabiq kuch messages dekhne ke liye elevated privileges ki zaroorat ho sakti hai.

### 5. tail

File ki last lines display karta hai.

```bash
tail /var/log/syslog
```

Ye command un systems par kaam karegi jahan `/var/log/syslog` file mojood ho.

Last 20 lines ke liye:

```bash
tail -n 20 /var/log/syslog
```

### 6. less

Bari log file ko page by page read karne ke liye:

```bash
less /var/log/syslog
```

Exit karne ke liye `q` press karein.

### 7. grep

Log file mein kisi specific word ko search karne ke liye:

```bash
grep "error" /var/log/syslog
```

Ye matching lines display karta hai, agar file mojood ho aur aapko access ho.

### 8. Authentication Logs

Kuch Debian aur Ubuntu systems mein authentication logs yahan hotay hain:

```bash
sudo less /var/log/auth.log
```

Kuch Red Hat based systems mein authentication information `/var/log/secure` mein ho sakti hai.

Agar ye files available na hon, to systemd journal check karein.

### 9. SSH Service Logs

Systemd use karne wale systems mein:

```bash
sudo journalctl -u ssh
```

Kuch distributions mein SSH service ka naam `sshd` hota hai:

```bash
sudo journalctl -u sshd
```

Sirf woh command use karein jo aapke system ki service ke naam se match karti ho.

## 10. Important Linux Commands

### 1. whoami

Current username display karta hai.

```bash
whoami
```

### 2. id

User ki UID, GID aur group information show karta hai.

```bash
id
```

### 3. sudo -l

Current user ke liye configured sudo permissions list karne ki koshish karta hai.

```bash
sudo -l
```

### 4. passwd

Apna password change karne ke liye:

```bash
passwd
```

### 5. su

Doosray user ka account switch karne ke liye use hota hai, agar authorization aur password requirements puri hon.

```bash
su username
```

Root account par switch karne ki command:

```bash
su -
```

Ye tabhi kaam karegi jab root account aur authentication configuration is ki ijazat dein.

### 6. uptime

System kitni dair se chal raha hai aur load average kya hai, ye show karta hai.

```bash
uptime
```

### 7. free -h

RAM aur swap usage show karta hai.

```bash
free -h
```

### 8. df -h

Filesystem ki disk space usage show karta hai.

```bash
df -h
```

### 9. ps aux

Running processes ki list display karta hai.

```bash
ps aux
```

### 10. top

Processes aur CPU/memory usage ko real time mein monitor karta hai.

```bash
top
```

Exit karne ke liye `q` press karein.

## 11. Practical Lab

Is practical lab mein basic commands ko safe tareeqay se practice karein.

### Step 1: Current User Check Karein

```bash
whoami
```

Maqsad: Pata lagana ke aap kis user ke account mein hain.

### Step 2: User Groups Check Karein

```bash
id
```

Maqsad: User ki UID, GID aur groups check karna.

### Step 3: Current Directory Check Karein

```bash
pwd
```

Maqsad: Current working directory maloom karna.

### Step 4: Files List Karein

```bash
ls -la
```

Maqsad: Current directory ki normal aur hidden files dekhna.

### Step 5: Logs Directory Dekhein

```bash
ls /var/log
```

Maqsad: System mein available log files ki listing dekhna.

### Step 6: Recent System Logs Check Karein

```bash
journalctl -n 20
```

Maqsad: Systemd journal ki recent entries dekhna.

### Step 7: Sudo Permissions Check Karein

```bash
sudo -l
```

Maqsad: Pata lagana ke current user ke liye kaun se sudo rules configured hain.

Note: Sirf authorized system par practice karein. Agar sudo access nahi hai, to administrator se permission lein.

## 12. Security Best Practices

1. Daily tasks ke liye normal user account use karein.
2. Sirf zaroorat ke waqt sudo use karein.
3. Unknown commands ko administrator privileges ke sath run na karein.
4. Password kisi ke sath share na karein.
5. File permissions ko carefully configure karein.
6. Logs ko regularly monitor karein.
7. Important logs ko bina samjhay delete ya modify na karein.
8. Software ko trusted repositories se install karein.
9. System ko update rakhein.
10. Sirf authorized systems par security testing karein.

## 13. Quick Revision

- **Root User:** Linux ka superuser account.
- **Normal User:** Limited permissions wala account.
- **User Level:** Normal user ki permissions ke mutabiq execution.
- **Root Level:** Administrative privileges ke sath execution.
- **Sudo:** Authorized user ko elevated privileges ke sath command run karne deta hai.
- **Permissions:** Files aur directories ke access rules.
- **Logs:** System aur applications ki activities ka record.
- **journalctl:** Systemd journal logs dekhne ki command.
- **dmesg:** Kernel messages display karta hai.
- **tail:** File ki last lines display karta hai.
- **grep:** Text ya log files mein matching content search karta hai.
- **whoami:** Current username show karta hai.
- **id:** User ID aur groups show karta hai.
- **chmod:** Permissions change karta hai.
- **chown:** File ownership change karta hai.

## 14. Conclusion

Root aur normal users ke darmiyan difference samajhna Linux security ke liye bohat zaroori hai. Sudo authorized users ko administrative tasks perform karne mein help karta hai, jabke logs system activities aur errors ko investigate karne ka tareeqa provide karte hain.

Linux commands ki regular practice se system administration, troubleshooting aur cybersecurity ki skills improve hoti hain.
