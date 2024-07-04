- Annotated tag
    - Syntax, e.g. `git tag -a v1.4 [commit_checksum] -m "add xml determiner function in this version"`
        - `-a` stands for annotation.
        - `-m`, like in `git commit -m "some message"`, stands for message.
            - If one chooses to not specify using `-m`, Git will prompt you with Git's default editor.
        - `[commit_checksum]`, when not specified, will default to the latest one.


`git push <remote> <tagname>` to push a tag some git server,
or `git push origin --tags` to push all your tags that weren't already pushed to the server.

`git tag` or `git tag -l "v1*"` to list tags.

Use `git show <tagname>` to show the tag and its related commit.

Use `git tag -d <tagname>` to delete a tag locally on your machine.
To delete the tag from a server, there are two ways:
1. `git push <remote> --delete <tagname>`
2. `git push origin :refs/tags/<tagname>`

`git checkout <tagname>` to check out the commit that the tag is pointing to.

