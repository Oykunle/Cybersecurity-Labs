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

  
---------------------------------------------------------------------------------------------------------------------------------------



## Directory Permissions Lab

### Objective
Learn how to manage directories and their permissions in Linux.

### Commands / Steps Practiced

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

