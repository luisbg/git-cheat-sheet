<html>
<body>
<div id="table-of-contents">
<div id="text-table-of-contents">
<ul>
<li><a href="#sec-1">Configure</a></li>
<li><a href="#sec-2">Create repositories</a></li>
<li><a href="#sec-3">Make changes</a></li>
<li><a href="#sec-4">Group changes</a></li>
<li><a href="#sec-5">Refactor filenames</a></li>
<li><a href="#sec-6">Suppress tracking</a></li>
<li><a href="#sec-7">Save fragments</a></li>
<li><a href="#sec-8">Review history</a></li>
<li><a href="#sec-9">Redo commits</a></li>
<li><a href="#sec-10">Synchronize changes</a></li>
</ul>
</div>
</div>
<br>
<h2>Git Cheat Sheet</h2>
<br>
<ul>
<li>Configure<a id="sec-1" name="sec-1">
<ul>
<li><code>git config &#x2013;global user.name "[name]"</code>
<ul>
<li>Sets the name you want attached to your commit transactions</li>
</ul>
</li>
<li><code>git config &#x2013;global user.email "[email address]"</code>
<ul>
<li>Sets the email you want attached to your commit transactions</li>
</ul>
</li>
<li><code>git config &#x2013;global color.ui auto</code>
<ul>
<li>Enables helpful colorization of command line output</li>
</ul>
</li>
<li><code>git config &#x2013;global push.default current</code>
<ul>
<li>Update a branch with the same name as current branch if no refspec is given</li>
</ul>
</li>
<li><code>git config &#x2013;global core.editor [editor]</code>
<ul>
<li>Which editor to use when commit and tag that lets you edit messages</li>
</ul>
</li>
<li><code>git config &#x2013;global diff.tool [tool]</code>
<ul>
<li>Specify which command to invoke as the specified tool for git difftool</li>
</ul>
</li>
</ul>
</li>
<li>Create repositories<a id="sec-2" name="sec-2">
<ul>
<li><code>git init [project-name]</code>
<ul>
<li>Creates a new local repository with the specified name</li>
</ul>
</li>
<li><code>git clone [url]</code>
<ul>
<li>Downloads a project and its entire version history</li>
</ul>
</li>
</ul>
</li>
<li>Make changes<a id="sec-3" name="sec-3">
<ul>
<li><code>git status</code>
<ul>
<li>Lists all new or modified files to be committed</li>
</ul>
</li>
<li><code>git status -s</code>
<ul>
<li>Short view of status</li>
</ul>
</li>
<li><code>git diff</code>
<ul>
<li>Shows file differences not yet staged</li>
</ul>
</li>
<li><code>git add [file]</code>
<ul>
<li>Snapshots the file in preparation for versioning</li>
</ul>
</li>
<li><code>git add .</code>
<ul>
<li>Add all modified files to be commited</li>
</ul>
</li>
<li><code>git add '*.txt'</code>
<ul>
<li>Add only certain files</li>
</ul>
</li>
<li><code>git add &#x2013;patch filename.x (or -p for short)</code>
<ul>
<li>Snapshot only chunks of a file</li>
</ul>
</li>
<li><code>git rm [file]</code>
<ul>
<li>Tell git not to track the file anymore</li>
</ul>
</li>
<li><code>git diff &#x2013;staged</code>
<ul>
<li>Show what has been added to the index via git add but not yet committed</li>
</ul>
</li>
<li><code>git diff HEAD</code>
<ul>
<li>Shows what has changed since the last commit.</li>
</ul>
</li>
<li><code>git diff HEAD^</code>
<ul>
<li>Shows what has changed since the commit before the latest commit</li>
</ul>
</li>
<li><code>git diff [branch]</code>
<ul>
<li>Compare current branch to some other branch</li>
</ul>
</li>
<li><code>git difftool -d</code>
<ul>
<li>Same as diff, but opens changes via difftool that you have configured</li>
</ul>
</li>
<li><code>git difftool -d master..</code>
<ul>
<li>See only changes made in the current branch</li>
</ul>
</li>
<li><code>git diff &#x2013;no-commit-id &#x2013;name-only &#x2013;no-merges origin/master&#x2026;</code>
<ul>
<li>See only the file names that has changed in current branch</li>
</ul>
</li>
<li><code>git diff &#x2013;stat</code>
<ul>
<li>See statistics on what files have changed and how</li>
</ul>
</li>
<li><code>git reset [file]</code>
<ul>
<li>Unstages the file, but preserves its contents</li>
</ul>
</li>
<li><code>git commit</code>
<ul>
<li>Record changes to git. Default editor will open for a commit message</li>
</ul>
</li>
<li><code>git commit -m "[descriptive message]"</code>
<ul>
<li>Records file snapshots permanently in version history</li>
</ul>
</li>
<li><code>git commit &#x2013;amend</code>
<ul>
<li>Change the history, editing the HEAD commit</li>
</ul>
</li>
<li><code>git commit --fixup=[sha]; git rebase -i --autosquash</code>
<ul>
<li>Change the history, editing a specific commit other than HEAD</li>
</ul>
</li>
<li><code>git rebase -i HEAD~5</code>
<ul>
<li>Change the history, reword/edit/squash/fix a group of latest commits</li>
</ul>
</li>
</ul>
</li>
<li>Group changes<a id="sec-4" name="sec-4">
<ul>
<li><code>git branch</code>
<ul>
<li>Lists all local branches in the current directory</li>
</ul>
</li>
<li><code>git branch [branch-name]</code>
<ul>
<li>Create a new branch</li>
</ul>
</li>
<li><code>git checkout [branch-name]</code>
<ul>
<li>Switches to the specified branch and updates the working directory</li>
</ul>
</li>
<li><code>git checkout -b &lt;name&gt; &lt;remote&gt;/&lt;branch&gt;</code>
<ul>
<li>Switches to a remote branch</li>
</ul>
</li>
<li><code>git checkout [filename]</code>
<ul>
<li>Return file to it's previous version, if it hasn’t been staged yet</li>
</ul>
</li>
<li><code>git merge [branch]</code>
<ul>
<li>Combines the specified branch's history into the current branch</li>
</ul>
</li>
<li><code>git merge &#x2013;no&#x2013;ff [branch]</code>
<ul>
<li>Merge branch without fast forwarding</li>
</ul>
</li>
<li><code>git branch -a</code>
<ul>
<li>See the full list of local and remote branches</li>
</ul>
</li>
<li><code>git branch -d [branch]</code>
<ul>
<li>Deletes the specified branch</li>
</ul>
</li>
<li><code>git branch -D [branch]</code>
<ul>
<li>Hard branch delete, will not complain</li>
</ul>
</li>
<li><code>git branch -m &lt;old<sub>name</sub>&gt; &lt;new<sub>name</sub>&gt;</code>
<ul>
<li>Rename a branch</li>
</ul>
</li>
</ul>
</li>
<li>Refactor filenames<a id="sec-5" name="sec-5">
<ul>
<li><code>git rm [file]</code>
<ul>
<li>Deletes the file from the working directory and stages the deletion</li>
</ul>
</li>
<li><code>git rm &#x2013;cached [file]</code>
<ul>
<li>Removes the file from version control but preserves the file locally</li>
</ul>
</li>
<li><code>git mv [file-original] [file-renamed]</code>
<ul>
<li>Changes the file name and prepares it for commit</li>
</ul>
</li>
</ul>
</li>
<li>Suppress tracking<a id="sec-6" name="sec-6">
<ul>
<li>.gitignore
<ul>
<li>*.log</li>
<li>build/</li>
<li>temp-*</li>
<li>A text file named .gitignore suppresses accidental versioning of files and paths matching the specified patterns</li>
</ul>
</li>
<li><code>git ls-files &#x2013;other &#x2013;ignored &#x2013;exclude-standard</code>
<ul>
<li>Lists all ignored files in this project</li>
</ul>
</li>
</ul>
</li>
<li>Save fragments<a id="sec-7" name="sec-7">
<ul>
<li><code>git stash</code>
<ul>
<li>Temporarily stores all modified tracked files</li>
</ul>
</li>
<li><code>git stash pop</code>
<ul>
<li>Restores the most recently stashed files</li>
</ul>
</li>
<li><code>git stash list</code>
<ul>
<li>Lists all stashed changesets</li>
</ul>
</li>
<li><code>git stash drop</code>
<ul>
<li>Discards the most recently stashed changeset</li>
</ul>
</li>
</ul>
</li>
<li>Review history<a id="sec-8" name="sec-8">
<ul>
<li><code>git log</code>
<ul>
<li>Lists version history for the current branch</li>
</ul>
</li>
<li><code>git log &#x2013;follow [file]</code>
<ul>
<li>Lists version history for a file, including renames</li>
</ul>
</li>
<li><code>git log &#x2013;pretty=format:"%h %s" &#x2013;graph</code>
<ul>
<li>Pretty commit view, you can customize it as much as you want</li>
</ul>
</li>
<li><code>git log &#x2013;author='Name' &#x2013;after={1.week.ago} &#x2013;pretty=oneline &#x2013;abbrev-commit</code>
<ul>
<li>See what the author has worked on in the last week</li>
</ul>
</li>
<li><code>git log &#x2013;no-merges master..</code>
<ul>
<li>See only changes in this branch</li>
</ul>
</li>
<li><code>git diff [file-branch]&#x2026;[second-branch]</code>
<ul>
<li>Shows content differences between two branches</li>
</ul>
</li>
<li><code>git show [commit]</code>
<ul>
<li>Outputs metadata and content changes of the specified commit</li>
</ul>
</li>
<li><code>git rev-parse --short HEAD</code>
<ul>
<li>Check sha1/unique name of HEAD commit</li>
</ul>
</li>
</ul>
</li>
<li>Redo commits<a id="sec-9" name="sec-9">
<ul>
<li><code>git reset</code>
<ul>
<li>Unstage pending changes, the changes will still remain on file system</li>
</ul>
</li>
<li><code>git reset [commit/tag]</code>
<ul>
<li>Undoes all commits after [commit], preserving changes locally</li>
</ul>
</li>
<li><code>git reset &#x2013;hard [commit]</code>
<ul>
<li>Discards all history and changes back to the specified commit</li>
</ul>
</li>
</ul>
</li>
<li>Synchronize changes<a id="sec-10" name="sec-10">
<ul>
<li><code>git fetch [bookmark]</code>
<ul>
<li>Downloads all history from the repository bookmark</li>
</ul>
</li>
<li><code>git fetch -p</code>
<ul>
<li>Update history of remote branches, you can fetch and purge</li>
</ul>
</li>
<li><code>git merge [bookmark]/[branch]</code>
<ul>
<li>Combines bookmark's branch into current local branch</li>
</ul>
</li>
<li><code>git push</code>
<ul>
<li>Push current branch to remote branch</li>
</ul>
</li>
<li><code>git push [remote] [branch]</code>
<ul>
<li>Manually specify remote and branch to use every time</li>
</ul>
</li>
<li><code>git push -u origin master</code>
<ul>
<li>If a remote branch is not set up as an upstream, you can make it so</li>
</ul>
</li>
<li><code>git pull</code>
<ul>
<li>Downloads bookmark history and incorporates changes</li>
</ul>
</li>
<li><code>git pull [remote] [branch]</code>
<ul>
<li>Specify to pull a specific branch</li>
</ul>
</li>
<li><code>git remote</code>
<ul>
<li>See list of remote repos available</li>
</ul>
</li>
<li><code>git remote -v</code>
<ul>
<li>Detailed view of remote repos available</li>
</ul>
</li>
<li><code>git remote add [remote] [url]</code>
<ul>
<li>Add a new remote</li>
</ul>
</li>
</ul>
</li>
</ul>
</div>
</div>
</body>
</html>
