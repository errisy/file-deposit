# file-deposit

How to use github as web drive?

1) Add a file to .git (You have to invoke git at the folder where .git folder is available.
```
git add test.txt
```
2) Commit Changes:
```
git commit -m 'file-deposit' test.txt
```
3) Update to the server:
```
git push origin master
```
This step may ask for username and password. to avoid that, in the ./.git/config file, you change the [remote "origin"] url
```
[remote "origin"]
	url = https://username:password@github.com/errisy/file-deposit.git
	fetch = +refs/heads/*:refs/remotes/origin/*
```

then the push command will work without asking for username and password.

The strategy allows you to build a shared service that is hosted for free.
