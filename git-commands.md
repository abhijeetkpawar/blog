
Diff of changes since diversion:  
`git diff master...topic`


Remove untracked/ignored files:

    git clean [--dry-run]
    	-f = force
    	-d = directory
    	-X = only ignored
    	-x = ignored as well as non-ignored files

Push new local branch upstream:  
`git push -u origin <branch_name>`

###Delete###
- local branch:  **`git branch -d <branch>`**
- local remote-tracking branch:  **`git branch -dr <remote>/<branch>`**
- remote branch:  **`git push --delete origin <branch>`**

*[Delete Ref: http://stackoverflow.com/questions/2003505/delete-a-git-branch-both-locally-and-remotely]*

### Log ###
One line log:  
`git log --oneline --decorate`

Graph:  
`git log --graph --oneline --decorate`

Author-wise listing of git commits:  
`git shortlog`

Log commits since diversion from master:  
`git log master..feature`

Log commits not in master:  
`git log feature --not master`

Log Push/Pull/Fetch operations:  
`git reflog show origin/<branch>`

**Cache credentials:**  
`git config --global credential.helper cache`  
`git config --global credential.helper "cache --timeout=3600"`