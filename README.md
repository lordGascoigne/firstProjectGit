# Пробное оформление файла README

---


## Content
1. Common commands for Git Terminal user
2. The head ripple effect of Git
3. Synchronizing your local and remote repositories  
4. Hash, HEAD and file status in Git  

#### Common commands for Git Terminal user
*pwd* - print working directory  
**ls** - print list of objects in the directory, could be used with -a (showing hidden files)  
~~red_button~~ - it`s not existing, just a joke  
cd - change directory  
touch - create a file  
cat - print text files, what allows you to read them

#### The head ripple effect of Git

**git add** - stage your file, mark them to commit  
**git commit -m "<your description of your changes>"**  
**git push**  


#### Synchronizing your local and remote repositories

1. Generate ssh-key locally

```
$ ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub"

$ ssh-keygen -t rsa -b 4096 -C "электронная почта, к которой привязан ваш аккаунт на GitHub"
```

2. Check whether your key is generated

```
ls -a ~/.ssh
```

3.Linking ssh key and Github account

```
$ clip < ~/.ssh/id_rsa.pub

$ clip < ~/.ssh/id_ed25519.pub 
```

#### Hash, HEAD and file status in Git

Hash is commit ID (unique for every commit), it`s storing in hidden .git in the project repository.  

```
git log - command for checking commit`s info. (author, date, email, hash id)
```

```
git log --oneline - shorten log, one line - one commit history record.
```

Short hash remains unique withtin repository, so you can find certain one. 

**HEAD file** - storaging in hidden .git, pointing on the latest commit. HEAD contains link (refs/heads/main(master))to the file, with latest commit hash id.  
!!you can use word HEAD instead of latest commit hash id to call last commit!! 


##### File status in Git

There are 4:  
1. untracked - new files in the repository, no changes are being followed by Git, no previous versions, mentioned in **git add** or commits.  
2. staged - status after **git add** command. It`s in a list to be committed by **git commit**. It`s also called "indexed", "cached".  
3. tracked - files, where Git`s tracking the changes. They (files) could be add by **git add** or **git commit**.  
4. modified - there is difference between the current file condition and the latest version of it. F.e. file had been committed and then was changed.  
A file can have several status in the moment (one file, but different versions).

Huge thaks to [Yandex](https://practicum.yandex.ru/trainer/git-basics/lesson/c6b9607c-e8bc-4446-89f9-c74522c3492f/ "it`s yandex title")for their immensive impact on my learning
