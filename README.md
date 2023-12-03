# Version Control System

+ **Author :** Deepanshu Raj
+ **Created On :** Jan 4, 2021 (Monday)


## Version Control System :
         
  **`Git`** : Distributed Version Control System.
                
  Features listed in this Repo :
                      
  - Creating a Git repo.
  - Reviewing a Repo's History.
  - Adding Commits to a Repo.
  - Tagging, branching & Merging.
  - Undoing Changes.
  
## Common Instructions:

### ✳ 1. Creating a Git Repo

- <b>git init :</b> Create a new git Repository on your computer.
- <b>git clone :</b> Copy an existing repo on your computer(from a remote repo).
- <b>git status :</b> Status of the repo(at present).
- <b>git clone <url> <project_name_that_you_want> :</b> Copy Project with a different Project name. 

### ✳ 2. Reviewing a Repo's History

- <b>git log :</b> Log <b>[SHA , Author , Date & Message]</b> of all the commit made till present.
- <b>git log --oneline :</b> Single-Line Log of all the commits till present.
- <b>git log --stat :</b> More info<b>[files modified,no. of insertions/deletions,Summary of total modified files/ lines added/removed]</b> about the commits.
- <b>git log --patch :</b> or <b>git log -p :</b> Show the exact changes(modifications) for each commit. 
- <b>git log -p -w :</b> Ignore whitespace Changes of the commits.
- <b>git show <first_7_chars_of_the_SHA> :</b> Displays all the details of that particular commit, whose SHA has been given. 
- <b>git diff :</b> Display the Changes that have been made but haven't been commited yet.

### ✳ 3. Adding Commits to a Repo

- <b>git add <file> :</b> Stages the file.(WD->SI) 
- <b>git add . :</b> Stage all the modified files.
- <b>git rm --cached <file> :</b> Unstage a given File.(SI->WD)
- <b>git commit -m '<msg>' :</b> Commit changes.(SI->repo) [Only message can be provided with such commits]
- <b>git commit :</b> Commit changes.(SI->repo) [Default editor will open, & a desc. will be asked to enter].

#### {WD ~ Working Directory ; SI ~ Staging Index}

### ✳ 4. Tagging, Branching & Merging

- <b>git tag :</b> Tells us about the already present tags. 
- <b>git tag -a <tag_name> :</b> To create an <b>Annotated Tag.</b>[with desc.] @ current commit. 
- <b>git tag -d <tag_name> :</b> To delete a particular tag.
- <b>git tag <tag_name> :</b> To create a <b>Lightweight Tag.</b>[without desc.] @ current commit.
- <b>git tag -a <tag_name> <SHA_of_the_commit> :</b> To tag a particular commit[commit with the specified SHA]. 
- <b>git branch :</b> Display all the branches present at present in our repo.
- <b>git branch <branch_name> :</b> Creates a new branch with <branch_name> as it's name.
- <b>git checkout <branch_name> :</b> Changes the active branch to the branch with branch name as <branch_name>. 
- <b>git checkout -b <branch_name> :</b> Creates and checkout the branch with branch name as <branch_name>. 
- <b>git branch -d <b_name> :</b> deletes the branch with name as <b_name>.
- <b>git branch -D <b_name> :</b> Force deletes the branch with name as <b_name>.
- <b>git branch <b_name> <SHA_of_the_commit> :</b> Creates a branch at the commit whose SHA is passed. 
- <b>git log --oneline --graph --all :</b> Show all the branches in a visual representation.
- <b>git merge <name_of_the_branch_to_merge_in> :</b> Merge the active branch with the branch provided.

### ✳ 5. Undoing Changes

- <b>git commit --amend :</b> To modify the last commit(most recent commit)
- <b>git revert <SHA_of_the_commit> :</b> To undo the changes done in the commit with the given SHA.
- <b>git reset <relative_reference> :</b> <br>
  - <b>Modes(Labels) :</b><br>
    - --mixed [<b>git reset --mixed <relative_reference> or git reset <relative_reference> :</b> move the changes from Repo to WD].<br>
    - --soft [<b>git reset --soft <relative_reference> :</b> move the changes from repo to SI].<br>
    - --hard [<b>git reset --hard <relative_reference> :</b> erase the commit]

#### {WD ~ Working Directory ; SI ~ Staging Index}
