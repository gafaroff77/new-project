# REM!!! We are use abbreviation for git command!
# In any worked directory we must create dir "new-project"
$ mkdir new-project

# Initialize local project, branch "main"
$ git init -b main

# create file README.md
$ echo init > README.md

# staging README.md & commit
$ git add README.md && git ci -m "init"

# changed branche
$ git co -b development

# We in "development" branche. Do edit README.md with needed inf's
# After edit staged'n'commit
$ git add README.md && git ci -m "added step-by-step instruction in cli"

# go to branch "main" and merge development to this branch
$ git co main && git merge development

# here we create ssh keys for github ssh connect
$ ssh-keygen -o -t rsa -b 2048 -C "gafaroff77@gmail.com"
$ cat ~/.ssh/id_rsa.pub

# must store pub key to user's settings in github
# check connection
$ eval $(ssh-agent -s)
$ ssh -t git@github.com

# setup remote origin
git remote add origin git@github.com:gafaroff77/new-project.git

# push project
$ git push -u -f origin main

# ... PROFIT ))

