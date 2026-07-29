# Git Merge Conflict Resolution Lab

## Objective

The objective of this lab is to understand how Git handles merge conflicts and how to resolve them when two branches modify the same file differently.

---

## Lab Overview

In this lab, two branches (`master` and `GitWork`) independently create and modify the same file (`hello.xml`). Since both branches introduce different versions of the file, Git cannot automatically merge them, resulting in a merge conflict.

The conflict is then resolved manually (or using a merge tool), after which the merge is completed successfully.

---

## Steps Performed

1. Verified that the `master` branch was in a clean state.
2. Created a new branch named `GitWork`.
3. Added a new file `hello.xml` in the `GitWork` branch.
4. Modified and committed the file.
5. Switched back to the `master` branch.
6. Created another `hello.xml` with different content.
7. Committed the changes on `master`.
8. Viewed the commit history using Git log.
9. Compared differences between the branches.
10. Used Git Diff/P4Merge to visualize differences.
11. Attempted to merge `GitWork` into `master`.
12. Encountered a merge conflict because both branches added the same file with different content.
13. Resolved the conflict manually (or using a merge tool).
14. Committed the resolved merge.
15. Added merge backup files to `.gitignore`.
16. Committed the updated `.gitignore`.
17. Listed all branches.
18. Deleted the merged `GitWork` branch.
19. Viewed the final commit history.

---

## Commands Used

```bash
git checkout -b GitWork
git add .
git commit -m "Added hello.xml in GitWork branch"

git checkout master
git add .
git commit -m "Added hello.xml in master"

git log --oneline --graph --decorate --all
git diff master GitWork
git difftool master GitWork

git merge GitWork

git add hello.xml
git commit -m "Resolved merge conflict"

git add .gitignore
git commit -m "Added merge backup files to .gitignore"

git branch
git branch -d GitWork

git log --oneline --graph --decorate
```

---

## Merge Conflict Example

Git generated conflict markers similar to:

```xml
<<<<<<< HEAD
<message>Hello from Master Branch</message>
=======
<message>Hello from GitWork Branch</message>
>>>>>>> GitWork
```

The conflict was resolved by removing the markers and keeping the required final content.

---

## Result

- Successfully created and managed multiple branches.
- Understood why merge conflicts occur.
- Learned how to inspect conflicting changes.
- Successfully resolved the merge conflict.
- Updated `.gitignore` to ignore merge backup files.
- Deleted the merged feature branch.
- Verified the final commit history.

---

# Summary

This lab demonstrated Git's merge conflict resolution workflow. By creating conflicting changes on two branches, we observed Git's conflict detection mechanism and learned how to manually resolve conflicts. After resolving the conflict, the merge was completed successfully, unnecessary merge backup files were ignored using `.gitignore`, and the feature branch was safely deleted. This lab provides practical experience with one of the most important version control tasks used in collaborative software development.