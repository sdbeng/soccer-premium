## Instructions for the command line
- create branch
```
 git checkout -b feature/api 
 ```
 - make changes
 - make more changes

 - git add, commit, publish new created branch
 ```
 git add .
 git commit -m 'create new doc with instructions'
 git status
 git push -u origin feature/doc
 ```

 - create a PR for this feature branch on Github

I should get the message:
Branch 'feature/doc' set up to track remote branch 'feature/doc' from 'origin'.

Then do:
```
git fetch origin
git checkout -b feature/doc origin/feature/doc
```
If I'm in the feature branch, it will say the message:
fatal: A branch named 'feature/doc' already exists.

But it's all okay.
Finally, run:
```
git merge main
git checkout main
git merge --no-ff feature/doc
git push origin main

