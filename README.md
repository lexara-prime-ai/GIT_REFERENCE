
### Useful resource links
* A reference for standard git commands.

* [When to Rebase](https://www.bing.com/search?pglt=515&q=is%20git%20pull%20--rebase%20the%20best&cvid=429443f83a6e41bbaf5eab9d3077ca34&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIGCAEQABhAMgYIAhAAGEAyBggDEAAYQDIGCAQQABhAMgYIBRAAGEAyBggGEAAYQDIGCAcQABhAMgYICBAAGEAyCAgJEOkHGPxV0gEINzQ0OWowajGoAgCwAgA&FORM=ANNAB1&PC=U531)
* [Pull new updates from original GitHub repository into forked GitHub repository](https://stackoverflow.com/questions/3903817/pull-new-updates-from-original-github-repository-into-forked-github-repository)
* [When should I use git pull --rebase? - Stack Overflow](https://stackoverflow.com/questions/2472254/when-should-i-use-git-pull-rebase)


### Others
## Create a new branch based on the original repository's main branch

You can create a new branch based on the original repository's `main` branch by following these steps:

1.  **Fetch the latest changes from the original repository:** First, ensure that you have the original repository set as a remote (often named `upstream`):
    
```bash
git remote add upstream <URL-of-original-repo>
``` 
* Then, fetch the latest changes from the original repository's `main` branch:
    
```bash
git fetch upstream
``` 
    
2.  **Create a new branch based on the original `main` branch:** Now that you've fetched the latest updates from the original repository, create a new branch based on that:
    
```bash
git checkout -b new-branch-name upstream/main
``` 
    
3.  **Push the new branch to your fork (optional but recommended):** Push the newly created branch to your fork so that you have a remote copy:
    
```bash
git push origin new-branch-name
``` 
* Now you can work on this branch without affecting your fork's `main` branch. When you're done, you can create a pull request for this new branch as well.
