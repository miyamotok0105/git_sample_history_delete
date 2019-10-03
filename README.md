# git_test


## 1.Make file

```
# make file
touch a.txt
mkdir aa
touch aa/a.txt
# Add local git
git add a.txt
git add aa
# Commit local git
git commit -m "Add file"
# Push to remote git
git push origin master
```

## 2.Delete file from git history and file

Donot change anything before delete git history. If change some file, then you'll get some error.
You'd better to run this. `git reset --hard HEAD`.    

```
# Delete file from history
git filter-branch --index-filter 'git rm --cached --ignore-unmatch a.txt'
# Delete folder from history
git filter-branch --index-filter 'git rm --cached --ignore-unmatch aa/a.txt'
# Commit 
git commit -m "Delete file from histroy"
# Push to remote.
git push origin master --force
```


