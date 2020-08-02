Enable two factor authentification lead to pushing issue.

Two solution:

- create token
- add ssh key

Anyway just modify remote url:

```
$ git remote set-url origin git@github.com:USERNAME/REPOSITORY.git
```

-----------------------------------
### More info
- [doc](https://docs.github.com/en/github/using-git/changing-a-remotes-url#switching-remote-urls-from-https-to-ssh)
- [stack](https://stackoverflow.com/questions/17659206/git-push-results-in-authentication-failed)
