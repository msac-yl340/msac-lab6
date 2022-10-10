# Exercise 6 - Committing a change (full cycle)

1. Look at git status and ensure you have a clean working directory

        git status

Output
======
\my_repository>git status
On branch master
nothing to commit, working tree clean

2. Open your `fruits.txt` file  in VS Code, your favorite code editor

3. Add some lines to the file

        apple
        banana
        tomato

4. Save and exit the editor

5. Look at git status

        git status

Output
======
\my_repository>git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   fruits.txt

no changes added to commit (use "git add" and/or "git commit -a")

6. Add the file to the index

        git add fruits.txt

7. Check status

        git status

Output
======
\my_repository>git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   fruits.txt

8. Commit the changes (short commit message included on command line)

        git commit -m "Added more fruit to the list"

Output
======
\my_repository>git commit -m "Add more fruit to the list"
[master ca67262] Add more fruit to the list
 1 file changed, 4 insertions(+), 1 deletion(-)

9. Check status

        git status

Output
======
\my_repository>git status
On branch master
nothing to commit, working tree clean

10. Which of the steps could be omitted?

For new users, git status is useful ensure each step is executed without issue. As the users get more familiar with the process, git status could be omitted as the chance of making error is less likely. 

git add is another step for users to select which files they want to commit. If the users usually commit whatever changed files. This step could be committed as well.

11. Why might it be a bad idea to omit them?

Sometimes users make mistakes that could cause a dirty working tree. If they don't check the status using git status, it might be too late when they find out about the dirty working tree. Users could lose the source code or need to rebuild the branch as a result. 

As for the git add, if a user accidentally modified a file and do a git commit without git add, the user could overwrite a file unintentionally and could mean loss of codes or causing a program no longer functions properly.

12. Repeat the above steps to add a new file with the name `vegetables.txt`

Output
======
\my_repository>git add vegetables.txt

\my_repository>git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   vegetables.txt

13. Create a subdirectory named `equipment` and a new file named `appliances.txt` in that subdirectory

Output
======
\my_repository>git add equipment

\my_repository>git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   equipment/appliances.txt
        new file:   vegetables.txt

14. Repeat the above steps to commit the new file and directory

Output
======
\my_repository>git commit -m "vegetables.txt, equipment\appliances.txt added" vegetables.txt equipment
[master 4742a50] vegetables.txt, equipment\appliances.txt added
 2 files changed, 2 insertions(+)
 create mode 100644 equipment/appliances.txt
 create mode 100644 vegetables.txt

\my_repository>git status
On branch master
nothing to commit, working tree clean

15. Repeat the above steps 1-9, adding data to each of your files a few lines at a time, until you can easily do the steps without referring to the steps. You may want to add vegetables to the vegetables file, and appliances to the appliances - or vice versa

Add some lines in appliances.txt

Output
======
\my_repository>git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   equipment/appliances.txt

\my_repository>git add equipment

\my_repository>git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   equipment/appliances.txt

\my_repository>git commit -m "equipment\appliances.txt modified" equipment
[master 6031708] equipment\appliances.txt modified
 1 file changed, 3 insertions(+), 1 deletion(-)

\my_repository>git status
On branch master
nothing to commit, working tree clean
