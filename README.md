# Github_Map_Closing_Notes

### how github handles repo names
```
github allows [A-Za-z0-9_.-], and transforms all other characters to "-"
when we were getting each file name
we needed to check immediately if it passed and ignore/not create repo if it failed.
```

### when rebasing a large number of commits (implemented in next header)
```
if squashing make changes on a seperate branch
then, do not merge; 
instead preserve the old copy of master renaming
and then change the rebased branch to master
(implemented in next header: how to change master branch)
```
### how to change master branch
```
git branch -m master old-master
git branch -m seotweaks master
git push -f origin master
git push origin master:master --force
```

```
If you want to rename the current branch, you can do:

git branch -m newname
```

### warning regarding github map, in view mode.
```
submodules are only for viewing.
edits should be performed by cloning
and pushing particular repositories.
```

### updating a map
```
git clone --recursive https://github.com/MichaelDimmitt/Research.git
cd Research/;git submodule update --remote --merge;
git add .;git commit -m "applied updat operation git submodule update --remote --merge”;git push;
git clone --recursive https://github.com/MichaelDimmitt/Research.git;
```

### Additional Information coming soon.
#### secrets ... people may be warned
```
git rebase -i 504faf7d0b72c6d8e6fc0279a40fb39143d6d0ad
vi README.md 
git add .
git commit --amend --author="MichaelDimmitt <michaelgdimmitt@gmail.com>" --no-edit
git rebase --continue
git push --force-with-lease
```
