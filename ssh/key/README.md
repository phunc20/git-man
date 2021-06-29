

## Specify SSH Key when Executing Commands like `git clone/pull/push`
It seems that if one does not specify which SSH key to use, `git` will assume by default
the key under `~/.ssh/id_rsa`. Sometimes, you just created many keys and `~/.ssh/id_ras`
is not necessarilly the right private key that you want.

There are at least two methods which can come to rescue:

01. Set a particular env variable as you run your command, e.g.
  ```bash
  GIT_SSH_COMMAND="ssh -i /anywhere/you/put/your/private/key" git clone git@gitlab.com:username/your_super_secret_repo.git
  ```
02. Set in the file `~/.ssh/config`. This has the benefit that you do not have to remember to set `GIT_SSH_COMMAND` each time. Here is two example entries to set up `~/.ssh/config`
   ```config
   Host github.com
       HostName 13.239.175.159
       IdentityFile ~/.ssh/id_github
       IdentitiesOnly yes
   
   Host gitlab.com
       HostName 172.65.255.19
       IdentityFile ~/.ssh/id_gitlab
       IdentitiesOnly yes
   ```
