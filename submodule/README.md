https://www.atlassian.com/git/tutorials/git-submodule
https://git-scm.com/book/en/v2/Git-Tools-Submodules
https://blog.kennycoder.io/2020/06/14/Git-submodule-%E4%BD%BF%E7%94%A8%E6%95%99%E5%AD%B8/
http://jhjguxin.github.io/blog/2012/04/19/git-submodule-de-ren-shi-yu-zheng-que-shi-yong-!/
https://gist.github.com/gitaarik/8735255
https://github.blog/2016-02-01-working-with-submodules/


## How to Add A Submodule?
`git submodule add <remote_or_local_url> <local_path>`

For example, if you've cloned the neovim lsp config repo like this

```bash
mkdir -p ~/.config/nvim/pack/nvim/start
git clone https://github.com/neovim/nvim-lspconfig ~/.config/nvim/pack/nvim/start/
```

and you git-version-control your `~/.config/nvim/` and want to include `nvim-lspconfig/`
as a submodule, then you can run the following command
(after `cd`-ing into `~/.config/nvim/`):

```bash
git submodule add ./pack/nvim/start/nvim-lspconfig ./pack/nvim/start/nvim-lspconfig
```

Alternatively, if you did not clone the remote `nvim-lspconfig` repo at first place,
then you can run the following command from the git-initiated repo of `~/.config/nvim/`:

```bash
mkdir -p pack/nvim/start
git submodule add https://github.com/neovim/nvim-lspconfig ./pack/nvim/start/nvim-lspconfig
```

Either way, you'd obtain the following results:

```bash
~/.config/nvim $ git st -uno
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   .gitmodules
        new file:   pack/nvim/start/nvim-lspconfig

Untracked files not listed (use -u option to show untracked files)
~/.config/nvim $ bat .gitmodules
───────┬───────────────────────────────────────────────────────────────────────────────────
       │ File: .gitmodules
───────┼───────────────────────────────────────────────────────────────────────────────────
   1   │ [submodule "pack/nvim/start/nvim-lspconfig"]
   2   │     path = pack/nvim/start/nvim-lspconfig
   3   │     url = ./pack/nvim/start/nvim-lspconfig
───────┴───────────────────────────────────────────────────────────────────────────────────
~/.config/nvim $ 
```

I.e. two new staged files `.gitmodules` and `pack/nvim/start/nvim-lspconfig`.


## Other Things
The following two are equiv.
- `git clone --recurse-sudmodules <repo_url>`
- `git clone <repo_url>` then `cd <local_repo_name>` then `git submodule update --init --recursive`

And the following two are equiv.
- `git submodule update --init`
- `git submodule init` then `git submodule update`
