https://www.atlassian.com/git/tutorials/git-submodule
https://git-scm.com/book/en/v2/Git-Tools-Submodules
https://blog.kennycoder.io/2020/06/14/Git-submodule-%E4%BD%BF%E7%94%A8%E6%95%99%E5%AD%B8/
http://jhjguxin.github.io/blog/2012/04/19/git-submodule-de-ren-shi-yu-zheng-que-shi-yong-!/
https://gist.github.com/gitaarik/8735255
https://github.blog/2016-02-01-working-with-submodules/

`git submodule add <url>`



The following two are equiv.
- `git clone --recurse-sudmodules <repo_url>`
- `git clone <repo_url>` then `cd <local_repo_name>` then `git submodule update --init --recursive`

And the following two are equiv.
- `git submodule update --init`
- `git submodule init` then `git submodule update`
