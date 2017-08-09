# How to deal with git on Windows
I'm using git shell in order to do all of this. Typing up how to do things in git as I encounter them.

## Seeing what you committed.
1. Type git log in the git shell.
2. If you want to escape from the git log, press Q.

## If you are just messing around with your git and you accidently commit to the wrong repository. You want to get rid of that commit, plus  have your repository reflect that your mistake never ever did happen.
1. Type git log in the git shell.
2. Find the commit where you want to revert your repo to.
3. Highlight and right-click on that commit.
4. Press Q to stop the git log madness.
5. You're going to have to force push this one through. Type git push origin +whateveryourcommitnumberis.
6. Check your github to see if it is gone. Fingers crossed.

## Deleting a folder 

### If you have a local directory
1. Go to the location of the directory and delete it.
2. Go to GitHub and go to your repository. 
3. Click on the "Clone or Download" button and copy the address.
4. Open up your Git shell.
5. In your Git shell write: git clone <paste your repository>.
6. Change to the directory you wish to delete a folder and write: cd ~\Documents\GitHub\YourFolderName.
7. After that, write: git rm -r YourFolderName.
8. Now you need to commit the changes to git. Write: git commit -m "Removed YourFolderName."
9. Now you need to push the changes to git. Write: git push origin master.


