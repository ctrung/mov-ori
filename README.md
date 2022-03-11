# mov-ori
A repo with several branches from where we can play with repository migration

Migration procedure : 
```
git clone --mirror <url_of_old_repo>
cd <name_of_old_repo>
git remote add new-origin <url_of_new_repo>
git push new-origin --mirror
```
