
# Things that make you go "huh"

## You're trying to commit and you get a message in which your updates are rejected...
You might get a message along these lines:
`error: failed to push some refs to your repository.
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.`

This probably has happened because you made some changes on your repository online and you didn't bother to send those changes down to the folder stored on your computer. Don't despair. Do what the hints tell you and type `git pull`. You need to synchronize what you did online to your repository folder on your computer. After that, type `git status` to see what's going on. You might get a message that says your branch is ahead of your master, which means what is done online and on your computer is not synched up. Type `git push` in order to push your commits.
