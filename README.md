<div id="table-of-contents">
<h2>Table of Contents</h2>
<div id="text-table-of-contents">
<ul>
<li><a href="#sec-1">1. Git cheat sheet</a>
<ul>
<li><a href="#sec-1-1">1.1. Configure tooling</a>
<ul>
<li><a href="#sec-1-1-1">1.1.1. git config &#x2013;global user.name "[name]"</a></li>
<li><a href="#sec-1-1-2">1.1.2. git config &#x2013;global user.email "[email address]"</a></li>
<li><a href="#sec-1-1-3">1.1.3. git config &#x2013;global color.ui auto</a></li>
<li><a href="#sec-1-1-4">1.1.4. git config &#x2013;global push.default current</a></li>
<li><a href="#sec-1-1-5">1.1.5. git config &#x2013;global core.editor [editor]</a></li>
<li><a href="#sec-1-1-6">1.1.6. git config &#x2013;global diff.tool [tool]</a></li>
</ul>
</li>
<li><a href="#sec-1-2">1.2. Create repositories</a>
<ul>
<li><a href="#sec-1-2-1">1.2.1. git init [project-name]</a></li>
<li><a href="#sec-1-2-2">1.2.2. git clone [url]</a></li>
</ul>
</li>
<li><a href="#sec-1-3">1.3. Make changes</a>
<ul>
<li><a href="#sec-1-3-1">1.3.1. git status</a></li>
<li><a href="#sec-1-3-2">1.3.2. git status -s</a></li>
<li><a href="#sec-1-3-3">1.3.3. git diff</a></li>
<li><a href="#sec-1-3-4">1.3.4. git add [file]</a></li>
<li><a href="#sec-1-3-5">1.3.5. git add .</a></li>
<li><a href="#sec-1-3-6">1.3.6. git add '*.txt'</a></li>
<li><a href="#sec-1-3-7">1.3.7. git add &#x2013;patch filename.x (or -p for short)</a></li>
<li><a href="#sec-1-3-8">1.3.8. git rm [file]</a></li>
<li><a href="#sec-1-3-9">1.3.9. git diff &#x2013;staged</a></li>
<li><a href="#sec-1-3-10">1.3.10. git diff HEAD</a></li>
<li><a href="#sec-1-3-11">1.3.11. git diff HEAD^</a></li>
<li><a href="#sec-1-3-12">1.3.12. git diff [branch]</a></li>
<li><a href="#sec-1-3-13">1.3.13. git difftool -d</a></li>
<li><a href="#sec-1-3-14">1.3.14. git difftool -d master..</a></li>
<li><a href="#sec-1-3-15">1.3.15. git diff &#x2013;no-commit-id &#x2013;name-only &#x2013;no-merges origin/master&#x2026;</a></li>
<li><a href="#sec-1-3-16">1.3.16. git diff &#x2013;stat</a></li>
<li><a href="#sec-1-3-17">1.3.17. git reset [file]</a></li>
<li><a href="#sec-1-3-18">1.3.18. git commit</a></li>
<li><a href="#sec-1-3-19">1.3.19. git commit -m "[descriptive message]"</a></li>
<li><a href="#sec-1-3-20">1.3.20. git commit &#x2013;amend</a></li>
</ul>
</li>
<li><a href="#sec-1-4">1.4. Group changes</a>
<ul>
<li><a href="#sec-1-4-1">1.4.1. git branch</a></li>
<li><a href="#sec-1-4-2">1.4.2. git branch [branch-name]</a></li>
<li><a href="#sec-1-4-3">1.4.3. git checkout [branch-name]</a></li>
<li><a href="#sec-1-4-4">1.4.4. git checkout -b &lt;name&gt; &lt;remote&gt;/&lt;branch&gt;</a></li>
<li><a href="#sec-1-4-5">1.4.5. git checkout [filename]</a></li>
<li><a href="#sec-1-4-6">1.4.6. git merge [branch]</a></li>
<li><a href="#sec-1-4-7">1.4.7. git merge &#x2013;no&#x2013;ff [branch]</a></li>
<li><a href="#sec-1-4-8">1.4.8. git branch -a</a></li>
<li><a href="#sec-1-4-9">1.4.9. git branch -d [branch]</a></li>
<li><a href="#sec-1-4-10">1.4.10. git branch -D [branch]</a></li>
<li><a href="#sec-1-4-11">1.4.11. git branch -m &lt;old<sub>name</sub>&gt; &lt;new<sub>name</sub>&gt;</a></li>
</ul>
</li>
<li><a href="#sec-1-5">1.5. Refactor filenames</a>
<ul>
<li><a href="#sec-1-5-1">1.5.1. git rm [file]</a></li>
<li><a href="#sec-1-5-2">1.5.2. git rm &#x2013;cached [file]</a></li>
<li><a href="#sec-1-5-3">1.5.3. git mv [file-original] [file-renamed]</a></li>
</ul>
</li>
<li><a href="#sec-1-6">1.6. Suppress tracking</a>
<ul>
<li><a href="#sec-1-6-1">1.6.1. .gitignore</a></li>
<li><a href="#sec-1-6-2">1.6.2. git ls-files &#x2013;other &#x2013;ignored &#x2013;exclude-standard</a></li>
</ul>
</li>
<li><a href="#sec-1-7">1.7. Save fragments</a>
<ul>
<li><a href="#sec-1-7-1">1.7.1. git stash</a></li>
<li><a href="#sec-1-7-2">1.7.2. git stash pop</a></li>
<li><a href="#sec-1-7-3">1.7.3. git stash list</a></li>
<li><a href="#sec-1-7-4">1.7.4. git stash drop</a></li>
</ul>
</li>
<li><a href="#sec-1-8">1.8. Review history</a>
<ul>
<li><a href="#sec-1-8-1">1.8.1. git log</a></li>
<li><a href="#sec-1-8-2">1.8.2. git log &#x2013;follow [file]</a></li>
<li><a href="#sec-1-8-3">1.8.3. git log &#x2013;pretty=format:"%h %s" &#x2013;graph</a></li>
<li><a href="#sec-1-8-4">1.8.4. git log &#x2013;author='Name' &#x2013;after={1.week.ago} &#x2013;pretty=oneline &#x2013;abbrev-commit</a></li>
<li><a href="#sec-1-8-5">1.8.5. git log &#x2013;no-merges master..</a></li>
<li><a href="#sec-1-8-6">1.8.6. git diff [file-branch]&#x2026;[second-branch]</a></li>
<li><a href="#sec-1-8-7">1.8.7. git show [commit]</a></li>
</ul>
</li>
<li><a href="#sec-1-9">1.9. Redo commits</a>
<ul>
<li><a href="#sec-1-9-1">1.9.1. git reset</a></li>
<li><a href="#sec-1-9-2">1.9.2. git reset [commit/tag]</a></li>
<li><a href="#sec-1-9-3">1.9.3. git reset &#x2013;hard [commit]</a></li>
</ul>
</li>
<li><a href="#sec-1-10">1.10. Synchronize changes</a>
<ul>
<li><a href="#sec-1-10-1">1.10.1. git fetch [bookmark]</a></li>
<li><a href="#sec-1-10-2">1.10.2. git fetch -p</a></li>
<li><a href="#sec-1-10-3">1.10.3. git merge [bookmark]/[branch]</a></li>
<li><a href="#sec-1-10-4">1.10.4. git push</a></li>
<li><a href="#sec-1-10-5">1.10.5. git push [remote] [branch]</a></li>
<li><a href="#sec-1-10-6">1.10.6. git push -u origin master</a></li>
<li><a href="#sec-1-10-7">1.10.7. git pull</a></li>
<li><a href="#sec-1-10-8">1.10.8. git pull [remote] [branch]</a></li>
<li><a href="#sec-1-10-9">1.10.9. git remote</a></li>
<li><a href="#sec-1-10-10">1.10.10. git remote -v</a></li>
<li><a href="#sec-1-10-11">1.10.11. git remote add [remote] [url]</a></li>
</ul>
</li>
</ul>
</li>
</ul>
</div>
</div>

# Git cheat sheet<a id="sec-1" name="sec-1"></a>

## Configure tooling<a id="sec-1-1" name="sec-1-1"></a>

### git config &#x2013;global user.name "[name]"<a id="sec-1-1-1" name="sec-1-1-1"></a>

1.  Sets the name you want attached to your commit transactions

### git config &#x2013;global user.email "[email address]"<a id="sec-1-1-2" name="sec-1-1-2"></a>

1.  Sets the email you want attached to your commit transactions

### git config &#x2013;global color.ui auto<a id="sec-1-1-3" name="sec-1-1-3"></a>

1.  Enables helpful colorization of command line output

### git config &#x2013;global push.default current<a id="sec-1-1-4" name="sec-1-1-4"></a>

1.  Update a branch with the same name as current branch if no refspec is given

### git config &#x2013;global core.editor [editor]<a id="sec-1-1-5" name="sec-1-1-5"></a>

1.  Which editor to use when commit and tag that lets you edit messages

### git config &#x2013;global diff.tool [tool]<a id="sec-1-1-6" name="sec-1-1-6"></a>

1.  Specify which command to invoke as the specified tool for git difftool

## Create repositories<a id="sec-1-2" name="sec-1-2"></a>

### git init [project-name]<a id="sec-1-2-1" name="sec-1-2-1"></a>

1.  Creates a new local repository with the specified name

### git clone [url]<a id="sec-1-2-2" name="sec-1-2-2"></a>

1.  Downloads a project nd its entire version history

## Make changes<a id="sec-1-3" name="sec-1-3"></a>

### git status<a id="sec-1-3-1" name="sec-1-3-1"></a>

1.  Lists all new or modified files to be committed

### git status -s<a id="sec-1-3-2" name="sec-1-3-2"></a>

1.  Short view of status

### git diff<a id="sec-1-3-3" name="sec-1-3-3"></a>

1.  Shows file differences not yet staged

### git add [file]<a id="sec-1-3-4" name="sec-1-3-4"></a>

1.  Snapshots the file in preparation for versioning

### git add .<a id="sec-1-3-5" name="sec-1-3-5"></a>

1.  Add all modified files to be commited

### git add '\*.txt'<a id="sec-1-3-6" name="sec-1-3-6"></a>

1.  Add only certain files

### git add &#x2013;patch filename.x (or -p for short)<a id="sec-1-3-7" name="sec-1-3-7"></a>

1.  Snapshot only chunks of a file

### git rm [file]<a id="sec-1-3-8" name="sec-1-3-8"></a>

1.  Tell git not to track the file anymore

### git diff &#x2013;staged<a id="sec-1-3-9" name="sec-1-3-9"></a>

1.  Show what has been added to the index via git add but not yet committed

### git diff HEAD<a id="sec-1-3-10" name="sec-1-3-10"></a>

1.  Shows what has changed since the last commit.

### git diff HEAD^<a id="sec-1-3-11" name="sec-1-3-11"></a>

1.  Shows what has changed since the commit before the latest commit

### git diff [branch]<a id="sec-1-3-12" name="sec-1-3-12"></a>

1.  Compare current branch to some other branch

### git difftool -d<a id="sec-1-3-13" name="sec-1-3-13"></a>

1.  Same as diff, but opens changes via difftool that you have configured

### git difftool -d master..<a id="sec-1-3-14" name="sec-1-3-14"></a>

1.  See only changes made in the current branch

### git diff &#x2013;no-commit-id &#x2013;name-only &#x2013;no-merges origin/master&#x2026;<a id="sec-1-3-15" name="sec-1-3-15"></a>

1.  See only the file names that has changed in current branch

### git diff &#x2013;stat<a id="sec-1-3-16" name="sec-1-3-16"></a>

1.  See statistics on what files have changed and how

### git reset [file]<a id="sec-1-3-17" name="sec-1-3-17"></a>

1.  Unstages the file, but preserves its contents

### git commit<a id="sec-1-3-18" name="sec-1-3-18"></a>

1.  Record changes to git. Default editor will open for a commit message

### git commit -m "[descriptive message]"<a id="sec-1-3-19" name="sec-1-3-19"></a>

1.  Records file snapshots permanently in version history

### git commit &#x2013;amend<a id="sec-1-3-20" name="sec-1-3-20"></a>

1.  Changing the history, of the HEAD commit

## Group changes<a id="sec-1-4" name="sec-1-4"></a>

### git branch<a id="sec-1-4-1" name="sec-1-4-1"></a>

1.  Lists all local branches in the current directory

### git branch [branch-name]<a id="sec-1-4-2" name="sec-1-4-2"></a>

1.  Create a new branch

### git checkout [branch-name]<a id="sec-1-4-3" name="sec-1-4-3"></a>

1.  Switches to the specified branch and updates the working directory

### git checkout -b <name> <remote>/<branch><a id="sec-1-4-4" name="sec-1-4-4"></a>

1.  Switches to a remote branch

### git checkout [filename]<a id="sec-1-4-5" name="sec-1-4-5"></a>

1.  Return file to it's previous version, if it hasn’t been staged yet

### git merge [branch]<a id="sec-1-4-6" name="sec-1-4-6"></a>

1.  Combines the specified branch's history into the current branch

### git merge &#x2013;no&#x2013;ff [branch]<a id="sec-1-4-7" name="sec-1-4-7"></a>

1.  Merge branch without fast forwarding

### git branch -a<a id="sec-1-4-8" name="sec-1-4-8"></a>

1.  See the full list of local and remote branches

### git branch -d [branch]<a id="sec-1-4-9" name="sec-1-4-9"></a>

1.  Deletes the specified branch

### git branch -D [branch]<a id="sec-1-4-10" name="sec-1-4-10"></a>

1.  Hard branch delete, will not complain

### git branch -m <old<sub>name</sub>> <new<sub>name</sub>><a id="sec-1-4-11" name="sec-1-4-11"></a>

1.  Rename a branch

## Refactor filenames<a id="sec-1-5" name="sec-1-5"></a>

### git rm [file]<a id="sec-1-5-1" name="sec-1-5-1"></a>

1.  Deletes the file from the working directory and stages the deletion

### git rm &#x2013;cached [file]<a id="sec-1-5-2" name="sec-1-5-2"></a>

1.  Removes the file from version control but preserves the file locally

### git mv [file-original] [file-renamed]<a id="sec-1-5-3" name="sec-1-5-3"></a>

1.  Changes the file name and prepares it for commit

## Suppress tracking<a id="sec-1-6" name="sec-1-6"></a>

### .gitignore<a id="sec-1-6-1" name="sec-1-6-1"></a>

1.  \*.log

2.  build/

3.  temp-\*

4.  A text file named .gitignore suppresses accidental versioning of files and paths matching the specified patterns

### git ls-files &#x2013;other &#x2013;ignored &#x2013;exclude-standard<a id="sec-1-6-2" name="sec-1-6-2"></a>

1.  Lists all ignored files in this project

## Save fragments<a id="sec-1-7" name="sec-1-7"></a>

### git stash<a id="sec-1-7-1" name="sec-1-7-1"></a>

1.  Temporarily stores all modified tracked files

### git stash pop<a id="sec-1-7-2" name="sec-1-7-2"></a>

1.  Restores the most recently stashed files

### git stash list<a id="sec-1-7-3" name="sec-1-7-3"></a>

1.  Lists all stashed changesets

### git stash drop<a id="sec-1-7-4" name="sec-1-7-4"></a>

1.  Discards the most recently stashed changeset

## Review history<a id="sec-1-8" name="sec-1-8"></a>

### git log<a id="sec-1-8-1" name="sec-1-8-1"></a>

1.  Lists version history for the current branch

### git log &#x2013;follow [file]<a id="sec-1-8-2" name="sec-1-8-2"></a>

1.  Lists version history for a file, including renames

### git log &#x2013;pretty=format:"%h %s" &#x2013;graph<a id="sec-1-8-3" name="sec-1-8-3"></a>

1.  Pretty commit view, you can customize it as much as you want

### git log &#x2013;author='Name' &#x2013;after={1.week.ago} &#x2013;pretty=oneline &#x2013;abbrev-commit<a id="sec-1-8-4" name="sec-1-8-4"></a>

1.  See what the author has worked on in the last week

### git log &#x2013;no-merges master..<a id="sec-1-8-5" name="sec-1-8-5"></a>

1.  See only changes in this branch

### git diff [file-branch]&#x2026;[second-branch]<a id="sec-1-8-6" name="sec-1-8-6"></a>

1.  Shows content differences between two branches

### git show [commit]<a id="sec-1-8-7" name="sec-1-8-7"></a>

1.  Outputs metadata and content changes of the specified commit

## Redo commits<a id="sec-1-9" name="sec-1-9"></a>

### git reset<a id="sec-1-9-1" name="sec-1-9-1"></a>

1.  Unstage pending changes, the changes will still remain on file system

### git reset [commit/tag]<a id="sec-1-9-2" name="sec-1-9-2"></a>

1.  Undoes all commits after [commit], preserving changes locally

### git reset &#x2013;hard [commit]<a id="sec-1-9-3" name="sec-1-9-3"></a>

1.  Discards all history and changes back to the specified commit

## Synchronize changes<a id="sec-1-10" name="sec-1-10"></a>

### git fetch [bookmark]<a id="sec-1-10-1" name="sec-1-10-1"></a>

1.  Downloads all history from the repository bookmark

### git fetch -p<a id="sec-1-10-2" name="sec-1-10-2"></a>

1.  Update history of remote branches, you can fetch and purge

### git merge [bookmark]/[branch]<a id="sec-1-10-3" name="sec-1-10-3"></a>

1.  Combines bookmark's branch into current local branch

### git push<a id="sec-1-10-4" name="sec-1-10-4"></a>

1.  Push current branch to remote branch

### git push [remote] [branch]<a id="sec-1-10-5" name="sec-1-10-5"></a>

1.  Manually specify remote and branch to use every time

### git push -u origin master<a id="sec-1-10-6" name="sec-1-10-6"></a>

1.  If a remote branch is not set up as an upstream, you can make it so

### git pull<a id="sec-1-10-7" name="sec-1-10-7"></a>

1.  Downloads bookmark history and incorporates changes

### git pull [remote] [branch]<a id="sec-1-10-8" name="sec-1-10-8"></a>

1.  Specify to pull a specific branch

### git remote<a id="sec-1-10-9" name="sec-1-10-9"></a>

1.  See list of remote repos available

### git remote -v<a id="sec-1-10-10" name="sec-1-10-10"></a>

1.  Detailed view of remote repos available

### git remote add [remote] [url]<a id="sec-1-10-11" name="sec-1-10-11"></a>

1.  Add a new remote