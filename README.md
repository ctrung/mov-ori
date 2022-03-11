# mov-ori
A repo with several branches from where we can play with repository migration

Migration procedure : 
```sh
git clone --mirror <url_of_old_repo>
cd <name_of_old_repo>
git remote add new-origin <url_of_new_repo>
git push new-origin --mirror
```

Atlassian procedure to pick the desired refs : https://www.atlassian.com/git/tutorials/git-move-repository

**Remarques**

1. Un `git remote update` côté client resynchronise le repo local, équivalent à un `rmdir` et de nouveau un `git clone --mirror`.

1. Certains types de références ne sont pas poussables (eg. les pull requests car lectures seules, etc...).
```sh
$ git push new-remote --mirror
Enumerating objects: 13, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 8 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (13/13), 3.26 KiB | 3.26 MiB/s, done.
Total 13 (delta 3), reused 8 (delta 2)
remote: Resolving deltas: 100% (3/3), done.
To github.com:ctrung/mov-new.git
 * [new branch]      feature/new-procedures -> feature/new-procedures
 * [new branch]      main -> main
 * [new branch]      new-remote/feature/new-procedures -> new-remote/feature/new-procedures
 * [new branch]      new-remote/main -> new-remote/main
 * [new tag]         v1.0 -> v1.0
 ! [remote rejected] refs/pull/1/head -> refs/pull/1/head (deny updating a hidden ref)
error: failed to push some refs to 'git@github.com:ctrung/mov-new.git'
```
