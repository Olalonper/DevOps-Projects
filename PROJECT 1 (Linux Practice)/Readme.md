# FILE MANIPULATION

## `sudo` Command
This command is used to update the package lists for available software packages from the configured repositories. I used *sudo apt upgrade*.

![sudo](<Images/1. sudo command.PNG>)


## `pwd` command
pwd means Print Working Directory. it prints the path of the working directory, starting with the root.
pwd command does not have any argument or options, but it can accept flags for specific behavior like -L and -P.
I used the following; 
- *pwd -L* :This was used to obtain the symbolic path of my directory containing a symbolic link.
- *pwd -P* :This was used to display the actual path, ignoring symbolic links.

![pwd](<Images/2. pwd command.PNG>)


## `cd` command
cd command in linux known as the change directory command, is used to move from the current working directory to different directories in our system. the following syntax was used.

- *cd BreakFast* :I used this to the move into the *BreakFast* directory 
   - *cd OgiMoiMoi* : Then i used this to move into the *OgiMoiMoi* which a subdirectory in the BreakFast directory
   - *cd MoiMoiRecipe* : I used this to move into the *MoiMoiRecipe* which is a subdirectory in the OgiMoiMoi subdirectory

- *cd ..* :I used this to move up to the *OgiMoiMoi* subdirectory.
- *cd -* :I used this to move to the previous directory.
- *cd ~* :I used to move back to the home directory
- *cd /home/olalonpei/Lunch* :I used this to move to the Lunch directory

![cd](<Images/3. cd command.PNG>)
