# FILE MANIPULATION

## 1. `sudo` Command
This command is used to update the package lists for available software packages from the configured repositories. I used ***sudo apt upgrade***.

![`sudo`](<Images/1. sudo command.PNG>)


## 2. `pwd` command
pwd means Print Working Directory. it prints the path of the working directory, starting with the root.
pwd command does not have any argument or options, but it can accept flags for specific behavior like -L and -P.
I used the following; 
- ***pwd -L*** :This command was used to obtain the symbolic path of my directory containing a symbolic link.
- ***pwd -P*** :This command was used to display the actual path, ignoring symbolic links.

![`pwd`](<Images/2. pwd command.PNG>)


## 3. `cd` command
cd command in linux known as the change directory command, is used to move from the current working directory to different directories in our system. the following syntax was used.

- ***cd BreakFast*** :This command was used to the move into the ***BreakFast*** directory 
   - ***cd OgiMoiMoi*** :This command was used to move into the ***OgiMoiMoi*** which is a subdirectory in the BreakFast directory
   - ***cd MoiMoiRecipe*** : This command was used to move into the ***MoiMoiRecipe*** which is a subdirectory in the ***OgiMoiMoi*** subdirectory
- ***cd ..*** :This command was used to move up to the ***OgiMoiMoi*** subdirectory.
- ***cd -*** :This command was used to move to the previous directory.
- ***cd~*** :This command was used to move back to the home directory
- ***cd /home/olalonpei/Lunch*** :This command was used move to the Lunch directory

![`cd`](<Images/3. cd command.PNG>)


## 4. `ls` command
ls a linux command that lists directory contents of files and directories. it provided valuable information about files, directories, and their atrributes. ls command also lists files and directories in alphabetical order. The following command was used;


- ***ls -a*** :This command was used to display all the hidden files in the home directory
- ***ls -lh*** :This command was used to display file size in easy to read format i.e M for MB, K for KB, G for GB
- ***ls -R*** :This command was used to list/display files and directories recursively, including subdirectories.
- ***ls*** :This command was used to display contents in the home directory

![`ls -a`](<Images/4. ls -a command.PNG>)
![`ls -lh`](<Images/4. ls -lh comand.PNG>)
![`ls -R`](<Images/4. ls -R command.PNG>)
![`ls`](<Images/4. ls command.PNG>)


## 5. `cat` command
concatenated command in linux reads data from the file and gives its content as output. it helps us to create, view and conatenate. The following command was used;

- ***cat mealname.txt*** :This command was used to read the content of ***mealname.txt***
- ***cat sauce1.txt sauce2.txt > sauce3.txt*** :This command was used to merge the content of sauce1.txt and sauce2.txt into sauce3.txt.
- ***tac sauce.txt*** :This command was used to display sauce.txt content in reversed order.

![`cat`](<Images/5. cat command.PNG>)
![`cat`](<Images/5. cat merge command.PNG>)
![`cat`](<Images/5. tac cat command.PNG>)


## 6. `cp` command
it stands for copy. This command is used to copyy files or group files or directories. it creates an exact image of a file on a disk with a different file name. cp command requires at least two filename in its arguments. The following command was used:

- ***cp-R*** :This was used to copy Documents into Documents_backup directory.  

- ***cp sauce1.txt sauce4.txt*** :This was used to copy contents of sauce1.txt into sauce4.txt.

- ***cp sauce1.txt sauce2.txt sauce3.txt /home/olalonpei/username*** :This was used to copy the 3 .txt files into username directory. 

- ***cp sauce.txt /home/olalonpei/BreakFast*** :This was used to copy the .txt into  the BreakFast directory. 

![`cp`](<6. cp -r command.PNG>)
![`cp`](<6. cp command to copy contents to a file into another file.PNG>)
![`cp`](<6. cp command to files into a directory.PNG>)
![`cp`](<6. cp command.PNG>)

## 7. `mv` command
stands for move. This command is used to rename file directories and move files from one location to another within a file system. two distinct funtions of mv command is renaming a file or directory and moving a file or driectory to another location. The following command was used;

- ***mv mealprep1.txt /home/olalonpei/BreakFast*** :This was used to move the .txt file into the BreakFast directory

- ***mv mealprep.txt prepmeal.txt*** :This was used to rename mealprep.txt to prepmeal.txt.
![`mv`](<7. mv command to rename.PNG>)
![`mv`](<7. mv command.PNG>)


## 8. `mkdir` command
This allows the user to create directories or folders. this command can create multiple directories at once as well as set the permission to create a directory in the parent directory. The following command was used;

- ***mkdir FoodBlogging*** :I used this to create the ***FoodBlogging*** directory.

- ***mkdir FoodBlogging/StreetFood*** :I used this to create a folder inside the ***FoodBlogging*** directory.
![`mkdir`](<8. mkdir command.PNG>)


## 9. `rmdir` command
This is used to remove the empty directories from the filesystem in linux. The following command was used;
- ***rmdir -p FoodBlogging/StreetFood*** :I used this remove ***FoodBlogging*** directory, including all its ancestors. 
![`rmdir`](<9. rmdir command.PNG>)


## 10. `rm` command
Is used to remove objects such as files, directories, symbolic links and so on from the file system. rm rmoves references to objects from the filesystem, where those objects might have had multiple references. By default, it does not remove directories. The following command was used;
- ***rm remove*** ::I used this to delete the remove folder.
- ***rm reove2 reove3 reove4*** :I used this to delete reove2 reove3 reove4 folders.
![`rm`](<10. rm command.PNG>)


## 11. `touch` command
Is used to create a file without any content. the file created using the touch command is empty. This command can be used when the user doesn't have data to store at the time of file creation. The command used are; 
- ***touch teletubies*** :I used it to create a file.

- ***touch tiwinkie dipsy lala po*** :I used it to create multiple files.
![`touch`](<11. touch command.PNG>)