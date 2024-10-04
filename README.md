# zip file 

when include zip file in project then step flow.. Remove zip file command in the project bellow

1. git log --all --full-history -- "**.zip"   // .zip here your file name
2. Remove the File from the Commit History command:  git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch *.zip' --prune-empty --tag-name-filter cat -- --all
3.  Clean Up and Force Push command: 
git reflog expire --expire=now --all
git gc --prune=now --aggressive
4.Force Push command:  git push origin --force --all

Use this command step by step I hope your problem is solved..
Thank you ...


