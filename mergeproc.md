## Instructions for the command line
- create branch
```
 git checkout -b feature/api 
 ```
 - make changes
 - make more changes

 - Run git add, commit, publish new created branch
 ```
 git add .
 git commit -m 'create new doc with instructions'
 git status
 git push -u origin feature/doc1
 ```

 - create a PR for this feature branch on Github

I should get the message:
Branch 'feature/doc1' set up to track remote branch 'feature/doc1' from 'origin'.

Then do:
```
git fetch origin
git checkout -b feature/doc1 origin/feature/doc1
```
If I'm in the feature branch, it will say the message:
fatal: A branch named 'feature/doc1' already exists.

But it's all okay.
Finally, run:
```
git merge main
git checkout main
git merge --no-ff feature/doc1
git push origin main
```
Note: After the git merge... command, write the final commit message in vim, then save and exit.
