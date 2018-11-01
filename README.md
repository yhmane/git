# git
Study

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
You can upload your source files. 
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
You pull sources from remoete server
<pre><code>git pull</code></pre>

## git checkout
* you can checkout another branch from current branch. If you have same branch names, you only checkout.
<pre><code>git checkout [branch]</code></pre>

## git merge
* merge with no commit
<pre><code>gir merge [branch]</code></pre>

## git status
This command shows the current branch stage status.
<pre><code>git status</code></pre>

* The current sources changed, and you don't want to push to server then enter this command. This command stores the current status to the stash stack.
<pre><code>git stash      ## store the current status
git stash pop  ## This command pop up the last git stash</code></pre>

## git commit
* git commit

## git cherry-pick
* If you want to some commits not merged, and another commit needs merge.
<pre><code>git cherry-pick [commit-hash]</code></pre>

## git log
* This command shows commit log
<pre><code>git log</code></pre>
But, this command only shows commit-hash and date. So there is option -p. So you can shows the source code change.
<pre><code>git log -p
git log -p [commit-hash]  ## you cah shows from the commit-hash</code></pre>



### Git Reference Guide
* https://git-scm.com/docs
