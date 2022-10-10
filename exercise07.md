# Exercise 7 - More than one changed file

1. Ensure you have a clean working directory

        git status

Output
======
\my_repository>git status
On branch master
nothing to commit, working tree clean

2. Edit one of your `fruits.txt`, add a few items

        blueberry
        strawberry
        etc.

3. Edit `appliances.txt` and add a few items

        dishwasher
        dryer
        etc.

4. Look at git status, paste the output here

        git status

Output
======
\my_repository>git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   equipment/appliances.txt
        modified:   fruits.txt

no changes added to commit (use "git add" and/or "git commit -a")

5. Can you commit both of the changed files in a single commit?

Yes, I can commmit both the changed files in a single commit by entering 
git commit -m "fruits.txt and equipment\appliances.txt modified" fruits.txt equipment

Output
======
\my_repository>git commit -m "fruits.txt and equipment\appliances.txt modified" fruits.txt equipment
[master 925f1b1] fruits.txt and equipment\appliances.txt modified
 2 files changed, 6 insertions(+), 2 deletions(-)

6. After you do so, check that you have a clean working directory by running `git status`, and pasting the output here

Output
======
\my_repository>git status
On branch master
nothing to commit, working tree clean

7. Create a new file `equipment/furniture.txt`. Add content to both `vegetables.txt` and `furniture.txt`

Output
======
\my_repository>git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   vegetables.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        equipment/furniture.txt

no changes added to commit (use "git add" and/or "git commit -a")

8. How can you commit just one of the changed files?

I can commit just one of the changed files by only naming the file to be commited.

git commit -m "equipment\furniture.txt add" equipment

Output
======
\my_repository>git add equipment

\my_repository>git commit -m "vegetables.txt modified" vegetables.txt
[master 0227b3e] vegetables.txt modified
 1 file changed, 2 insertions(+), 1 deletion(-)

9. Check your `git status`

Output
======
\my_repository>git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   equipment/furniture.txt

10. What does red text mean in the output of `git status`?

The red text in the output of 'git status' means the files are changed that are not staged for commit or untracked.

11. What does green text mean in the output of `git status`?

The green text in the output of 'git status' means the files are changed and ready to be committed.

12. How can you make a single file show in both red and green in the output of `git status`?

I believe I can make a single file show in both red and green in the output of 'git status' by modifying a file after it's being staged for commit (green text). The new modified file git status will change to red text as the file is no longer staged. 
