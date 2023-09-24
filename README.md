# Пробное оформление файла README

---


## Content
1. Common commands for Git Terminal user
2. The head ripple effect of Git
3. Synchronizing your local and remote repositories

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

Huge thaks to [Yandex](https://practicum.yandex.ru/trainer/git-basics/lesson/c6b9607c-e8bc-4446-89f9-c74522c3492f/ "it`s yandex title")for their immensive impact on my learning
