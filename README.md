Git Pairing Exercise (Courtesy of Ada Developers Academy)
Sort your names alphabetically. The first is person "A" and the second is person "B"
Fork this repo to person A's account
A should use their own laptop, go into the directory where they store projects, and create a directory named poetry.
A then goes into the poetry directory and runs git init
A creates a file in that folder named still_i_rise.txt
A adds and commits that new file locally
A goes on GitHub and creates a repository named poetry
A follows the directions shown by GitHub to add the remote to their local repo
A pushes the local commits up to GitHub
B should then clone the repository to their local machine
A should add B as a collaborator to the repository in GitHub
B then opens the poetry file locally and adds this content of headings
B adds and commits that change, then pushes it to GitHub
A pulls the commit down to their local machine
A creates a branch on their local machine named verse_1 and adds in this content under the appropriate heading
B creates a branch on their local machine named verse_3 and adds in this content under the appropriate heading
A commits the change and pushes their branch to GitHub with git push origin verse_1
B commits the change and pushes their branch to GitHub with git push origin verse_3
A navigates to the homepage of the repository on GitHub. There should be a button available to "Compare and Create Pull Request" for your recently pushed branch (verse_1). Select this option and walk through the steps to Create a Pull Request for this branch.
B Repeats these steps to create a Pull Request for their verse_3 branch
B navigates to the repository on github and selects the tab for "Pull Requests". You should see A's pull request listed. Select this pull request, and use the green "Merge Pull Request" button to merge the PR. This will merge the branch into master on GitHub's copy of the repository. Don't forget to use GitHub's handy "diff" view to visually review the changes in the pull request.
A repeats this process to merge B's pull request.
Now both A and B should checkout the master branch on their machines and pull from master. This will bring down the changes from B and the merge commit from when the branch was merged to master.
Consult this tutorial for more information on working with Pull Requests on GitHub.

Ok, so we're written some "features" successfully. Let's create a conflict:

A fills in verse 2 with this content and commits it locally on master.
B fills in verse 2 with this content and commits it locally on master.
A pushes to master
B pushes to master and it is rejected. B pulls and gets a MERGE CONFLICT
B must manually resolve the conflict to figure out how the lines should be fit together, remove the conflict markers, commit, then push to GitHub.
A then pulls from GitHub and sees the file post-resolution.
Your final work should look like this.

Extension / Alternate Merging Workflow
It's also possible to merge branches on your local machine

B creates a branch on their local machine named caged_bird_1_to_3 and creates a new file under the poetry directory called caged_bird.markdown
B adds this content to the file
B stages and commits the new content, then pushes their branch to github (remember, git push <remote name> <branch name>).
A runs git fetch origin on their local machine. This pulls down all branches from the remote to A's local machine.
A runs git checkout caged_bird_1_to_3 to review the changes made by B
When A is satisfied with caged_bird_1_to_3, then they merge it into master with git checkout master and git merge caged_bird_1_to_3
A then pushes these newly-merged changes (git push origin master) so that B can pull them down.
Now both A and B should checkout the master branch on their machines and pull from master. This will bring down the changes from B and the merge commit from when the branch was merged to master.
Now A should complete this same process with a branch called caged_bird_4_to_6 using this content.
When A has pushed the branch, B should fetch from origin, checkout the branch, review it, then merge it to master.
Once it is merged, B should push to origin, then both partners should checkout master on their local machines and pull from origin to retrieve the newly merged changes.
Your finished product should look like this.