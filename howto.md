## Deleting a folder on Git on Windows

### If you have a local directory
1. Go to the location of the directory and delete it.
2. Go to GitHub and go to your repository. 
3. Click on the "Clone or Download" button and copy the address.
4. Open up your Git shell.
5. In your Git shell write: git clone <paste your repository>.
6. Change to the directory you wish to delete a folder and write: cd ~\Documents\GitHub\YourFolderName
7. After that, write: git rm -r YourFolderName
8. Now you need to commit the changes to git. Write: git commit -m "Removed YourFolderName."
9. Now you need to push the changes to git. Write: git push origin master

