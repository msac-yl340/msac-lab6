# Exercise 9 - Viewing history

1. Make a commit with a multi line commit message
   (leaving an empty line after the first line)

Output
======
\my_repository>git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        exercise9.txt

nothing added to commit but untracked files present (use "git add" to track)

\my_repository>git add *

\my_repository>git commit
[master cef06d6] Multi line commit message line 1
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 exercise9.txt

2. View that commit in the log

        git log -1

Output
======
\my_repository>git log -1
commit cef06d6ebab48210f413795013912eb389bf6680 (HEAD -> master)
Author: Yancy Li <yli340@student.mtsac.edu>
Date:   Sun Oct 9 22:56:21 2022 -0700

    Multi line commit message line 1

    Multi line commit message line 3

3. View the full commit log

        git log

Output
======
\my_repository>git log
commit cef06d6ebab48210f413795013912eb389bf6680 (HEAD -> master)
Author: Yancy Li <yli340@student.mtsac.edu>
Date:   Sun Oct 9 22:56:21 2022 -0700

    Multi line commit message line 1

    Multi line commit message line 3

commit 05f9b0f03fb717dc095618f40b20a8c86f0227e9
Author: Yancy Li <yli340@student.mtsac.edu>
Date:   Sun Oct 9 22:52:26 2022 -0700

    clothing.txt added

commit cab0b3c0cf02bb1ea0b5079e9cd6150e5a5101b9
Author: Yancy Li <yli340@student.mtsac.edu>
Date:   Sun Oct 9 22:49:17 2022 -0700

    Exercise 8 changes committed

commit 7947e56718eeeac462f02b2e024ee4b3fc39cb4a
Author: Yancy Li <yli340@student.mtsac.edu>
Date:   Sun Oct 9 22:36:01 2022 -0700

    equipment\furniture.txt added

commit 0227b3e8de0e43dffffe63277f18cc4fd8d83bbe
Author: Yancy Li <yli340@student.mtsac.edu>
Date:   Sun Oct 9 22:26:24 2022 -0700
:

*If the log fills your whole terminal, press `q` to exit*

4. View a shortened version of the commit log

        git log --oneline

Output
======
\my_repository>git log --oneline
cef06d6 (HEAD -> master) Multi line commit message line 1
05f9b0f clothing.txt added
cab0b3c Exercise 8 changes committed
7947e56 equipment\furniture.txt added
0227b3e vegetables.txt modified
925f1b1 fruits.txt and equipment\appliances.txt modified
6031708 equipment\appliances.txt modified
4742a50 vegetables.txt, equipment\appliances.txt added
ca67262 Add more fruit to the list
bab65dd First commit

5. Pick a commit hash from the log

925f1b1

6. View the commit log from the chosen commit backward

        git log --oneline <commit_hash>

Output
======
\my_repository>git log --oneline 925f1b1
925f1b1 fruits.txt and equipment\appliances.txt modified
6031708 equipment\appliances.txt modified
4742a50 vegetables.txt, equipment\appliances.txt added
ca67262 Add more fruit to the list
bab65dd First commit

7. How much of the commit hash do you need to specify? Hint, run `git help log`

The full length of the hash is 40 characters long; however, it's 7 characters by default. Depends on the project, I believe 7 characters is sufficient.  

8. How can you show just the last three commit messages?

I can show just the last three commit messages by entering git log -3

Output
======
\my_repository>git log -3
commit cef06d6ebab48210f413795013912eb389bf6680 (HEAD -> master)
Author: Yancy Li <yli340@student.mtsac.edu>
Date:   Sun Oct 9 22:56:21 2022 -0700

    Multi line commit message line 1

    Multi line commit message line 3

commit 05f9b0f03fb717dc095618f40b20a8c86f0227e9
Author: Yancy Li <yli340@student.mtsac.edu>
Date:   Sun Oct 9 22:52:26 2022 -0700

    clothing.txt added

commit cab0b3c0cf02bb1ea0b5079e9cd6150e5a5101b9
Author: Yancy Li <yli340@student.mtsac.edu>
Date:   Sun Oct 9 22:49:17 2022 -0700

    Exercise 8 changes committed
    