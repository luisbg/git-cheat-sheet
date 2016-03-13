## Git cheat sheet

 * Configure tooling
  * git config --global user.name "[name]"
    * Sets the name you want attached to your commit transactions
  * git config --global user.email "[email address]"
    * Sets the email you want attached to your commit transactions
  * git config --global color.ui auto
    * Enables helpful colorization of command line output
  * git config --global push.default current
    * Update a branch with the same name as current branch if no refspec is given
  * git config --global core.editor [editor]
    * Which editor to use when commit and tag that lets you edit messages
  * git config --global diff.tool [tool]
    * Specify which command to invoke as the specified tool for git difftool

 * Create repositories
  * git init [project-name]
    * Creates a new local repository with the specified name
  * git clone [url]
    * Downloads a project nd its entire version history

 * Make changes
  * git status
    * Lists all new or modified files to be committed
  * git status -s
    * Short view of status
  * git diff
    * Shows file differences not yet staged
  * git add [file]
    * Snapshots the file in preparation for versioning
  * git add .
    * Add all modified files to be commited
  * git add '*.txt'
    * Add only certain files
  * git add --patch filename.x (or -p for short)
    * Snapshot only chunks of a file
  * git rm [file]
    * Tell git not to track the file anymore
  * git diff --staged
    * Show what has been added to the index via git add but not yet committed
  * git diff HEAD
    * Shows what has changed since the last commit.
  * git diff HEAD^
    * Shows what has changed since the commit before the latest commit
  * git diff [branch]
    * Compare current branch to some other branch
  * git difftool -d
    * Same as diff, but opens changes via difftool that you have configured
  * git difftool -d master..
    * See only changes made in the current branch
  * git diff --no-commit-id --name-only --no-merges origin/master...
    * See only the file names that has changed in current branch
  * git diff --stat
    * See statistics on what files have changed and how
  * git reset [file]
    * Unstages the file, but preserves its contents
  * git commit
    * Record changes to git. Default editor will open for a commit message
  * git commit -m "[descriptive message]"
    * Records file snapshots permanently in version history
  * git commit --amend
    * Change the history, editing the HEAD commit
  * git commit --fixup=[sha]; git rebase -i --autosquash
    * Change the history, editing a specific commit other than HEAD
  * git rebase -i HEAD~5
    * Change the history, reword/edit/squash/fix a group of latest commits


 * Group changes
  * git branch
    * Lists all local branches in the current directory
  * git branch [branch-name]
    * Create a new branch
  * git checkout [branch-name]
    * Switches to the specified branch and updates the working directory
  * git checkout -b <name> <remote>/<branch>
    * Switches to a remote branch
  * git checkout [filename]
    * Return file to it's previous version, if it hasn’t been staged yet
  * git merge [branch]
    * Combines the specified branch's history into the current branch
  * git merge --no--ff [branch]
    * Merge branch without fast forwarding
  * git branch -a
    * See the full list of local and remote branches
  * git branch -d [branch]
    * Deletes the specified branch
  * git branch -D [branch]
    * Hard branch delete, will not complain
  * git branch -m <old_name> <new_name>
    * Rename a branch

 * Refactor filenames
  * git rm [file]
    * Deletes the file from the working directory and stages the deletion
  * git rm --cached [file]
    * Removes the file from version control but preserves the file locally
  * git mv [file-original] [file-renamed]
    * Changes the file name and prepares it for commit

 * Suppress tracking
  * .gitignore
    * *.log
    * build/
    * temp-*
    * A text file named .gitignore suppresses accidental versioning of files and paths matching the specified patterns
  * git ls-files --other --ignored --exclude-standard
    * Lists all ignored files in this project

 * Save fragments
  * git stash
    * Temporarily stores all modified tracked files
  * git stash pop
    * Restores the most recently stashed files
  * git stash list
    * Lists all stashed changesets
  * git stash drop
    * Discards the most recently stashed changeset

 * Review history
  * git log
    * Lists version history for the current branch
  * git log --follow [file]
    * Lists version history for a file, including renames
  * git log --pretty=format:"%h %s" --graph
    * Pretty commit view, you can customize it as much as you want
  * git log --author='Name' --after={1.week.ago} --pretty=oneline --abbrev-commit
    * See what the author has worked on in the last week
  * git log --no-merges master..
    * See only changes in this branch
  * git diff [file-branch]...[second-branch]
    * Shows content differences between two branches
  * git show [commit]
    * Outputs metadata and content changes of the specified commit
  * git rev-parse --short HEAD
    * Check sha1/unique name of HEAD commit

 * Redo commits
  * git reset
    * Unstage pending changes, the changes will still remain on file system
  * git reset [commit/tag]
    * Undoes all commits after [commit], preserving changes locally
  * git reset --hard [commit]
    * Discards all history and changes back to the specified commit

 * Synchronize changes
  * git fetch [bookmark]
    * Downloads all history from the repository bookmark
  * git fetch -p
    * Update history of remote branches, you can fetch and purge
  * git merge [bookmark]/[branch]
    * Combines bookmark's branch into current local branch
  * git push
    * Push current branch to remote branch
  * git push [remote] [branch]
    * Manually specify remote and branch to use every time
  * git push -u origin master
    * If a remote branch is not set up as an upstream, you can make it so
  * git pull
    * Downloads bookmark history and incorporates changes
  * git pull [remote] [branch]
    * Specify to pull a specific branch
  * git remote
    * See list of remote repos available
  * git remote -v
    * Detailed view of remote repos available
  * git remote add [remote] [url]
    * Add a new remote
