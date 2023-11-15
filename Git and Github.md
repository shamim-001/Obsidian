#git #github 
[50 git command - freecodecamp](https://www.freecodecamp.org/news/git-cheat-sheet/)

## How to switch to a newly created branch in Git:

```
git checkout branch_name
```

# Remote repo
```bash
git remote -v
```

```bash
git remote show origin
```

- `git ls-remote --get-url origin`: This command will display the URL for the `origin` remote repository.
- `git remote set-url origin <new-url>`: This command will change the URL for the `origin` remote repository to `<new-url>`.
- `git remote add <name> <url>`: This command will add a new remote repository named `<name>` with URL `<url>`.
- `git remote remove <name>`: This command will remove the remote repository named `<name>`.
