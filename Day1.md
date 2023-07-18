# Day 1 Task: 

1. how to check your present working directory.
```
pwd
```
2. List all the files or directories including hidden files.
```
ls -a
```
3. Create a nested directory env/test/frontend (directory inside directory)
```
mkdir -p env/test/frontend
```
4. List all the files having .sh extension
```
ls *.sh 
```
5. List the files and directories with index numbers Inodes.
```
ls -i
```
6. List only directories.(we can also specify a pattern)
```
ls -d */
```
7. Make a hidden directory (also . before a file to make it hidden).
```
mkdir .HideMe 
```
## Commonly Used Linux commands:
```bash
sudo (command)       #lets you perform tasks that require administrative or root permissions.

pwd [option]         #To find path of your current working directory

cat filename.txt.    #It lists, combines, and writes file content to the standard output.

cp filename1.txt filename2.txt    #to copy files or directories and their content.

touch /home/username.html     #to create an empty file or generate and modify a timestamp in the Linux command line.

locate -i school*note   #find a file in the database system.

grep blue notepad.txt   #to find a word by searching through all the texts in a specific file.

df -h     #to report the system’s disk space usage, shown in percentage and kilobyte (KB).

du /home/user/Documents  #to check how much space a file or a directory takes up

head note.txt         # to view the first ten lines of a text

tail -n colors.txt      #to displays the last ten lines of a file.

diff note.txt note_update.txt       #the diff command compares two contents of a file line by line.

tar -cvf newarchive.tar /home/user/Documents    #archives multiple files into a TAR file – a common Linux format similar to ZIP, with optional compression.

chmod 777 note.txt #to modifies a file or directory’s read, write, and execute permissions.

kill SIGKILL 63773    # to terminate an unresponsive program manually.

ping google.com     #for checking whether a network or a server is reachable.
