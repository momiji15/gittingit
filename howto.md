# How to deal with git on Windows
I'm using git shell in order to do all of my gittery.  These things worked for me...hopefully they will work for you too.Typing up how to do things in git as I encounter them. Excuse the disorganization.

## Checking to see what is the what is the origin
1. type `git remote -v`

## You have git set up and ready to go. You multiple respositories going on and you want to commit to the one repository you've been working on.
1. Let's first check to see what the origin is. Type `git remote -v`.
2. If the origin is right, then you're alright. If not, then you need to change directories.
3. Type `cd ~\Documents\GitHub\YourFolderName`.
4. Type `git status` to see which files you have changed.
5. Type `git add filename` to include the files you want to commit. You might have to do this multiple times.
6. Type `git commit -m "Put whatever commit message you want"`.
7. Let's push it through the repository. Type `git push origin master` in order to do that. 

## Seeing what you committed.
1. Type `git log` in the git shell.
2. If you want to escape from the git log, press `Q`.

## If you are just messing around with your git and you accidently commit to the wrong repository. You want to get rid of that commit, plus  have your repository reflect that your mistake never ever did happen.
1. Type `git log` in the git shell.
2. Find the commit where you want to revert your repo to.
3. Highlight and right-click on that commit.
4. Press `Q` to stop the git log madness.
5. You're going to have to force push this one through. Type `git push origin +whateveryourcommitnumberis`.
6. Check your github to see if it is gone. Fingers crossed.

NOTE: Word on the street is that you should proceed with caution with this. Like if you're in a group working on something, this might not be the best thing to do for your situation. You might want to do the following instead...keep on reading...

## If you want to get rid of a commit the safe way...and you don't care if theres "remants" of it on your GitHub
1. Type `git log` in the git shell.
2. Find the commit where you want to revert your repo to.
3. Highlight and right-click on that commit.
4. Press `Q` to end the git log.
5. Type: `git revert commitnumber(seriously write your commit number)`

## Deleting a folder 

### If you have a local directory
1. Go to the location of the directory and delete it.
2. Go to GitHub and go to your repository. 
3. Click on the "Clone or Download" button and copy the address.
4. Open up your Git shell.
5. In your Git shell write: `git clone` <paste your repository>.
6. Change to the directory you wish to delete a folder and write: `cd ~\Documents\GitHub\YourFolderName`.
7. After that, write `git rm -r YourFolderName`.
8. Now you need to commit the changes to git. Write: `git commit -m "Removed YourFolderName."`
9. Now you need to push the changes to git. Write: `git push origin master`.
  
 ### If you want to delete your file on your GitHub but you want to keep it locally
 For a single file:
 `git rm --cached -r mydirectory`

 For single directory:
 Let's just say you wanted to get rid of your .gitignore file...
 `git rm --cached -r .gitignore`

### Cloning a repository
1. Click on "Clone or download."
2. Copy the link.
3. Open up your Git shell, command line...wherever you do your thing with Git.
4. Type `git clone` and then paste the link.


### If you get a message about updates being rejected becauase the remote contains work you do not have locally
If you get this wonderful message when trying to commit something:
`hint: Updates were rejected because the remote contains work that you do`
`hint: not have locally. This is usually caused by another repository pushing`
`hint: to the same ref. You may want to first integrate the remote changes`
`hint: (e.g., 'git pull ...') before pushing again.`

Just do what the instructions say and type `git pull` and then `git push origin master`.

## You're working on a project with someone and you forked someone's repo. That someone made a commit to their repo and when you go to your forked repo, you see a message that says "This branch is 4 commits behind whateverthenameoftherepo:master."
Okay, not going to lie....I refered to this lovely blog post by [Gary Gregory](https://garygregory.wordpress.com/2016/11/10/how-to-catch-up-my-git-fork-to-master/) on how to do this. You could just click on that or read on. I won't be mad at you.

- Open up your command line/git shell/whatever.
- Change to the local directory of the project.
- Go the the repository of the person who has the master repo and click on that clone/download button(the green one). Copy that link. 
- In your command line write `git remote add upstream https://github.com/personsusername/personsrepo.git`. Of course this is purely an 
  example. 
- If you want to make sure all is well, type `git remote -v` to see what's up.
- Now you're going to have to get those commits from the master repository so you will need to type `git fetch upstream`.
- And now you're going to merge those changes to your local master branch: `git merge upstream/master`
