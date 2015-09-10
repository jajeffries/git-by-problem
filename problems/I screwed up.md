# I screwed up
Everyone does it, but how can git help us fix it?

## and I want to get rid of everything from the last 10 minutes

    git reset --hard master@{"10 minutes ago"}

`git reset` resets the current HEAD to the specified state. `--hard` means that it will reset both the index (think of this like your local git repo) and the working tree (the files you have on disc). `master` is the branch you are on. The `@` after it lets you specify how far back you want to go. In this case we want to go back ten minutes so we say `"10 minutes ago", but we can also be more specific. For example, to go back 1 month, 1 day and 1 second we could use:

    git reset --hard master@{"1 month 1 day 1 second ago"}

Or to go back to 1 day ago we could use:

    git reset --hard master@{"yesterday"}
    
## and want to temporarily go back to my last commit

    git stash
    
This reverts your working tree back to your last commit, but stores the changes you've made since as a stash. To get your changes back and keep the stash you can use

    git stash apply
    
or to get your changes back and remove the last stash you can use

    git stash pop



