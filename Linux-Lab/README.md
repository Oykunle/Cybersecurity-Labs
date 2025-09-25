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


##Directory Permissions Lab

##Objective
Learn how to manage directories and their permissions in Linux.

##Commands / Steps Practiced

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


##File Ownership and User Permissions Lab

##Objective

Learn how to manage file ownership and user/group permissions in Linux.

##Commands / Steps Practiced


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

Reflection (What I Learned)
	-	Learned how to view file ownership in Linux.
	-	Understood the difference between user and group ownership.
	-	Practiced changing file ownership and verifying the changes.



**==================================================================**



##File Editing & Text Manipulation Lab

##Objective

Learn how to view, create, edit, and manage files in Linux using command-line editors and text manipulation commands.

##Tools
	•	Ubuntu/Kali Linux terminal
	•	Text editors: nano, vim

##Commands / Steps Practiced


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

Reflection (What I Learned)
	- Learned how to edit files using nano and vim.
	- Practiced viewing file content with head, tail, and cat.
	- Understood file operations like copy, move, and delete.
