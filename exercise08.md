# Exercise 8 - Viewing changes before committing

1. Ensure your working directory is clean

Output
======
\my_repository>git commit -m "equipment\furniture.txt added" equipment
[master 7947e56] equipment\furniture.txt added
 1 file changed, 1 insertion(+)
 create mode 100644 equipment/furniture.txt

\my_repository>git status
On branch master
nothing to commit, working tree clean

2. Add text to any one of your files

3. Delete different text from another of your files

4. Look at `git status`

Output
======
\my_repository>git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   equipment/appliances.txt
        modified:   vegetables.txt

no changes added to commit (use "git add" and/or "git commit -a")

5. View all the changes you've made

        git diff

Output
======
\my_repository>git diff
diff --git a/equipment/appliances.txt b/equipment/appliances.txt
index 36d0aac..1dbd28f 100644
--- a/equipment/appliances.txt
+++ b/equipment/appliances.txt
@@ -1,5 +1,4 @@
 toaster
 microwave
-kettle
 dishwasher
 dryer
\ No newline at end of file
diff --git a/vegetables.txt b/vegetables.txt
index 0c227af..edbfbca 100644
--- a/vegetables.txt
+++ b/vegetables.txt
@@ -1,2 +1,3 @@
 kale
-cucumber
\ No newline at end of file
+cucumber
+beet
\ No newline at end of file

6. Does the following command return anything?

        git diff --staged

No, the following command does not return anything as nothing is staged yet.

7. Add one of your changed files to the index

        git commit add <changed file>

Output
======
\my_repository>git add vegetables.txt

8. What do these commands show?

        git diff
        git diff --staged

Output
======
\my_repository>git diff
diff --git a/equipment/appliances.txt b/equipment/appliances.txt
index 36d0aac..1dbd28f 100644
--- a/equipment/appliances.txt
+++ b/equipment/appliances.txt
@@ -1,5 +1,4 @@
 toaster
 microwave
-kettle
 dishwasher
 dryer
\ No newline at end of file

\my_repository>git diff --staged
diff --git a/vegetables.txt b/vegetables.txt
index 0c227af..edbfbca 100644
--- a/vegetables.txt
+++ b/vegetables.txt
@@ -1,2 +1,3 @@
 kale
-cucumber
\ No newline at end of file
+cucumber
+beet
\ No newline at end of file

9. Add the other changed file to the index

        git commit add <other changed file>
        
Output
======
\my_repository>git add equipment


10. What do these commands show?

        git diff
        git diff --staged

Output
======
\my_repository>git diff

\my_repository>git diff --staged
diff --git a/equipment/appliances.txt b/equipment/appliances.txt
index 36d0aac..1dbd28f 100644
--- a/equipment/appliances.txt
+++ b/equipment/appliances.txt
@@ -1,5 +1,4 @@
 toaster
 microwave
-kettle
 dishwasher
 dryer
\ No newline at end of file
diff --git a/vegetables.txt b/vegetables.txt
index 0c227af..edbfbca 100644
--- a/vegetables.txt
+++ b/vegetables.txt
@@ -1,2 +1,3 @@
 kale
-cucumber
\ No newline at end of file
+cucumber
+beet
\ No newline at end of file

11. Commit the changes

Output
======
\my_repository>git commit -m "Exercise 8 changes committed"
[master cab0b3c] Exercise 8 changes committed
 2 files changed, 2 insertions(+), 2 deletions(-)

12. Check that your working directory is clean

Output
======
\my_repository>git status
On branch master
nothing to commit, working tree clean

13. Create a new file named `clothing.txt`

14. Does the new untracked file show up in git diff?

        git diff

No, the new untracked file does not show up in git diff.

15. Add and commit the new file

Output
======
\my_repository>git add clothing.txt

\my_repository>git commit -m "clothing.txt added"
[master 05f9b0f] clothing.txt added
 1 file changed, 1 insertion(+)
 create mode 100644 clothing.txt

\my_repository>git status
On branch master
nothing to commit, working tree clean
