### Assignment 1 - Basic Shell Commands

Do the exercises below. *How to provided your answer is specificed in italics.* Copy your answer to a text file then save and submit this text file as your completed assignment. You may use plain text (.txt) or Markdown (.md) format. Please name your file `1_first_last.txt` or `1_first_last.md` (substitute your first and last name).

#### A. Basic commands

1. Navigate to your working directory for the class.
2. Within that directory, create a temporary test directory.
3. Create a file using one method I showed you.
4. Create a file using a different method I showed you.
5. Rename one of the files.
6. Copy one of the files.
7. Delete one of the files.
8. Delete the temporary directory.
9. Get a list of the commands you've typed already.
10. See which processes are running on your computer.

*Copy your terminal commands and output as your answers.*

#### B. Working with commands

1. Pick a command from class. Using a Unix command to find out, what does this command do?
2. Pick a command from class. Using a Google search to find out, what does this command do?
3. Where are the commands `mv` and `cp` are located on your computer?
4. What happens when you type `Tab` in the middle of typing a command?
5. What happens when you type `Tab` in the middle of typing a file name or path?

*Write your answers.*

#### C. Setting up your bash environment

1. Download a text editor such as [Atom](https://atom.io) or [Sublime Text](https://www.sublimetext.com) if you haven't already.
2. Using your text editor, customize your terminal by editing the file `.bash_profile` in your home directory. Alternatively, you can edit the file `.bashrc` in your home directory and have it automatically sourced by `.bash_profile` (see Lesson 2).
3. Source your bash profile file with the command `source ~/.bash_profile`.
4. Open a new terminal to make sure it automatically sources your bash profile file. You may have to change the preferences in the Terminal app.

*No answers need be submitted.*

#### D. More commands

1. Print the first 5 lines of a text file.
2. Print the last 10 commands you entered.
3. View the contents of a file without printing anything to the screen.
4. Open a file in its designated application.
5. Determine the kind/type of a file.
6. Search for a word in a file.
7. Get only the third column of a tab-delimited file. (To insert a tab character, type `Ctrl-V` and then `Tab`.)
8. Using a different method, get the first field of a tab-delimited file and save it as a new file.

*Copy your terminal commands and output as your answers.*

#### E. Paths and variables

1. Navigate to root and home directories using absolute paths.
2. Navigate to root and home directories using relative paths.
3. Store an integer as a shell variable then print it.
4. Store a file name as a shell variable.
5. Print your current path variable.
6. Print your home directory.
7. Write a `for` loop to count to 10.

*Copy your terminal commands and output as your answers.*

#### F. Executing bash scripts and dot-files

1. Write a bash script that uses the commands `mkdir`, `cat`, `mv`, `echo`, and a `for` loop.
2. Execute your bash script using the terminal.


```
A.
$ cd ~/sio209
$ mkdir test
$ cd test
$ cat > file1
I am creating a file using cat.
^C
$ touch file2
$ nano file2
(add text using nano)
$ mv file2 file3
$ cp file1 file2
$ rm file1
$ cd ..
$ rm -r test
$ history
$ top

B
1. `cd` – Unix commands `man cd`, `help cd`, and `cd --help` will tell us what `cd` does, which is to change directories in different ways.
2. `ls` – Googling "unix command ls" tells us how the `ls` command works to list directory contents.
3. The commands `which mv` and `which cp` tell us that these commands are in `/bin` on our computer.
4. Typing `Tab` in the middle of a command attemps to complete the command we are writing.
5. Typing `Tab` in the middle of a file name or path attemps to complete the file name or path we are writing.

C

D
$ head -n 5 FILE
$ history | tail
$ less FILE
$ open FILE
$ file FILE
$ grep WORD FILE
$ cut -d '    ' -f 3 FILE
$ cat FILE | awk '{FS="\t"}; {print $3}' > NEWFILE
$ cat FILE | perl -alne 'print $F[2]' > NEWFILE

E
$ cd /
$ cd /Users/luke
$ cd ../..
$ cd ~
$ A=5
$ echo $A
$ B='myfile.txt'
$ echo $PATH
$ echo $HOME
$ for i in {1..10}; do echo $i; done

F
# myscript.sh
mkdir tempdir
cd tempdir
echo "text here" > myfile
cat myfile
mv myfile myfile2
for i in line1 line2 line3
do
    echo $i >> myfile2
done
cat myfile2
```
