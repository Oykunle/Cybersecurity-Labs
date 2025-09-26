# Linux Lab

## Objective
Learn basic Linux commands and environment setup for cybersecurity tasks.

## Tools
- Ubuntu/Kali Linux terminal

## Commands / Steps Practiced

1. **pwd** – Print working directory  
```bash
pwd
```
Shows the current folder you are working in.

2. **ls -l** – List files with details (permissions, owner, size, etc.)  
```bash
ls -l
```
Helps see file rights and attributes.

3. **mkdir** – Make directory  
```bash
mkdir lab-practice
```
Creates a new folder.

4. **cd** – Change directory  
```bash
cd lab-practice
```
Moves you into another folder.

5. **touch** – Create empty file  
```bash
touch notes.txt
```
Creates a new file.

6. **chmod 644** – Change file permissions  
```bash
chmod 644 notes.txt
```
Sets: User = read/write, Group = read, Others = read.

7. **cat** – Display file content  
```bash
cat notes.txt
```
Prints the content of a file.

## Reflection (What I Learned)
- Learned how to navigate the Linux file system.  
- Understood file and folder permissions.  
- Practiced creating and managing files/folders in the terminal.

**==================================================================**


## Directory Permissions Lab

## Objective
Learn how to manage directories and their permissions in Linux.

## Commands / Steps Practiced

1. **mkdir** – Create a new directory  
```bash
mkdir lab-test
```
Creates a new folder called lab-test.

2. **ls -ld** – View directory permissions
```bash
ls -ld lab-test
```
Displays the directory details and permissions.

3. **chmod 750** – Change directory permissions  
```bash
sudo chmod 750 lab-test
```
Sets: Owner = read/write/execute, Group = read/execute, Others = no access.

4. **chown** – Change owner and group 
```bash
sudo chown kali:staff lab-test
```
Sets kali as owner and staff as the group.

5. **ls -ld** – Verify changes 
```bash
ls -ld lab-test
```
Confirm the new permissions and ownership.

## Reflection (What I Learned)
- Learned how to create directories in Linux.
- Understood directory permission levels (read, write, execute).
- Practiced changing ownership and verifying permissions.


**==================================================================**


## File Ownership and User Permissions Lab

## Objective

Learn how to manage file ownership and user/group permissions in Linux.

## Commands / Steps Practiced


1. **ls -l** – View file details including ownership
```bash
ls -l notes.txt
```
Shows the owner, group, and permissions of the file notes.txt.

2. **chown** – Change file owner and group
```bash
sudo chown kali:staff notes.txt
```
Sets kali as owner and staff as the group for notes.txt.

3. **chown (user only)** – Change only the owner
```bash
sudo chown oyetest notes.txt
```
Changes the owner to oyetest but keeps the group the same.

4. **chgrp** – Change the group only
```bash
sudo chgrp staff notes.txt
```
Changes the group of notes.txt to staff without affecting the owner.

## Reflection (What I Learned)
- Learned how to view file ownership in Linux.
- Understood the difference between user and group ownership.
- Practiced changing file ownership and verifying the changes.



**==================================================================**



## File Editing & Text Manipulation Lab

## Objective

Learn how to view, create, edit, 
and manage files in Linux using command-line
editors and text manipulation commands.

## Tools
	•	Ubuntu/Kali Linux terminal
	•	Text editors: nano, vim

## Commands / Steps Practiced


1. **nano** – Edit a file
```bash
nano notes.txt
```
Opens notes.txt in the nano editor.

2. **vim** – Edit a file  
```bash
vim notes.txt
```
Opens notes.txt in Vim editor.

3. **head** – View first lines of a file 
```bash
head notes.txt
```
Shows the first 10 lines of the file.

4. **tail** –  View last lines of a file
```bash
tail notes.txt
```
Shows the last 10 lines of the file.

5. **cat** – View full file content
```bash
cat notes.txt
```
Displays the complete file content.

6. **cp** –  Copy a file 
```bash
cp notes.txt notes_backup.txt
```
Creates a copy of the file called notes_backup.txt.

7. **mv** – Move or rename a file
```bash
mv notes.txt notes_old.txt
```
Renames or moves the file.

8. **rm** –  Delete a file
```bash
rm notes_old.txt
```
Removes the specified file.

## Reflection (What I Learned)
- Learned how to edit files using nano and vim.
- Practiced viewing file content with head, tail, and cat.
- Understood file operations like copy, move, and delete.



**==================================================================**



## Process Management in Linux

## Objective

Learn how to view, manage, and control processes in Linux, 
including monitoring resource usage, stopping processes, 
and adjusting their priority.

## Commands / Steps Practiced


1. **ps** – Show running processes
```bash
ps
ps aux
```
Displays current processes.
ps → shows your shell processes.
ps aux → shows all running processes with details (user, PID, CPU, memory).

2. **top** – live view processess
```bash
top
```
Displays processes dynamically with CPU/memory usage.
Press q to quit.

3. **kill** – Terminate a process
```bash
kill <PID>
kill -9 <PID>
```
Stops a process using its Process ID (PID).
-9 forces termination.

4. **jobs, fg, bg** –  Manage background/foreground jobs
```bash
sleep 100 &
jobs
fg %1
bg %1
```
& → runs a process in the background.
jobs → shows active jobs in the shell.
fg %1 → brings job 1 to foreground.
bg %1 → resumes job 1 in background.

5. **nice / renice** – Adjust process priority
```bash
nice -n 10 command
renice -n -5 -p <PID>
```
nice → starts a command with a given priority.
renice → changes priority of an existing process.
Range: -20 (highest priority) to 19 (lowest).



## Reflection (What I Learned)
- Learned how to find and monitor running processes.
- Understood how to kill or stop misbehaving applications.
- Practiced moving jobs between background and foreground.
- Learned to adjust process priority for better system performance.



**==================================================================**



## File Searching & Finding in Linux

## Objective

Learn how to search for files, directories, 
and content inside files using Linux commands.

## Commands / Steps Practiced


1. **find** – search for files and directories
```bash
find /home -name notes.txt
find . -type d -name "lab*"
```
Finds a file named notes.txt in /home.
Finds directories starting with lab in the current directory.

2. **locate** – Quickly search using file database
```bash
locate notes.txt
```
Faster than find because it searches a prebuilt database.
Run sudo updatedb to refresh the database.

3. **grep** – Search inside files for text patterns
```bash
grep "Linux" notes.txt
grep -r "password" /etc/
```
Searches for the word Linux in notes.txt.
Recursively searches for password in /etc/.

4. **which** –  Locate executable file path
```bash
which python3
```
Shows the full path of the command/program (e.g., /usr/bin/python3).

5. **whereis** – Locate binaries, source, and manual pages
```bash
whereis ls
```
Finds where the binary, source code, 
and man pages of ls are stored.

## Reflection (What I Learned)
- Learned how to search files and directories using find and locate.
- Understood how to search inside files with grep.
- Practiced locating executables with which and whereis.
- Gained skills for troubleshooting and finding system resources.



**==================================================================**



## Networking Basics in Linux

## Objective

Learn how to check network configurations, 
test connectivity, resolve domain names, 
trace network routes, and list open ports in Linux.

## Commands / Steps Practiced


1. **ip addr** – Show network interfaces and IP addresses
```bash
ip addr
```
Displays details of all network interfaces, 
IP addresses (IPv4 & IPv6), 
and MAC addresses.

2. **ping** – Test connectivity to another host
```bash
ping -c 5 facebook.com
```
Sends ICMP echo requests. Helps verify if a host/domain is reachable and measures response time.

3. **nslookup** – Query DNS records
```bash
nslookup facebook.com
```
Checks domain-to-IP mapping using DNS servers. 
Useful for troubleshooting name resolution.

4. **traceroute** –  Trace the path packets take to reach a destination
```bash
traceroute google.com
```
Shows each hop (router) between my computer and the target. 
Helps identify delays or failures in the network path.

5. **ss -tuln** – Show active network sockets
```bash
ss -tuln
```
Lists listening TCP/UDP ports and their associated IP addresses. 
Useful for checking open services and potential vulnerabilities.

## Reflection (What I Learned)
- Understood how to view IP addresses and interfaces with ip addr.
-  Learned to use ping for checking connectivity and latency.
- Practiced resolving domains with nslookup.
- Saw how traceroute maps out the journey of packets.
- Checked open ports with ss, important for system administration and security monitoring.

### Networking Checks (example outputs)

**Main interface**
- eth0 — 192.168.64.2/24 (from `ip addr`)

**Connectivity / Latency**
- `ping -c 5 facebook.com` → avg latency ~27.9 ms, 0% packet loss
- `ping -c 5 youtube.com` → avg latency ~31.9 ms, 0% packet loss

**DNS**
- `nslookup facebook.com` → Server: 192.168.64.1 (resolver), resolves to public IP(s)

**Path to Google**
- `traceroute google.com` → shows local gateway 192.168.64.1 then ISP hops and final Google hops (~25–30 ms)

**Open/listening services**
- `ss -tuln` shows:
  - SSH listening on `0.0.0.0:22` (network-accessible)
  - PostgreSQL (or DB) listening on `127.0.0.1:5432`, `127.0.0.1:5433` (local only)
  - Docker bridge `172.17.0.1/16` present
