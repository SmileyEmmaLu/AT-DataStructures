# GitHub Notes

## Commands:
These are the commands that you must know for git

```bash
git clone 'yourUrl'
git status
git pull
git add 'fileName'
git add -A
git commit -m "your message"
git push
git checkout -b 'newBranchName'
git merge master
git push --set-upstream origin newBranchName
```
## Workflow:
### Working on Master-

The workflow for working on master is:
`git clone 'yourUrl'`
~~add files, change files~~
`git pull`
`git status`
`git add -A`
`git commit -m "your message about what you changed"`
`git push`
~~repeat as needed~~

### Working on a Branch-
`git clone 'yourUrl'`
`git checkout -b 'branchName'`
~~add files, change files~~
`git merge master`
`git status`
`git add -A`
`git commit -m "your message about what you changed"`
`git push --set-upstream origin branchName` (only needs to happen once)
~~repeat changing things, adding ,commiting and pushing as needed~~

~~ON GITHUB~~
Create a pull request with a description of the changes your branch made.

Let other coder review code and merge branch with master.

Delete local and remote branch on terminal:

Local- `git -d branchName`
Remote- `git push origin --delete branchName`
All other collaborators- `git fetch --all --prune`





