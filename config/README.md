## Files in This Directory
Put
- `./gitconfig` to `~/.gitconfig`
- `./config` to `.git/config` of any of your github/gitlab projects


## Global and Local Configurations
You can have a global Git configuration (usually at `~/.gitconfig`), but then
for each project you do not necessarily want to use the same configuration.

A possible scenario is that you use the same machine for work and for personal matters.
You'll have two identities, one as an employee of your company, another as yourself.
You then have company projects and personal projects. You need to separate them.

Say your global Git config is set to you as a company employee. Then for your personal
projects, you could make a **local Git config**. For example, say, you clone your personal
project
```bash
$ git clone git@github.com:phunc20/mySuperProj.git
```

Then, in order to create a local Git config, you create a file like this
```bash
$ cd mySuperProj
$ vim .git/config
$ # After editing, it should look like this
$ cat .git/config
[core]
        ...
        sshcommand = ssh -i ~/.ssh/id_rsa
[remote "origin"]
        ...
[branch "main"]
        ...
[user]
        name = <your_personal_username>
        email = <your_personal_email>
```
The three lines indicated above should be payed with attention.



# Old Notes
```bash
$ git config --global user.name "phunc20"
$ git config --global user.email "wucf20@gmail.com"
$ git config --global core.editor vim
$ git config --list
```



```
`~/.gitconfig`
----
[alias]
	co = checkout
	br = branch
	st = status
	logv = log --all --graph --oneline
[user]
	email = wucf20@gmail.com
	name = phunc20
[core]
	editor = vim
[init]
	defaultBranch = trunk
```
