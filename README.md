# git_exe
Created repo with README.md initially \
$ git pull origin main

# Create a feature branch for project setup with the proper Zoho task ID
$ git branch TE-T158_Project_Setup

# Create a sub-branch from the project setup branch
$ git branch sub_Project_Setup TE-T158_Project_Setup \
$ git checkout sub_Project_Setup \
$ git branch
    TE-T158_Project_Setup \
    main
  * sub_Project_Setup

# 1.Squash
there were originally 3 commits in file1 sub_Project_Setup branch \
$ git rebase -i HEAD~3 \
    -> Successfully rebased and updated refs/heads/sub_Project_Setup.

# 2.Reset
    $ git log --oneline 
        18c63c1 (HEAD -> sub_Project_Setup) file 1 commit 4 in sub_Project_Setup 
        fa998e2 (origin/sub_Project_Setup) file 1 commit 3 in sub_Project_Setup 
        addba78 (origin/main, origin/TE-T158_Project_Setup, main, TE-T158_Project_Setup) Initial commit 

    $ git reset --hard fa998e2 
    $ git log --oneline 
        fa998e2 (HEAD -> sub_Project_Setup, origin/sub_Project_Setup) file 1 commit 3 in sub_Project_Setup
        addba78 (origin/main, origin/TE-T158_Project_Setup, main, TE-T158_Project_Setup) Initial commit

# 3.Rebase
    $ git pull origin main

    $ git checkout sub_Project_Setup

    $ git rebase main \
        -> Successfully rebased and updated refs/heads/sub_Project_Setup.

    $ git checkout main
    $ git merge sub_Project_Setup
    $ git push origin main


    
