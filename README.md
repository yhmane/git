# git
Study

## global setting
* setting user name, email

<pre><code>git config --list 				## show global list
git config --global user.name "Hwang Yunho"		## set user name
git config --global user.email "hwang9yh@gmail.com"	## set user email
</code></pre>

## git branch
* You can use branch command when you want to see branch list. Below is branch command examples.

<pre><code>git branch                        ## shows local branch list
git branch -r                     ## shows remote branch list
git branch -a                     ## shows local and remote branch list 
git branch [new branch]           ## checkout new branch
</code></pre> 

* If you want to delete local branch [example]
<pre><code>git checkout master
git branch -d example
</code></pre> 

* And you also want to delete the branch from remote server.
Then delete local branch and add one line.
<pre><code>git push origin :example
</code></pre> 

## git push
* You can upload your source files. 
1. Check your local branch which files are unstaged.
<pre><code>git status</code></pre> 
2. Then choose files and add.
<pre><code>git add example.html example2.html    ## this command adds files which you select
git add .                             ## this command adds all the files which are unstaged files
</code></pre>
3. Next, write the commit messages
<pre><code>git commit                       ## If you enter this command, then your cgi turns on commit write pages
git commit -m "[commit message]" ## You can write your command easily</code></pre>
4. Finally push your commit
<pre><code>git push</code></pre>

> Some push way
* push local branch to remote branch
<pre><code>git push [remote server] [local branch]:[remote branch]</code></pre>

* push local branch to same name remote branch
<pre><code>git push [remoete server] [local branch]</code></pre>

## git pull
* You pull sources from remoete server
<pre><code>git pull</code></pre>

## git checkout
* you can checkout another branch from current branch. If you have same branch names, you only checkout.
<pre><code>git checkout [branch]</code></pre>

## git merge
* merge with no commit
<pre><code>gir merge [branch]</code></pre>

## git status
* This command shows the current branch stage status.
<pre><code>git status</code></pre>

* The current sources changed, and you don't want to push to server then enter this command. This command stores the current status to the stash stack.
<pre><code>git stash       ## store the current status
git stash list  ## Show all stash list
git stash apply ## This command applies the last git stash and the last git stash remains on stash list
git stash apply stash@{number} ## This command applies stash@{number}. Number is stash index from 0~
git stash pop   ## This command pop up the last git stash
git stash drop  ## This command drops stash@{0}
git stash drop stash@{number} ## This command drop stash@{number}. Number is stash index from 0~
git stash clear ## This command drops all stash stack.          
</code></pre>

## git commit
* git commit

## git cherry-pick
* If you want to some commits not merged, and another commit needs merge.
<pre><code>git cherry-pick [commit-hash]</code></pre>

## git log
* This command shows commit log
<pre><code>git log</code></pre>
* But, this command only shows commit-hash and date. So there is option -p. So you can shows the source code change.
<pre><code>git log -p
git log -p [commit-hash]  ## you cah shows from the commit-hash
git log --since="2018-11-01" --author="yhmane" ## shows the log since the day that commit user == author</code></pre>

## git tag
* This command shows release version
<pre><code>git tag ## shows the tagging version ex) v1.0 v1.1 ...
git tag -l v1.1.* ## find and show the version like v1.1.1 v1.1.2 ....
</code></pre>

* Add tag. There are two ways adding tag.
<pre><code>git tag v1.0 ## First way is Lightweight Tag. It only shows the version.
git tag -a v1.0 -m"Release version 1.0" ## Second way is Annotated Tag. It shows person, email, date, and messages
</code></pre>

* Push tag to remote repository
<pre><code>git push origin v1.0 ## only push v1.0
git push origin --tags ## if you want to push all tags, then use this command.
</code></pre>

* Delete tag
<pre><code>git tag -d v1.0 ## delete tag local branch.
git push origin :v1.0 ## delete tag from remote repository.
</code></pre>


## git clean
* This command removes untracked files from the working tree
<pre><code>git clean [-d] [-f] [-i] [-n] [-q] [-e <pattern>] [-x | -X] [--] <path>…​...
git clean -f ## removes untracked files
git clean -fd ## removes untracked directories and files
</code></pre>


## git blame
* This command shows what revision and author last modified each line of a file
* If you use this command with git diff command, you can get difference or errors more effectively
<pre><code>git blame [-c] [-b] [-l] [--root] [-t] [-f] [-n] [-s] [-e] [-p] [-w] [--incremental]
	    [-L <range>] [-S <revs-file>] [-M] [-C] [-C] [-C] [--since=<date>]
	    [--progress] [--abbrev=<n>] [<rev> | --contents <file> | --reverse <rev>..<rev>]
	    [--] <file>
git blame [file] ## shows last commit msg&author of file from start to end
git blame -L 5,9 [file] ## shows last commit msg&author of file line 5~9
</code></pre>

## git rebase
* This command reapplies commits on top of another base tip. But I don't recommend this command.
<pre><code>
git rebase -i HEAD~<N>    ## This command shows N~HEAD, N-1~HEAD ... , HEAD
                          ## Then you can choose pick, squash, reword, edit, fixup, exec, drop
                          pick = use commit
                          reword = use commit, but edit the commit message
                          edit = use commit, but stop for amending
                          squash = use commit, but meld into previous commit
                          fixup = like squash, but discard
                          exec = run command using shell
                          drop = remove commit
                          
if you choose the command, then rebase start.
When you have resolved this problem run "git rebase --continue".
If you would prefer to skip this patch, instead run "git rebase --skip".
To check out the original branch and stop rebasing run "git rebase --abort".

If you push commit remote server, then I never recommend rebase ...
</code></pre>


### Git Reference Guide
* https://git-scm.com/docs
