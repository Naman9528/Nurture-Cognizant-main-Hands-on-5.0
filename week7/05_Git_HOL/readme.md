# Git Cleanup and Push to Remote Repository

## Objective

The objective of this lab is to learn how to synchronize a local Git repository with a remote GitHub repository by pulling the latest changes, verifying the repository status, and pushing local commits to the remote repository.

---

## Prerequisites

- Git installed
- GitHub repository configured as the remote repository
- Previous hands-on lab (Git-T03-HOL_002) completed

---

## Lab Overview

This lab focuses on cleaning up the local repository and synchronizing it with the remote repository hosted on GitHub. It demonstrates how to verify the repository status, pull the latest changes from the remote repository, push pending local commits, and confirm that the changes are successfully reflected on GitHub.

---

## Steps Performed

1. Verified that the `master` branch was in a clean state.
2. Listed all available local and remote branches.
3. Pulled the latest changes from the remote repository.
4. Pushed the pending local commits to the remote GitHub repository.
5. Verified that the changes were successfully reflected in the remote repository.

---

## Commands Used

```bash
git checkout master
git status

git branch -a

git pull origin master

git push origin master
```

---

## Result

- Verified the repository was in a clean state.
- Confirmed the available branches.
- Synchronized the local repository with the remote repository.
- Successfully pushed all pending commits to GitHub.
- Verified the updated repository on GitHub.

---

# Summary

In this lab, the local Git repository was synchronized with the remote GitHub repository. The repository status was verified, available branches were listed, the latest changes were pulled from the remote repository, and pending local commits were pushed successfully. Finally, the remote repository was verified to ensure that all local changes were uploaded successfully, completing the Git synchronization process.