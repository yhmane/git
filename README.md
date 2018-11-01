# git
Study

## git branch
You can use branch command when you want to see branch list. Below is branch command examples.

<pre><code>git branch                        ## shows local branch list
git branch -r                     ## shows remote branch list
git branch -a                     ## shows local and remote branch list 
git branch [new branch]           ## checkout new branch
</code></pre> 

If you want to delete local branch [example]
<pre><code>git checkout master
git branch -d example
</code></pre> 

And you also want to delete the branch from remote server.
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
<pre><code>git commit                        ## If you enter this command, then your cgi turns on commit write pages
git commit -m "[commit message]" ## You can write your command easily</code></pre>
4 . Finally push your commit
<pre><code>git push</code></pre>
## git pull

## git checkout

## git merge

## git status

## git commit

## git abort

## git cherry-pick

## git log
