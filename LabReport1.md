# LabReport1
##For each of the commands cd, ls, and cat, and using the workspace you created in this lab:
1. Share an example of using the command with no arguments.
2. Share an example of using the command with a path to a directory as an argument.
3. Share an example of using the command with a path to a file as an argument.

## cd:
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

## ls:
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
- I got the output of "lecture1" because ls is used to list the files and folder in the given path. Since I was on the path "/home", it showed me the list of files and folders in director, which only has "lecture1".
- This output is not an error.

**2. ls with a path to a directory as an argument**
```
{
  [user@sahara ~]$ pwd
  /home
  [user@sahara ~]$ ls /home/lecture1/messages
  en-us.txt  es-mx.txt  ko.txt  zh-cn.txt
  [user@sahara ~]$ pwd
  /home
  [user@sahara ~]$
}
```
- Using ls with a path to a directory as an argument into the message folder.
- The working directory when the command runs is "/home".
- I got the output of "en-us.txt  es-mx.txt  ko.txt  zh-cn.txt", this shows that ls shows me the list of the files in the folder in the director that I chose, which is the message folder containing the four language text files.
- The working directory at the end is still "/home" because it only gets the list that I need without changing the directory.

**3. ls with a path to a file as an argument**
```
{
  [user@sahara ~]$ pwd
  /home
  [user@sahara ~]$ ls /home/lecture1/messages/zh-cn.txt
  /home/lecture1/messages/zh-cn.txt
  [user@sahara ~]$ pwd
  /home
  [user@sahara ~]$ 
}
```
- Using ls with a path to a file called "zh-cn.txt" in the folder "messages".
- The working directory when the command runs is "/home".
- I got the output of "/home/lecture1/messages/zh-cn.txt", this is because ls can only show the the list of files or folders in the directory, which, in this case, it is asked to show the list in a file that caused an error.
- Therefore, the output is an error because it can not show the list in a file and causes it to output the directory it is asked to show.

## cat:
**1. cat with no arguments**
```
  {
  [user@sahara ~]$ pwd
  /home
  [user@sahara ~]$ cat
}
```
- The working directory when the command runs is "/home".
- I did not get an output because when I use "cat" without any arguments, the command will only read the data from the input and write them as an output.
This is the output if I use cat and type something else:
```
{
  [user@sahara ~]$ pwd
  /home
  [user@sahara ~]$ cat
  it just repeats what I type
  it just repeats what I type
}
```
> This shows that it only repeats what I type, which I input "it just repeats what I type" and outputs "it just repeats what I type". And can't stop, as explained above.
- This is not an error because it is asked to read the input and output the same thing.

**2. cat with a path to a directory as an argument**
```
{
  [user@sahara ~]$ pwd
  /home
  [user@sahara ~]$ cat /home/lecture1/messages
  cat: /home/lecture1/messages: Is a directory
  [user@sahara ~]$ pwd
  /home
  [user@sahara ~]$ 
}
```
- Using cat with a path to the directory "messages".
- The working directory when the command runs is "/home".
- The output is "cat: /home/lecture1/messages: Is a directory". This is because "cat" is used to print the contents of the files in the given path. In this case, it is asked to print the content of a directory, which causes an error.
- Therefore, the output is an error and prints "Is a directory", showing that it is not a file and can not print the contents.

**3. cat with a path to a file as an argument**
```
{
  [user@sahara ~]$ pwd
  /home
  [user@sahara ~]$ cat /home/lecture1/Hello.java
  import java.io.IOException;
  import java.nio.charset.StandardCharsets;
  import java.nio.file.Files;
  import java.nio.file.Path;
  
  public class Hello {
    public static void main(String[] args) throws IOException {
      String content = Files.readString(Path.of(args[0]), StandardCharsets.UTF_8);    
      System.out.println(content);
    }
  }[user@sahara ~]$ pwd
  /home
  [user@sahara ~]$ 
}
```
- Using cat with a path to a file called "Hello.java"
- The working directory when the command runs is "/home".
- I got the output of the coding that was in the file "Hello.java". This is because "cat" can print out the contents of one or more files in the given path.
- This is not an error; the working directory is still "/home".
