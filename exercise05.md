# Exercise 5 - Making your first commit

1. If you just completed Exercise 4, `git status` should show that you have "changes to be committed"

2. Commit the changes with the command

        git commit

3. Your editor will open automatically.  Read the text that is already there.

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# On branch master
#
# Initial commit
#
# Changes to be committed:
#       new file:   fruits.txt
#

4. Enter your commit message, e.g.

        First commit

5. Save and exit from the editor

Output
======
\my_repository>git commit
[master (root-commit) bab65dd] First commit
 1 file changed, 1 insertion(+)
 create mode 100644 fruits.txt

6. Check git status again, and paste the contents below.

        git status

Output
======
\my_repository>git status
On branch master
nothing to commit, working tree clean
