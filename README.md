# Frontend-Programming

Git information

User Authentication:

```
git config –global user.email “youremail@”
git config –global user.name “yourname”
```

For creating a new repository

```
echo "# project-30" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/shiva-palakurthy/Frontend-Programming.git
git push -u origin main
```

To push an existing repository

```
git remote add origin https://github.com/shiva-palakurthy/Frontend-Programming.git
git branch -M main
git push -u origin main
```

To remove the existing remote

```
git remote remove origin
```

To get the origin URL

```
git config --get remote.origin.url
```

To switch to the target branch:

```
git checkout main
git checkout main <filename>
```

Commands to maintain both the origin and the local have the same version of code

```
git fetch
git log HEAD..origin/main
git pull origin main
```

`git fetch` - This command downloads all the new commits and branch updates from the remote(does not merge yet).
then check with `git status` if local is behind the remote.
If git status is not working
Steps to follow
`git branch -vv` - Verify your local branch and its upstream
`git log HEAD..origin/main` - This command shows a list of the commits that are in the 'origin/main' branch but not in your local 'main' branch (your current branch).
We can also run `git diff main..origin/main`
If the git branch -vv command shows that your local branch isn't tracking a remote one
Use `git branch --set-upstream-to=origin/main` command to set it manually. when committing for the first time if you use `git push -u origin main` command, it achieves the same goal of linking your local branch to its remote counterpar.

Once you have verified that a newer version of the code exists on the remote, you can bring the changes into your local branch by running `git pull`.

To download code from the remote to the local machine

```
git clone <git-branch-url>
```

1. to merge the changes from the source branch to the current branch
2. Git command that merges a specified branch into the current branch, forcing the creation of a new merge commit even if a fast-forward merge would be possible
   This merge commit acts as a record of the merge operation itself, connecting the two branches in the commit history.

```
git merge <branch_name>
or
git merge --no-ff <branch_name>
```
