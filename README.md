git commands in order:

git init (creates an empty local repository)  

git remote add origin git@github-tul44699:tul44699/merge-conflicts.git (adds a remote repository where changes can be committed to)

git add . (adds local files to staging) 

git commit -m "feat: add spec.txt" (creates baseline locally)

git push (pushes commits to remote)

git checkout -b branch-a (creates a new branch and switches to it)

git add .

git commit -m "feat: edit line 2"

git checkout master

git checkout -b branch-b

git add .

git commit -m "feat: edit line 2(branch b)"

git checkout master

git merge branch-a (attempts to merge branch-a into current branch(master))

git merge branch-b

git add .

git commit -m "fix merge conflict"

git push


there was a merge conflict because both branch A and B tried to make changes from the same baseline. The changes were applied to the same line so git didn't know what version to keep.
To fix the merge conflict, i just removed one of the changes and markers and modified the line to accommodate both changes
