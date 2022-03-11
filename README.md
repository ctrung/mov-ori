# mov-ori
A repo with several branches from where we can play with repository migration

Migration procedure : 
```
git clone --mirror <url_of_old_repo>
cd <name_of_old_repo>
git remote add new-origin <url_of_new_repo>
git push new-origin --mirror
```

Atlassian procedure to pick the desired refs : https://www.atlassian.com/git/tutorials/git-move-repository

NB : un `git remote update` côté client resynchronise le repo local, équivalent à un `rmdir` et de nouveau un `git clone --mirror`.
