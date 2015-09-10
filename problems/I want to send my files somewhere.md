# I want to send my files somewhere

## like a central repository

	git remote add origin https://github.com/user/repo.git
	git push origin master

Here we are adding a new remote with the address `https://github.com/user/repo.git` and calling it origin. Then we are pushing the contents of our local branch with the name `master` to the remote branch called `origin`. 

Alternatively you can use

	git push -u origin master

which will set the local branch to track changes on the upstream branch. This is often used for linking your repository to github.
