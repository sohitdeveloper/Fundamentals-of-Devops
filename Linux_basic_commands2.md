# Basic Linux Commands2
# Task: What is the linux command to

1. To view what's written in a file.
```
vim fileName
```
2. To change the access permissions of files.
```
chmod a+w+r+x fileName
```
`+ = add permission, - = remove permission, = = set permission explicitly, r = read, w = write, x = execute`

3. To check which commands you have run till now.
```
history
```
4. To remove a directory/ Folder.
```
rmdir folderName
```
5. To create a fruits.txt file and to view the content.
```
echo "fruit file created" > fruits.txt
```
6. Add content in devops.txt (One in each line) - Apple, Mango, Banana, Cherry, Kiwi, Orange, Guava.
```
vim devops.txt
i ~ (to go in insert mode)
```
now type the text as your normal editor
```
esc (press escape for exit from insert mode)
```
now it's time to save and exist
```
:wq (press enter for write and save)
```
7. To Show only top three fruits from the file.
```
head -n ${noOfLine} fileName
```
-n ~ number of line you want to echo from that file

8. To Show only bottom three fruits from the file.
```
tail -n 3 fileName
```
9. To create another file Colors.txt and to view the content.
```
touch Colors.txt && cat Colors.txt
```
10. Add content in Colors.txt (One in each line) - Red, Pink, White, Black, Blue, Orange, Purple, Grey.
```
vim Colors.txt
i
Red↩️
Pink↩️
White↩️
Black↩️
Blue↩️
Orange↩️
Purple↩️
Grey↩️
esc
:wq↩️
```
11. To find the difference between fruits.txt and Colors.txt file.
```
diff fruits.txt Colors.txt
```
