# Lecture 06 — File Read, echo, Operators aur Wildcards

## 1. Introduction

Linux aik powerful operating system hai jo servers, networking aur cybersecurity mein use hota hai.

Linux mein terminal ke through hum different commands execute karte hain.

Is lecture mein hum seekhein ge:

- File Reading Commands
- cat Command
- less Command
- head Command
- tail Command
- echo Command
- Redirection Operators
- Logical Operators
- Pipe Operator
- Wildcards
- Practical Lab

# 2. File Reading in Linux

## What is File Reading?

File Reading ka matlab kisi file ke andar mojood information ko read ya display karna hai.

Linux mein files read karne ke liye different commands use hoti hain.

## 2.1 cat Command

Definition:

The cat command is used to display the complete content of a file.

cat command file ke andar mojood complete text terminal par show karti hai.

Syntax:

cat filename

Example:

cat notes.txt

Agar notes.txt file mein Linux ke notes likhe hain to cat command tamam notes display karegi.

Multiple files read karna:

cat file1.txt file2.txt

Uses:

- File content read karna.
- Multiple files ka content display karna.
- Files ko combine karke output show karna.

## 2.2 less Command

Definition:

The less command is used to view file content one page at a time.

less command large files ko easily read karne ke liye use hoti hai.

Command:

less notes.txt

Useful Keys:

- Space = Next page
- b = Previous page
- Enter = Next line
- q = Exit

Example:

less /var/log/syslog

Is command se system log file ko page by page read kiya ja sakta hai, agar file available ho.

## 2.3 head Command

Definition:

The head command displays the first lines of a file.

head command file ki starting lines show karti hai.

By default first 10 lines display hoti hain.

Command:

head notes.txt

First 5 lines:

head -n 5 notes.txt

Uses:

- File ki starting information check karna.
- Large files ka beginning part read karna.
- Log files ki initial entries dekhna.

## 2.4 tail Command

Definition:

The tail command displays the last lines of a file.

tail command file ki last lines show karti hai.

By default last 10 lines display hoti hain.

Command:

tail notes.txt

Last 5 lines:

tail -n 5 notes.txt

Live log monitoring:

tail -f /var/log/syslog

Ye command new log entries ko live display karti hai, agar file available aur readable ho.

# 3. echo Command

## What is echo?

Definition:

The echo command is used to display text or variable values on the terminal.

echo command terminal par message ya text display karti hai.

Example:

echo "Hello World"

Output:

Hello World

## 3.1 Display a Message

Command:

echo "Welcome to Linux"

Output:

Welcome to Linux

## 3.2 Save Text in a File

Command:

echo "My First Linux File" > notes.txt

Ye command notes.txt file mein text write karti hai.

Agar file already exist karti hai to us ka purana content overwrite ho jata hai.

## 3.3 Append Text in a File

Command:

echo "Learning Linux Commands" >> notes.txt

Ye command file ke end mein new text add karti hai.

Purana content delete nahi hota.

## 3.4 Display Variables

Example:

name="Student"

echo $name

Output:

Student

Yahan $name variable ki value display karta hai.

# 4. Redirection Operators

## What is Redirection?

Definition:

Redirection is used to change the input or output destination of a command.

Redirection ka matlab command ke input ya output ko kisi doosri location par send karna hai.

## 4.1 Greater Than (>)

Ye operator command ka output file mein save karta hai.

Example:

echo "Hello Linux" > file.txt

Important:

Agar file pehle se exist karti hai to us ka purana content overwrite ho jata hai.

## 4.2 Double Greater Than (>>)

Ye operator file ke end mein new content add karta hai.

Example:

echo "New Linux Lesson" >> file.txt

Isay append operator bhi kehte hain.

## 4.3 Less Than (<)

Ye operator file ko command ke input ke taur par use karta hai.

Example:

sort < names.txt

Ye names.txt ka content sort command ko input deta hai.

## 4.4 Error Redirection (2>)

Ye operator command ki error output ko file mein save karta hai.

Example:

ls unknownfolder 2> error.txt

Agar folder exist nahi karta to error message error.txt mein save hoga.

## 4.5 Output and Error Redirection

Example:

command > output.txt 2> error.txt

Is mein normal output output.txt mein aur errors error.txt mein save hote hain.

# 5. Pipe Operator (|)

Definition:

The pipe operator sends the output of one command as input to another command.

Pipe operator aik command ka output doosri command ka input bana deta hai.

Example:

ls | less

Is command mein ls ki output less command ke through display hoti hai.

Another Example:

cat notes.txt | wc -l

Ye file mein lines ki total quantity count karta hai.

Example:

ps aux | grep apache

Ye process list mein apache se related entries search karta hai.

# 6. Logical Operators

Logical operators multiple commands ko conditions ke according execute karte hain.

## 6.1 AND Operator (&&)

Definition:

The AND operator executes the second command only if the first command succeeds.

Agar first command successful ho tabhi second command execute hoti hai.

Example:

mkdir myfolder && cd myfolder

Explanation:

1. Pehle myfolder create hoga.
2. Agar folder successfully create ho gaya to cd command execute hogi.
3. Terminal myfolder ke andar chala jayega.

## 6.2 OR Operator (||)

Definition:

The OR operator executes the second command only if the first command fails.

Agar first command fail ho jaye to second command execute hoti hai.

Example:

cd myfolder || echo "Folder not found"

Agar folder open nahi hota to error message display hoga.

## 6.3 Semicolon (;)

Semicolon multiple commands ko sequence mein execute karta hai.

Example:

date; pwd; whoami

Explanation:

- date current date aur time show karta hai.
- pwd current directory show karta hai.
- whoami current username show karta hai.

Pehli command fail ho tab bhi baqi commands execute hoti hain.

## 6.4 NOT Operator (!)

Bash mein ! command ke exit status ko reverse karta hai.

Example:

! false

Ye successful status return karta hai kyun ke false command unsuccessful status return karti hai.

# 7. Wildcards in Linux

## What are Wildcards?

Definition:

Wildcards are special characters used to match filenames and patterns in Linux.

Wildcards ka use files ko un ke names ya patterns ke through search aur select karne ke liye hota hai.

Linux mein common wildcards:

- *
- ?
- []

## 7.1 Asterisk (*)

Asterisk zero ya more characters ko match karta hai.

Example:

ls *.txt

Ye current directory mein tamam .txt files show karega.

Another Example:

ls file*

Ye un files ko show karega jin ke names file se start hote hain.

## 7.2 Question Mark (?)

Question mark exactly one character ko match karta hai.

Example:

ls file?.txt

Ye following files match kar sakta hai:

- file1.txt
- file2.txt
- fileA.txt

Lekin file10.txt match nahi hogi kyun ke ? sirf aik character match karta hai.

## 7.3 Square Brackets ([])

Square brackets given characters mein se kisi aik character ko match karte hain.

Example:

ls file[123].txt

Ye following files match kar sakta hai:

- file1.txt
- file2.txt
- file3.txt

## 7.4 Character Range

Square brackets mein range bhi use kar sakte hain.

Example:

ls file[1-5].txt

Ye file1.txt se file5.txt tak matching files show karega.

Another Example:

ls [a-z]*

Ye lowercase English letter se start hone wale filenames match kar sakta hai.

# 8. Difference Between Wildcards

| Wildcard | Meaning | Example |
|----------|---------|---------|
| * | Zero or more characters | *.txt |
| ? | Exactly one character | file?.txt |
| [] | Given characters mein se one | file[123].txt |
| [1-5] | Range mein se one character | file[1-5].txt |

# 9. Practical Linux Lab

Ab hum practical commands execute karein ge.

## Step 1: Create a Directory

mkdir LinuxPractice

## Step 2: Open Directory

cd LinuxPractice

## Step 3: Create a File

touch notes.txt

## Step 4: Write Text in File

echo "Welcome to Linux" > notes.txt

## Step 5: Read File

cat notes.txt

## Step 6: Add More Text

echo "Linux is an operating system" >> notes.txt

## Step 7: Display First Line

head -n 1 notes.txt

## Step 8: Display Last Line

tail -n 1 notes.txt

## Step 9: Display Complete File

cat notes.txt

## Step 10: Create Multiple Files

touch file1.txt file2.txt file3.txt

## Step 11: Use Wildcard

ls *.txt

## Step 12: Use Pipe

ls | less

## Step 13: Check Current Directory

pwd

# 10. Important Differences

## cat vs less

cat complete file content display karta hai.

less file ko page by page display karta hai.

## head vs tail

head file ki starting lines show karta hai.

tail file ki ending lines show karta hai.

## > vs >>

> purana content overwrite karta hai.

>> file ke end mein new content add karta hai.

## && vs ||

&& second command tab execute karta hai jab first successful ho.

|| second command tab execute karta hai jab first fail ho.

# 11. Important Interview Questions

Q1: What is the cat command?

Answer: It displays the complete content of a file.

Q2: What is the less command?

Answer: It displays file content one page at a time.

Q3: What is the head command?

Answer: It displays the first lines of a file.

Q4: What is the tail command?

Answer: It displays the last lines of a file.

Q5: What is the echo command?

Answer: It displays text or variable values on the terminal.

Q6: What is the difference between > and >>?

Answer: > overwrites content, while >> appends new content.

Q7: What is a pipe operator?

Answer: It sends one command's output as input to another command.

Q8: What is the purpose of &&?

Answer: It executes the next command only if the previous command succeeds.

Q9: What is the purpose of ||?

Answer: It executes the next command only if the previous command fails.

Q10: What are wildcards?

Answer: Wildcards are special characters used to match filename patterns.

Q11: What does * mean?

Answer: It matches zero or more characters.

Q12: What does ? mean?

Answer: It matches exactly one character.

# 12. Conclusion

Is lecture mein hum ne Linux ki important commands aur operators seekhe.

Hum ne cat, less, head aur tail ke through files read karna seekha.

echo command ke through text display aur file mein save karna seekha.

Redirection operators ke through output aur input manage karna seekha.

&&, || aur ; ke through multiple commands execute karna seekha.

Wildcards ke through files ko patterns ki help se search karna seekha.

Ye tamam commands Linux Fundamentals aur System Administration ke liye bohat important hain.
