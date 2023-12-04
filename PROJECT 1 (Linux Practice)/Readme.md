# FILE MANIPULATION

## 1. `sudo` Command
This command is used to update the package lists for available software packages from the configured repositories. The following command was used 
- ***sudo apt upgrade*** :

![`sudo`](<Images/1. sudo command.PNG>)



## 2. `pwd` command
pwd means Print Working Directory. it prints the path of the working directory, starting with the root.
pwd command does not have any argument or options, but it can accept flags for specific behavior like -L and -P.
I used the following; 
- ***pwd -L***  :This command was used to obtain the symbolic path of my directory containing a symbolic link.
- ***pwd -P***  :This command was used to display the actual path, ignoring symbolic links.

![`pwd`](<Images/2. pwd command.PNG>)



## 3. `cd` command
cd command in linux known as the change directory command, is used to move from the current working directory to different directories in our system. the following syntax was used.
- ***cd BreakFast***  :This command was used to the move into the ***BreakFast*** directory 
   - ***cd OgiMoiMoi***  :This command was used to move into the ***OgiMoiMoi*** which is a subdirectory in the BreakFast directory
   - ***cd MoiMoiRecipe***  : This command was used to move into the ***MoiMoiRecipe*** which is a subdirectory in the ***OgiMoiMoi*** subdirectory
- ***cd ..***  :This command was used to move up to the ***OgiMoiMoi*** subdirectory.
- ***cd -***  :This command was used to move to the previous directory.
- ***cd~***  :This command was used to move back to the home directory
- ***cd /home/olalonpei/Lunch***  :This command was used move to the Lunch directory

![`cd`](<Images/3. cd command.PNG>)



## 4. `ls` command
ls a linux command that lists directory contents of files and directories. it provided valuable information about files, directories, and their atrributes. ls command also lists files and directories in alphabetical order. The following command was used;
- ***ls -a***  :This command was used to display all the hidden files in the home directory
- ***ls -lh***  :This command was used to display file size in easy to read format i.e M for MB, K for KB, G for GB
- ***ls -R***  :This command was used to list/display files and directories recursively, including subdirectories.
- ***ls***  :This command was used to display contents in the home directory

![`ls -a`](<Images/4. ls -a command.PNG>)
![`ls -lh`](<Images/4. ls -lh comand.PNG>)
![`ls -R`](<Images/4. ls -R command.PNG>)
![`ls`](<Images/4. ls command.PNG>)



## 5. `cat` command
concatenated command in linux reads data from the file and gives its content as output. it helps us to create, view and conatenate. The following command was used;
- ***cat mealname.txt***  :This command was used to read the content of ***mealname.txt***
- ***cat sauce1.txt sauce2.txt > sauce3.txt***  :This command was used to merge the content of sauce1.txt and sauce2.txt into sauce3.txt.
- ***tac sauce.txt***  :This command was used to display sauce.txt content in reversed order.

![`cat`](<Images/5. cat command.PNG>)
![`cat`](<Images/5. cat merge command.PNG>)
![`cat`](<Images/5. tac cat command.PNG>)



## 6. `cp` command
it stands for copy. This command is used to copyy files or group files or directories. it creates an exact image of a file on a disk with a different file name. cp command requires at least two filename in its arguments. The following command was used:
- ***cp-R***  :This command was used to copy Documents into Documents_backup directory.  
- ***cp sauce1.txt sauce4.txt***  :This command was used to copy contents of sauce1.txt into sauce4.txt.
- ***cp sauce1.txt sauce2.txt sauce3.txt /home/olalonpei/username***  :This command was used to copy the 3 .txt files into username directory. 
- ***cp sauce.txt /home/olalonpei/BreakFast***  :This command was used to copy the .txt into  the BreakFast directory. 

![`cp`](<6. cp -r command.PNG>)
![`cp`](<6. cp command to copy contents to a file into another file.PNG>)
![`cp`](<6. cp command to files into a directory.PNG>)
![`cp`](<6. cp command.PNG>)



## 7. `mv` command
stands for move. This command is used to rename file directories and move files from one location to another within a file system. two distinct funtions of mv command is renaming a file or directory and moving a file or driectory to another location. The following command was used;
- ***mv mealprep1.txt /home/olalonpei/BreakFast***  :This command was used to move the .txt file into the BreakFast directory
- ***mv mealprep.txt prepmeal.txt***  :This command was used to rename mealprep.txt to prepmeal.txt.

![`mv`](<7. mv command to rename.PNG>)
![`mv`](<7. mv command.PNG>)



## 8. `mkdir` command
This command allows the user to create directories or folders. this command can create multiple directories at once as well as set the permission to create a directory in the parent directory. The following command was used;
- ***mkdir FoodBlogging***  :This command was used to create the ***FoodBlogging*** directory.
- ***mkdir FoodBlogging/StreetFood***  :This command was used to create a folder inside the ***FoodBlogging*** directory.
![`mkdir`](<8. mkdir command.PNG>)



## 9. `rmdir` command
This command is used to remove the empty directories from the filesystem in linux. The following command was used;
- ***rmdir -p FoodBlogging/StreetFood***  :This command was used remove ***FoodBlogging*** directory, including all its ancestors.

![`rmdir`](<9. rmdir command.PNG>)



## 10. `rm` command
This command is used to remove objects such as files, directories, symbolic links and so on from the file system. rm rmoves references to objects from the filesystem, where those objects might have had multiple references. By default, it does not remove directories. The following command was used;
- ***rm remove***  :This command was used to delete the remove folder.
- ***rm reove2 reove3 reove4***  :This command was used to delete reove2 reove3 reove4 folders.

![`rm`](<10. rm command.PNG>)



## 11. `touch` command
This command is used to create a file without any content. the file created using the touch command is empty. This command can be used when the user doesn't have data to store at the time of file creation. The command used are; 
- ***touch teletubies***  :This command was used  to create a file.
- ***touch tiwinkie dipsy lala po***  :This command was used to create multiple files.

![`touch`](<11. touch command.PNG>)



## 12. `locate` command
This command is used to find files by name. The following command was used;
- ***locate -i lunch***  :This command was used to locate lunch. 

![`locate`](<12. locate command.PNG>)



## 13. `find` command
This command was used to find files and directories. It supports searching by file,folder,name,creation data, modification date,owner and permissions. The following command was used;
- ***find -name sauce1.txt***  :This command was used to find the sauce1.txt file.
![`find`](<13. find command2.PNG>)



## 14. `grep` command
This command is used to filter searches a file for a particular pattern of characters, and displays all lines that contain that pattern. The following command was used;
- ***grep -i dodo sauce3.txt***  :This command used to search for word ***dodo*** regardless of the case sensitivity.
- ***grep -c dodo sauce3.txt***  :This was used to search for the count of number of matches.
- ***grep -l dodo sauce3.txt sauce4.txt sauce.txt***  :This was used to search for the whole word in a .txt file.

![`grep`](<14. grep command -i -c -l.PNG>)



## 15. `df` command
This command displays information about file system disk space usage on the mounted file system. The following command was used;
- ***df***  :This command used to display infromation about all the mounted file systems which.
- ***df sauce3.txt*** :This command was used to display the mount information for the sauce3.txt file.
- ***df -h sauce3.txt***  :This command was used to display size in power of 1024. 
- ***df -h***  :This command was used to display size in power of 1024.

![`df`](<15. df -a command.PNG>)



## 16. `du` command
This command is used for estimating file and directory sapce usage. This following command was used;
- ***du /home/olalonpei/Lunch***  :This command was used to show information about the storage consumption of the ***Lunch*** directory.

![`16`](<16. du command.PNG>)



## 17. `head` command
This command prints the top N number of data of given input. By default, it prints 10 lines of the specified files. The following command was used;
- ***head sauce3.txt***  :This command was used to print the default first 10 lines of the .txt file.
- ***head -n 5 sauce3.txt*** :This command was used to print the first 5 lines.
- ***head -c 3 sauce3.txt*** :This command was used to print the first 3 bytes from the .txt file.
- ***head -q sauce3.txt sauce4.txt*** :This command was used to print top lines from two .txt file.

![`head`](<17. head command -q -n -c.PNG>)



## 18. `tail` command 
It prints the last N number of data of given input. By default, it prints 10 lines of the specified files. The following command was used;
- ***tail sauce3.txt***  :This command was used to print the default last 10 lines of the .txt file.
- ***tail -n 5 sauce3.txt***  :This command was used to print the last 5 lines.
- ***tail -c 13 sauce3.txt***  :This command was used to print the last 3 bytes from the .txt file.
- ***tail -q sauce3.txt sauce4.txt***  :This command was used to print last set of lines from two .txt file.

![`tail`](<18. tail command -n -q -c.PNG>)



## 19. `diff` command
This command is used to display thy discrepancies in the files by comparing the files line by line. The following command was used;
- ***diff sauce3.txt sauce4.txt***  :This command was used to check if there were any discrepancies between both .txt file.
- ***diff -c sauce3.txt sauce4.txt***  :This command was used to check if there were any discrepancies between both .txt file.
- ***diff -u sauce3.txt sauce4.txt***  :This command was used to check if there were any discrepancies between both .txt file.
- ***diff -i sauce3.txt sauce4.txt***  :This command was used to check if there were any discrepancies between both .txt file.

![`diff`](<19. diff -c -u -i command.PNG>)




## 20. `tar` command
This command is used to create archive and extract the archive files. tar command provides archiving functionality in linux. we can also use the linux tar command to create compressed or uncompressed archive file and also maintain and modify them. The following command was used;
- ***tar -cf archive.tar teletubies dipsy lala po*** :This command was used to archive the ***teletubies dipsy lala po*** files
- ***tar -tf archive.tar*** :This command was used to diplay the ***teletubies dipsy lala po*** files archived
- ***tar -xf archive.tar*** :This command was used to extract ***teletubies dipsy lala po*** the file archived.

![`tar`](<20. tar -cf -tf -xf command.PNG>)



# FILE PERMISSION & OWNERSHIP

## 21. `chmod` command
This command is used to change access mode of a file. The following command was used;
- ***chmod 777 sauce1.txt***  :This command was to change permission type of the ***sauce1.txt*** file.

![`chmod`](<21. chmod command-1.png>)



## 22. `chown` command
This command changes user ownership of a file, or directory. The following command was used;
- ***chown olalonpei sauce1.txt***  :This command was used to change owner of the ***sauce1.txt*** file.

![`chown`](<22. chown commandd.PNG>)




## 23. `jobs` command
This command is used to list all jobs on the system wether active or stopped. The following command was used;
- ***jobs*** :This command used to display the status of jobs in the current shell
- ***jobs -l*** :This command was used to list process IDs in addition to the normal information
- ***jobs -p*** :This command was used this to display the process ID.

![`jobs`](<23. jobs command...PNG>)




## 24. `kill` command
This command is a built-in command which is used to terminate processes manually. The following command was used;
- ***ps ux*** :This command was used to list the jobs running 
- ***kill -9 65*** :This command used to kill ***nano mealname.txt***

![`kill`](<24. kill command...PNG>)



## 25. `ping` command
This command is used to check the network connectivity between host and server/host. The following command was used;
- ***ping google.com***  : This command was used to check google.com is reachable.
- ***ctrl+c***   :to stop pinging.

![`ping`](<25. ping command.png>)




## 26. `wget` command
wget is used to download files from the server even when the user has not logged on t the system and it can work in the background without hindering the current process. The following command was used;
- ***wget https://wordpress.org/latest.zip***  :This command was used to download and archive wordpress web.

![`wget`](<26. wget command.PNG>)


## 27. `uname` command
This displays the information about the system. The following command was used;
- ***uname -a*** :This commandwas used to print information about the system
- ***uname -s*** :This command was used to print the kernel name.
- ***uname -n*** :This command was used to print the hostname of the current computer

![`uname`](<27. uname command.PNG>)




## 28. `top` command
This is used to show the linux processes, it provided a real time view of the running system. The following command was used;
- ***top***  :This was used to show real time view of the system.

![`top`](<28. top command.png>)




## 29. `history` command
This is used to view the previously executed command. The following command was used;
- ***history***  :This was used to display commands used.

![`history`](<29. history command.PNG>)



## 30. `man` command
This is used to display the user manual of any command that can run on the terminal. The following command was used;
- ***man ls***  :This command was used to diplay manual for ls.

![`man`](<30. man ls command.PNG>)




## 31. `echo` command
This is a built-in command that allows users to display lines of text or strings that are passed as arguments. Options are the various options available for modifying the behavior of the echo command such as (-e -n -E \b \c \a etc) while String is the what we want to display that is the word,sentence,statement.The following command was used;
- ***echo"Meals for Meals"*** 
:This command was used to display Meals for Meals.
- ***echo -n "Meals for Meals"***  :This command was used to omit echoing trailing newline
- ***echo -e "Meals \bfor \bMeals"*** :This command was used to remove all the spaces in between the text.
- ***echo -e "Meals \cfor Meals"*** :This command was used to suppress trailing new line and to continue without emitting new line.
- ***echo -e "\aMeals for Meals"***  :This command was used to play sound

![`echo`](<31. echo -e -n command.PNG>)




## 32. `zip` `unzip` command
Zip command is used to compress files to reduce file size and is also used to as file package utility, each file is stored in a single .zip file with the extension zip. WHILE unzip command will list, test, or extract files from a zip archive. The following command was used;
 ***zip latest.zip mealname.txt mealname2.txt mealname3.txt*** :This command was used to zip the mentioned .txt file.
- ***unzip latest.zip mealname.txt mealname2.txt mealname3.txt*** :This command was used to unzip the mentioned .txt file.

![`zip`](<32. zip command.PNG>)
![`unzip`](<32. unzip command.PNG>)




## 33. `hostname` command
This command is used Is to obtain the DNS name and set. The following command was used;
- ***hostname***  :This was command was used to obtain the system hostname.
- ***hostname -a***  :This command was used to display all aliases of the host.
- ***hostname -A***  :This command was used to display the FQDN (Fully Qualified Domian Name) but it returned nothing.
- ***hostname -i***  :This command was used to display the IP address of the host
- ***hostname -I***  :This command was used to get all IP network addresses.

![`hostname`](<33. hostname command...PNG>)




## 34. `useradd` `userdel` command
This is used to add user accounts to a system while usedel deletes it. Only those who with root priviledges or sudo can run this command. The following commands was used.
- ***sudo adduser ouser***  :This comman was used to create the ***ouser*** account.
- ***sudo userdel ouser***  :This command was used to delete the ***ouser*** account.

![`useradd`](<34. useradd command.PNG>)
![`userdel`](<34. userdel command.PNG>)



## 35. `apt get`




## 36. `nano` `vi`
This allows users to edit and manage files via a text editor. The following command was used;
- ***nano mealprep2.txt***  :This command was used pull up nano editor for the .txt file.
- ***vi mealprep2.txt***  :This command was used to pull up vi editor for the .txt file.

![`nano`](<36. nano comand.PNG>)
![`vi`](<36. vi command.PNG>)


## 37. `alias` `unalias` command
This command allows you to create a shortcut with the same functionality as a command, file name, or text while unalias is used to undo it. The following command was used;
- ***alias Meals=m***  :This command was used to replaces Meals with m.
- ***unalias Meals***  :This command was used to reemove an exisiting alias, in this case Meals.

![`alias` `unalias`](<37. alias and unalias command.PNG>)




## 38. `su` command
this command is used to switch to another user account
- ***su -p olalonpei***  :This command was used to switch to a user that is ***olalonpei***
- ***su -l newuser***  :This command was used to run a login script to switch to a different username that is ***newuser***

![`su`](<38. su -l -p command.PNG>)




## 39. `htop` command
htop command in linux system is a command line utility that allows the user to interactively monitor the system's vital resources or server's processes in real time. The following command was used;
- ***htop -C***  :This command was used to start htop in monochrome mode
- ***htop -u***  :This command was used to show only the processes of a given user

![`htop`](<39. htop -u command.PNG>)
![`htop`](<39. htop -C command.PNG>)



## 40. `ps` command
This command is used to list the currently running processes and their PIDs along with some other information depends on different options. The following commands was used;
- ***ps***  :Shows the processes for the current shell
- ***ps -u***  :This command was used to list processes associated with ***olalonpei***(user)
- ***ps -A***  :This command was used to to view all running processes.
- ***ps -T***  :This command was used to to display all processes associated with the current shell session.

![`ps`](<40. ps -u -A -T command.PNG>)
![`ps`](<40. ps command.PNG>)