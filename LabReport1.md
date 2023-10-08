# LabReport1
##For each of the commands cd, ls, and cat, and using the workspace you created in this lab:
1. Share an example of using the command with no arguments.
2. Share an example of using the command with a path to a directory as an argument.
3. Share an example of using the command with a path to a file as an argument.

##cd:
**1. cd with no arguments**
```
{
  [user@sahara ~]$ pwd
  /home
  [user@sahara ~]$ cd
  [user@sahara ~]$ pwd
  /home
}
```
- Printing the "cd" without arguments brings me back to the home directory, so it does nothing when I am not in a directory. 
- The working directory when the command runs is "/home."
- I got the output of noting because I cd brings me back to the home directory, and since I am in the home directory, it does nothing.
- The output is not an error.
**2. cd with a path to a directory as an argument**
```
{
  [user@sahara ~]$ pwd
  /home
  [user@sahara ~]$ cd /home/lecture1/messages
  [user@sahara ~/lecture1/messages]$ pwd
  /home/lecture1/messages
  [user@sahara ~/lecture1/messages]$ 
}
```
- Using cd with a path to a directory going to messages.
- The working directory when the command runs is "/home".
- I got the output "/home/lecture1/messages" because cd with a path changes the working directory from "home" to "messages". Therefore, it prints "/home/lecture1/messages".
- The output is not an error.

**3. cd with a path to a file as an argument**
```
{
  [user@sahara ~]$ pwd
  /home
  [user@sahara ~]$ cd /home/lecture1/messages/zh-cn.txt
  bash: cd: /home/lecture1/messages/zh-cn.txt: Not a directory
  [user@sahara ~]$ pwd
  /home
  [user@sahara ~]$ 
}
```
- Using cd with a path to a file as an argument going into a text file called "zh-cn.txt"
- The working directory when the command runs is "/home".
- I got the output of "bash: cd: /home/lecture1/messages/zh-cn.txt: Not a directory".  I got this because cd is for changing the current working directory  to the given path, but in this case, it is asked to go into a text file, which will cause issues and not recognize the code and work.
- Therefore, the output is an error because the command is for changing directory, not going into files, so it outputs the same directory from the beginning.

##cd:
**1. ls with no arguments**
```
{
  [user@sahara ~]$ pwd
  /home
  [user@sahara ~]$ ls
  lecture1
  [user@sahara ~]$ pwd
  /home
  [user@sahara ~]$ 
}
```
- The working directory when the command runs is "/home".
- I got the output of "lecture1" because ls is used to list the files and folder in the given path. Since I was on the path "/home" it showed me the list of files and folders in director, which only has "lecture1".
- This output is not an error.

**2. ls with a path to a directory as an argument**
