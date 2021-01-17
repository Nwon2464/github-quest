### Initialize a git repo on your local computer
- git init 
- git add .
- git commit -m "memo" or git commit -am "memo" (-am only works for the files that are untracked)

### Initialize a git repo on github
- create a new repository
- copy the url on your newly created repo
- git remote add origin url
- git remote -v  to check it's completed
- git push -u origin master  to take our commits locally and push them up to github
(-u stands for set upstream which basically means origin master is default thing and whenever i run git push, push to origin master, every repo comes with master branch)


### logging git status that are previous histories
-git log or git log --oneline

### Collaborating projects with others 
------work flow------
1. git fork 
to complete copy of someone's repo on my github, lets say tony's repo.
(taking existing tony's repo and copying it into your github so that you can now make changes on my github)

2. git clone url
to clone the repo that you forked down to my local computer
(click clone or download and copy the url, in your terminal, set cd with empty files, and git clone url )


2.5 check to see if everything works with npm install, then you are ready to make changes.

3. git checkout -b add-new-index-js
creating a new branch 

4. make some changes and git add .

5. git commit -m "added index.js with new branch"

6. git push origin add-new-index-js

7. go to github page where you forked it, click Compare & pull request
(this means hey i made some commits and changes on this branch on my fork, I want Tony to merge those changes into his master
)

8. on Tony github page, he should accept "Merge pull request" to be in sync with my commits

9. on Tony terminal, git fetch to fetch all of the changes from github, in his terminal, it will say your branch is behind "origin/master" by x commits,
so git pull to have all the changes on tony's locally

10. on my terminal, my master branch is no longer in sync with tony's master branch. so on my terminal, git checkout master and look at my forked repo. it will say this branch is x commits behind tony:master. grab the remote for tony url and  pull his remote on my machine so git remote add tony url and git pull tony master

11. delete branch add-new-index-js by git branch -d add-new-index-js for the sake of a good practice after merging the pull request

12. git push to be in sync with my origin master and tony master 

this is one cycle about collaborating with someone.
