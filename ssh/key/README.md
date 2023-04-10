

## Specify SSH Key when Executing Commands like `git clone/pull/push`
It seems that if one does not specify which SSH key to use,
`git` will assume by default the key under `~/.ssh/id_rsa`.
Sometimes, you just created many keys and `~/.ssh/id_ras`
is not necessarilly the right private key that you want to use.

There are at least two ways in which you can specify the key to be used.

1. Set a particular env variable as you run your command, e.g.
  ```bash
  GIT_SSH_COMMAND="ssh -i /anywhere/you/put/your/private/key" git clone git@gitlab.com:username/your_super_secret_repo.git
  ```
1. Set in the file `~/.ssh/config`. This has the benefit that you do not have to remember to set `GIT_SSH_COMMAND` each time. Here is two example entries to set up `~/.ssh/config`
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
   - Note that **the string next to `Host`**, in the above cases, `github.com` and
     `gitlab.com` **could have been anything**. For example, you might have two
     GitLab accounts, one for your company and another for your own personal work.
     Then one way to separate them apart is to put them like this in `~/.ssh/config`:
     ```config
     Host personal_gitlab
         HostName 172.65.255.19
         IdentityFile ~/.ssh/id_personal_gitlab
         IdentitiesOnly yes

     Host company_gitlab
         HostName 172.65.255.19
         IdentityFile ~/.ssh/id_company_gitlab
         IdentitiesOnly yes
     ```
     
     The only things you need to pay attention are
        - To clone, say, some repo from your personal GitLab
          ```bash
          $ git clone git@personal_gitlab:phunc20/<name_repo>.git
          ```
        - You need to specify the right file paths of the right keys
