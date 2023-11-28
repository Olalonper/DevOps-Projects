# FILE MANIPULATION

## `sudo` Command
This command is used to update the package lists for available software packages from the configured repositories. I used ***sudo apt upgrade***.

![sudo](<Images/1. sudo command.PNG>)


## `pwd` command
pwd means Print Working Directory. it prints the path of the working directory, starting with the root.
pwd command does not have any argument or options, but it can accept flags for specific behavior like -L and -P.
I used the following; 
- ***pwd -L*** :This command was used to obtain the symbolic path of my directory containing a symbolic link.
- ***pwd -P*** :This command was used to display the actual path, ignoring symbolic links.

![pwd](<Images/2. pwd command.PNG>)


## `cd` command
cd command in linux known as the change directory command, is used to move from the current working directory to different directories in our system. the following syntax was used.

- ***cd BreakFast*** :This command was used to the move into the ***BreakFast*** directory 
   - ***cd OgiMoiMoi*** :This command was used to move into the ***OgiMoiMoi*** which is a subdirectory in the BreakFast directory
   - ***cd MoiMoiRecipe*** : This command was used to move into the ***MoiMoiRecipe*** which is a subdirectory in the OgiMoiMoi subdirectory
- ***cd ..*** :This command was used to move up to the *OgiMoiMoi* subdirectory.
- ***cd -*** :This command was used to move to the previous directory.
- ***cd~*** :This command was used to move back to the home directory
- ***cd /home/olalonpei/Lunch*** :This command was used move to the Lunch directory

![cd](<Images/3. cd command.PNG>)


## `ls` command
ls a linux command that lists directory contents of files and directories. it provided valuable information about files, directories, and their atrributes. ls command also lists files and directories in alphabetical order. The following command was used;


***ls -a*** :This command was used to display all the hidden files in the home directory
***ls -lh*** :This command was used to display file size in easy to read format i.e M for MB, K for KB, G for GB
***ls -R*** :This command was used to list/display files and directories recursively, including subdirectories.
***ls*** :This command was used to display contents in the home directory

![`ls -a`](<Images/4. ls -a command.PNG>)
![`ls -lh`](<Images/4. ls -lh comand.PNG>)
![`ls -R`](<Images/4. ls -R command.PNG>)
![`ls`](<Images/4. ls command.PNG>)



