
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

## Fetch the latest changes from the original repository and merge them into your forked `main` branch

1.  **Fetch the latest changes from the original repository:** If you haven't already, add the original repository as a remote (usually named `upstream`):
    
```bash
git remote add upstream <URL-of-original-repo>
``` 
    
* Then, fetch the latest changes from the `upstream` repository:
    
```bash
git fetch upstream
``` 
    
2.  **Switch to your fork's `main` branch:** Ensure you're on your fork's `main` branch:
    
```bash
git checkout main
``` 
    
3.  **Merge changes from the original `main` branch into your fork's `main`:** Merge the latest changes from the original repository's `main` branch into your fork's `main`:
    
```bash
git merge upstream/main
``` 
    
4.  **Push the updated `main` branch to your fork:** Once the merge is complete and there are no conflicts, push the updated `main` branch to your fork:
    
```bash
git push origin main
``` 
* This process ensures that your fork's `main` branch is up to date with the latest changes from the original repository before you start working on a new branch.

## Deleting a branch both locally and remotely

### 1. **Delete the branch locally:**

Make sure you're not currently on the branch you want to delete (switch to `main` or another branch if needed):

```bash
git checkout main
``` 

* Then delete the branch **locally**:

```bash
git branch -d scr_55_implement_create_table_on_catalog
``` 

If you want to force delete (e.g., if the branch has unmerged changes):

```bash
git branch -D scr_55_implement_create_table_on_catalog
``` 

### 2. **Delete the branch remotely:**

To delete the remote branch, use the following command:

```bash
git push origin --delete scr_55_implement_create_table_on_catalog
``` 

* After running these commands, the branch will be deleted both locally and remotely.
