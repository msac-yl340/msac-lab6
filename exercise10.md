# Exercise 10 - Understanding Commits

1. Look at your commit log

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

2. Choose a commit hash

7947e56

3. See what type of object that hash names

        git cat-file -t <hash>

Output
======
\my_repository>git cat-file -t 7947e56
commit

4. Examine the contents of that commit closely

        git cat-file -p <hash>

Output
======
\my_repository>git cat-file -p 7947e56
tree 01c2a78fa5973f217c6918164b50e96aa7b8a332
parent 0227b3e8de0e43dffffe63277f18cc4fd8d83bbe
author Yancy Li <yli340@student.mtsac.edu> 1665380161 -0700
committer Yancy Li <yli340@student.mtsac.edu> 1665380161 -0700

equipment\furniture.txt added

5. Find the parent's hash in the commit log

Output
======
\my_repository>git cat-file -p 0227b3e8de0e43dffffe63277f18cc4fd8d83bbe
tree 4a4d71b84a48b026854b834167e245a895325b6b
parent 925f1b1ae107e56d61675adad8f8e5754ec7e6e5
author Yancy Li <yli340@student.mtsac.edu> 1665379584 -0700
committer Yancy Li <yli340@student.mtsac.edu> 1665379584 -0700

vegetables.txt modified

6. Look at the contents of the tree

        git cat-file -p <hash>

Output
======
\my_repository>git cat-file -p 4a4d71b84a48b026854b834167e245a895325b6b
040000 tree abf2b11cca913502b22b8f41232947bb09e15701    equipment
100644 blob d56d8347cf98cc62a1cddae0188aa9545b6b2f1a    fruits.txt
100644 blob 0c227af7b59b63cc129399ff1b7052ec3ee8f769    vegetables.txt

7. Examine the contents of one of the blobs

Output
======
\my_repository>git cat-file -p d56d8347cf98cc62a1cddae0188aa9545b6b2f1a
cantaloupe
apple
banana
tomato
blueberry
strawberry

8. What type of object does the parent hash represent?

        git cat-file -t <hash>

commit 

9. Examine the contents of the parent and its tree

10. Do the trees you looked at have any matching hashes listed?

No, the trees I looked at does not have any matching hashes listed.
