# INITIALIZING A REPOSITORY AND MAKING COMMITS

## 1. `Initializing a Git repository`
This was achieved by doing the below;
- Install Git
- Open the git bash terminal
- Create a working folder or directory.
  - ***mkdir Git-Project*** :This command was used to create ***Git-Project*** directory.
- Move into the working directory.
  - ***cd Git-Project***  :This command was used to move into the ***Git-Project*** directory.
- While you are inside the directory run ***git init***

![`Initializing a Git repository`](<Images/1. Initializing a Git Repository.PNG>)




## 2. `Making your first commit`
This was achieved by doing the below;
- Inside the working directory ***i.e Git-Project*** create a file.
  - ***touch forcommit.txt***  :This command was used to create the .txt file.
- Write any sentence of your choice inside the text file.
  - ***echo "Excited to be making my first commit > index.txt"***  :This command was used to display lines of text.
- Add your chnages to git staging area.
  - ***git add .***  :This command was used to add changes.
- Commit the changes and run command.
  - ***git commit -m "initial commit"***  :This command was used to commit the chnages ***-m*** flag is a parameter to pass in the commit message.

  ![`Making yout first commit`](<Images/2. Making your first commit.PNG>)




  ## 3. `Making your first branch`
  This was achieved by doing the below;
- Make a new branch.
  - ***git checkout -b north***  :This command was used to create ***north*** branch.The ***-b*** flag helps create and change into a new branch.

![`Making your first branch`](<Images/3. Making your first Branch.PNG>)




## 4. `Listing your git branch`
This was achieved by doing the below;
- List the branch(es) on your local git repository.
  - ***git branch***  :This command was used to list the branch.

![`Listing your git branch`](<Images/4. Listing your git Branch.PNG>)



## 5. `Changing into an old branch`
This was achieved by doing the below;
- Change into an existing or old branch
  - ***git checkout main***  :This command was used to change into the ***main*** branch.

![`Changing into an old branch`](<Images/5. Changing into an Old Branch.PNG>)




## 6. `Merging a branch into another branch`
This was acheived by doing the below;
- Change into branch A and run merge command;
  - ***echo "adding another section of how interesting this is" > forcommit.txt***  :This command was used to display lines of text.
  - ***git status***  :This command was used to check the status of the .txt file.
  - ***git add .***  :This command was used to add changes.
  - ***git commit -m "adding a section of how interesting this is"***  :This command was used to commit the chnages.
  - ***git chechout north***  :This command was used to exit the ***main*** branch and enter into the ***north*** branch.
  - ***git merge main***  :This command was used to merge content of ***main*** branch with ***north*** branch

![`Merging a branch into another branch`](<Images/6. Merging a Branch into another Branch.PNG>)




## 7. `Deleting git branch`
This was acheived by doing the below;
- To delete a Git branch.
   - ***git branch -d north***  :This command was used to delete the ***north*** branch.

![`Deleting git branch`](<Images/7. Deleting git branch.PNG>)   





# COLLABORATION AND REMOTE REPOSITORIES
First thing that needs to be done is this section is to create an account on github using the below steps and screenshot as a guide;
- Open github.com [visit github.com/join](https://www.github.com/join)
- Next enter your email and click continue.
- Next create your passowrd and click continue.
- Next enter your username and click continue.
- Next click on the verify button to verify your identity.
- Next click on the Create button to create your account.
- An activation code will be sent to your email, enter the code in the textboxes provided then click continue.
- Select your preferences and click continue.

![`visit github.com/join`](<Images/github step (1).PNG>)
![`visit github.com/join`](<Images/github step (2).PNG>)
![`visit github.com/join`](<Images/github step (3).PNG>)
![`visit github.com/join`](<Images/github step (4).PNG>)
![`visit github.com/join`](<Images/github step (5).PNG>)
![`visit github.com/join`](<Images/github step (6).PNG>)
![`visit github.com/join`](<Images/github step (7).PNG>)
![`visit github.com/join`](<Images/github step (8).PNG>)



# CREATING YOUR FIRST REPOSITORY
Upon signing up on github, create a Repository using the below steps and screenshot as a guide;
- Click on the plus sign located at the top right corner of your github profile page. A dropdown menu will appear, select new.
- Fill out the form by adding a unique repository name, description and ticking the box to add a Readme.md file.
- Click the green button to create your repository.

![`visit github.com/join`](<Images/github step (9).PNG>)
![`visit github.com/join`](<Images/github step (10).PNG>)
![`visit github.com/join`](<Images/github step (11).PNG>)



# TO COPY A REPOSITORY LINK
To copy your repository link using the below steps and screenshot as a guide
- Scroll to code highlighted in green (beside your repository name) and Click it.
- A dropdown menu will appear. 
- To copy highlight the link or click the copy icon.

![`visit github.com/join`](<Images/github step (12).PNG>)
![`visit github.com/join`](<Images/github step (13).PNG>)



## 8. `Pushing your local git repository to your remote github repository`
This is schieved by doing the below;
- Add a remote repository to the local repository.
  - ***git remote add origin https://github.com/Olalonper/GitPRJ.git***  :This command was used to add the repo link

- After commiting your chnages to the local repo. Push the content to the remote repository.
  - ***git push origin main***  :Thi command was nor working as it was returning an error message.
  - ***git pull***  :This command was used as git bash suggested but that also wasnt working.
  - ***git push orign main***  :This command was used but it wasnt working as well.
  - ***git pull origin main***  This command was used to get rid of the error butit was returning **fatal: refusing to merge unrelated histories**. 

> ### SOLUTIONS
> - ***git pull --rebase origin main***  :This command was used to local commit ontop of remote head. 
> - ***git push -u origin main*** :This command was used to push the local repository to the remote branch 

![`Pushing your local git repository to your remote github repository`](<Images/8. Pushing your local git repository to your remote github repository.PNG>)

![`Pushing your local git repository to your remote github repository`](<Images/8. Pushing your local git repository to your remote github repository2.PNG>)


