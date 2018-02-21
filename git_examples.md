##### switch to master branch:
git checkout master

##### ensure our master is up to date:
git pull remoteRepoName master

#####With the master branch up to date, we'll use git rebase to consolidate:
git rebase -i master

That command will show a list of each commit, as such:

pick fb554f5 This is commit 1
pick 2bd1903 This is commit 2
pick d987ebf This is commit 3

#####Edit the summary shown to you by the rebase command, leaving the commit you want to be the main commit as "pick" and changing all subsequent "pick" commands as "squash":

pick fb554f5 This is commit 1
squash 2bd1903 This is commit 2
squash d987ebf This is commit 3

Write/quit past the editor twice (the second screen would allow you to change the commit message, though I like to keep it the same). At this point, your commits are squashed into one. Run the following command to force a push of the new, consolidated commit:

##### Force a push:
git push -f

This forced push updates the source repository and our commits have become one. If you had already submitted a pull request at GitHub, the pull request would now show only one commit! With one consolidated commit, code review becomes much, much easier!




#### more command examples:

Create and Checkout a New Branch
#branches from currently checked out directory
git checkout -b <branchName>
Checkout a Remote Branch
git checkout -b <localBranchName> origin/<remoteBranchName>
Abort Changes of a File
git checkout -- <fileName>
Modify the Previous Commit's Message
git commit --amend
Partial Change Checkin
git add --edit
Undo the Previous Commit
git revert HEAD^
Temporarily Stash Changes, Restore Later

#### After changes have been made...
git stash

#### Do some other stuff here, like switch branches, merge other changes, etc.

#Re-apply the changes
git stash pop
Delete a Remote Branch
git push origin :<branchName>
Pull in the Latest from a Shared Repository
#### Add a remote branch
git remote add <remoteName> <gitAddress>
	#### For example:  git remote add lightfaceOfficial git://github.com/darkwing/LightFace.git

#### Get changes from that branch
git fetch <remoteName>
Tagging, Deleting, and Pushing Tags
#### Create a Tag
git tag <tagName>

#### Delete the tag
git tag -d <tagName>

#### Push Tags
git push --tags
Who F'd it All Up?
git blame <fileName>
