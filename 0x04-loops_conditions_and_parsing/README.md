0x04. Loops, conditions and parsing
Resources📚
Read or watch:

Loops sample
Variable assignment and arithmetic
Comparison operators
File test operators
Make your scripts portable
Learning Objectives💡
What you should learn from this project:

How to create SSH keys
What is the advantage of using #!/usr/bin/env bash over #!/bin/bash
How to use while, until and for loops
How to use if, else, elif and case condition statements
How to use the cut command
What are files and other comparison operators, and how to use them
man or help:

env
cut
for
while
until
if
Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google: General

How to create SSH keys
What is the advantage of using #!/usr/bin/env bash over #!/bin/bash
How to use while, until and for loops
How to use if, else, elif and case condition statements
How to use the cut command
What are files and other comparison operators, and how to use them
General Requirements
Allowed editors: vi, vim, emacs
All your files will be interpreted on Ubuntu 14.04 LTS
All your files should end with a new line
A README.md file, at the root of the folder of the project, is mandatory
All your Bash script files must be executable
You are not allowed to use awk
Your Bash script must pass Shellcheck (version 0.3.3-1~ubuntu14.04.1 via apt-get) without any error
The first line of all your Bash scripts should be exactly #!/usr/bin/env bash
The second line of all your Bash scripts should be a comment explaining what is the script doing
Watch this:
What is a server?
What is data center?
Read this:
Server
What is Virtual MAchine (VM)
What are Containers and why do you nedd them?
Shellcheck
Shellcheck is a tool that will help you write proper Bash scripts. It will make recommendations on your syntax and semantics and provide advice on edge cases that you might not have thought about. Shellcheck is your friend! All your Bash scripts must pass Shellcheck without any error or you will not get any points on the task.

To install Shellcheck type:

sudo apt-get install shellcheck
For every feedback, Shellcheck will provide a code that you can use to get more information about the issue, for example for code SC2034, you can browse SC2034.

Shell
System engineering & DevOps

Manpage
Most of Unix systems are managed by using Shell. Just as you need to know a minimum number of words to have a discussion in a language, you need to know a minimum number of commands to be able to easily interact with a system. Unix systems all have, sometimes with slight differences, the same set of commands. While it is not too hard to remember commands, it might be hard to remember all of their options and how exactly to use them. The solution to this is the man command. Let’s go through a part of the ssh one, as there are few elements to know to be able to read a man page:

NAME
ssh — OpenSSH SSH client (remote login program)

SYNOPSIS
ssh [-1246AaCfgKkMNnqsTtVvXxYy] [-b bind_address] [-c cipher_spec] [-D [bind_address:]port] [-E log_file] [-e escape_char] [-F configfile] [-I pkcs11] [-i identity_file] [-L [bind_address:]port:host:hostport] [-l login_name] [-m mac_spec] [-O ctl_cmd] [-o option] [-p port]
[-Q cipher | cipher-auth | mac | kex | key] [-R [bind_address:]port:host:hostport] [-S ctl_path] [-W host:port] [-w local_tun[:remote_tun]] [user@]hostname [command]

DESCRIPTION
ssh (SSH client) is a program for logging into a remote machine and for executing commands on a remote machine. It is intended to replace rlogin and rsh, and provide secure encrypted communications between two untrusted hosts over an insecure network. X11 connections and arbitrary TCP ports can also be forwarded over the secure channel.
Some tips:
The NAME will summarize what the command is doing. As it is usually super short, you might want to look at DESCRIPTION (bellow) if ever it does not gives clear enough information
The SYNOPSIS will help you to understand the structure of the command:
   A shell command usually have this format: command options parameters
   Options inside [] are optional
   The string without [] are mandatory
ssh [-1246AaCfgKkMNnqsTtVvXxYy] [-D [bind_address:]port]
   ssh is mandatory
       -1246AaCfgKkMNnqsTtVvXxYy is optional
       -D [bind_address:]port is optional (with bind_address: being itself optional within -D [bind_address:]port
Commands
Here is the (non-exhaustive) list of commands & concepts you should master to be verbose with Unix systems:

awk # pattern scanning and processing language
basename # strip directory and suffix from filenames
bg # resumes suspended jobs without bringing them to the foreground
cat # print files
cd # change the shell working directory.
chmod # change file mode
chown # change file owner and group
crontab # maintain crontab files
curl # transfer a URL
cut # remove sections from each line of files
date # display or set date and time
dig # DNS lookup utility
df # report file system disk space usage
diff # compare files line by line
du # estimate file space usage
echo # display a line of text
find # search for files in a directory hierarchy
fg # resumes suspended jobs and bring them to the foreground
grep # print lines matching a pattern
kill # send a signal to a process
less # read file with pagination
ln # create links
ls # list directory contents
lsb_release # print distribution-specific information
lsof # list open files
mkdir # create
mv # move files
nc # arbitrary TCP and UDP connections and listens
netstat # print network connections, routing tables, interface statistics...
nice # execute a utility with an altered scheduling priority
nproc # print the number of processing units available
passwd # change user password
pgrep # look up processes based on name and other attributes
pkill # send signal to processes based on name and other attributes
printenv # print all or part of environment
pwd # print name of current/working directory
top # display Linux processes
tr # translate or delete characters
ps # report a snapshot of the current processes
rm # remove files or directories
rmdir # remove directories
rsync # remote file copy
scp # secure copy (remote file copy program)
sed # stream editor for filtering and transforming text
sleep # suspend execution for an interval of time
sort # sort lines of text file
ssh # OpenSSH SSH client (remote login program)
ssh-keygen # SSH key generation, management and conversion
su # substitute user identity
sudo # execute a command as another user
tail # output the last part of files
tar # manipulate archives files
tr # translate or delete characters
uname # Print operating system name
uniq # report or omit repeated lines
uptime # show how long system has been running
w # Show who is logged on and what they are doing
whereis # locate the binary, source, and manual page files for a command
which # locate a command
wc # print newline, word, and byte counts for each file
xargs # build and execute command lines from standard input
| # redirect standard output to another command
> # redirect standard output
< # redirect standard input
& # send process to background
Shortcuts
Some handy shortcuts:

CTRL+A # go to beginning of line
CTRL+B # moves backward one character
CTRL+C # stops the current command
CTRL+D # deletes one character backward or logs out of current session
CTRL+E # go to end of line
CTRL+F # moves forward one character
CTRL+G # aborts the current editing command and ring the terminal bell
CTRL+K # deletes (kill) forward to end of line
CTRL+L # clears screen and redisplay the line
CTRL+N # next line in command history
CTRL+R # searches in your command history
CTRL+T # transposes two characters
CTRL+U # kills backward to the beginning of line
CTRL+W # kills the word behind the cursor
CTRL+Y # retrieves last deleted string
CTRL+Z # stops the current command, resume with fg in the foreground or bg in the background
0. Create a SSH RSA key pair
Read for this task:

How do I set up SSH authentication keys in Linux or Mac?
How do I set up SSH authentication keys in Windows?
man: ssh-keygen

You will soon have to manage your own servers hosted on remote data centers. We need to set them up with your RSA public key so that you can access them via SSH.

Create a RSA key pair.

Requirements:

Keep the private key to yourself in a secure location, you will use it later to connect to your servers using SSH. Some storing ideas are Dropbox, Google Drive, password manager, USB key. Failing to do so will prevent you to access your servers, which will prevent you from doing your projects.
If you decide to add a passphrase to your key, make sure to save this passphrase in a secure location, you will not be able to use your keys without the passphrase
SSH and RSA keys will be covered in depth in a later project.

when you generate an rsa key two files are generated: "id_rsa", "id_rsa.pub":

"id_rsa.pub" is the public key, It is the one that we are going to use at point 0 of the project, we must change its name.
"id_rsa": It is the private key and it is the one that must be kept in a confident place
1. For Holberton School loop
Write a Bash script that displays Holberton School 10 times.

You must use the for loop (while and until are forbidden)

sylvain@ubuntu$ head -n 2 1-for_holberton_school 
#!/usr/bin/env bash
# This script is displaying "Holberton School" 10 times
sylvain@ubuntu$ ./1-for_holberton_school 
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
sylvain@ubuntu$ 
Note that:

The first line of my Bash script starts with #!/usr/bin/env bash (To be portable).
The second line of my Bash scripts is a comment explaining what it is doing.
2. While Holberton School loop
Write a Bash script that displays Holberton School 10 times.

You must use the while loop (for and until are forbidden)

sylvain@ubuntu$ ./2-while_holberton_school
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
sylvain@ubuntu$ 
3. Until Holberton School loop
Write a Bash script that displays Holberton School 10 times.

You must use the until loop (for and while are forbidden)

sylvain@ubuntu$ ./3-until_holberton_school
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
sylvain@ubuntu$ 
4. If 9, say Hi!
Write a Bash script that displays Holberton School 10 times, but for the 9th iteration, displays Holberton School and then Hi on a new line.

You must use the while loop (for and until are forbidden)

You must use the if statement

sylvain@ubuntu$ ./4-if_9_say_hi
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Holberton School
Hi
Holberton School
sylvain@ubuntu$ 
5. 4 bad luck, 8 is your chance
Write a Bash script that loops from 1 to 10 and:

displays bad luck for the 4th loop iteration

displays good luck for the 8th loop iteration

displays Holberton School for the other iterations

Requirements:

You must use the while loop (for and until are forbidden)
You must use the if, elif and else statements
sylvain@ubuntu$ ./5-4_bad_luck_8_is_your_chance
Holberton School
Holberton School
Holberton School
bad luck
Holberton School
Holberton School
Holberton School
good luck
Holberton School
Holberton School
sylvain@ubuntu$ 
For the most curious:

8 in the Chinese culture
4 in the Chinese culture
6. Superstitious numbers
Write a Bash script that displays numbers from 1 to 20 and:

displays 4 and then bad luck from China for the 4th loop iteration

displays 9 and then bad luck from Japan for the 9th loop iteration

displays 17 and then bad luck from Italy for the 17th loop iteration

Requirements:

You must use the while loop (for and until are forbidden)
You must use the case statement
sylvain@ubuntu$ ./6-superstitious_numbers
1
2
3
4
bad luck from China
5
6
7
8
9
bad luck from Japan
10
11
12
13
14
15
16
17
bad luck from Italy
18
19
20
sylvain@ubuntu$ 
7. Clock
Write a Bash script that displays the time for 12 hours and 59 minutes:

display hours from 0 to 12

display minutes from 1 to 59

Requirements:

You must use the while loop (for and until are forbidden)
Note that in this example, we only display the first 70 lines using the head command.

sylvain@ubuntu$ ./7-clock | head -n 70
Hour: 0
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
54
55
56
57
58
59
Hour: 1
1
2
3
4
5
6
7
8
9
sylvain@ubuntu$ 
8. For ls
Write a Bash script that displays:

The content of the current directory

