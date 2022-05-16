# README of multi_remote_repo_test

This repository is used for testing the following

- Create a local git repository, don't link to any remote repository (e.g, Github, Gitee, ...)

- Create some files and commit to this local repository, **still**, for the moment, don't link this local repository to any remote (as above said)

- Still create some files, delete some files, edit some files, ... and commit them to this local repository, repeat again and again, until you don't want to do anymore. **Still**, at this point, don't link this local repository to any remote (as above said)

- Link this to an empty remote repository (this remote repository should have been created from remote, e.g., created in Github), by using `git remote add <repo_name> <url>`

  ```sh
  # Command
  git remote add <repo_name> <url>
  # For example, here now I'm in a local git repo
  # and I created an empty remote repo named multi_remote_repo_test in Github,
  # then I link this local git repo to the remote by sepcifying the name and its URL
  git remote add origin git@github.com:Pyrad/multi_remote_repo_test.git
  ```

- After linking it to the remote (for example, here I first linked it to a Github repository named 'multi_remote_repo_test'), push local changes to the remote for the first time. 
  Since the first time there's no corresponding branch in the remote repository, then we should specify one when before pushing for the first time

  ```sh
  # -*-*-*-*-*-*-*-* Choice 1 -*-*-*-*-*-*-*-*
  # Set remote's branch which corresponds this local repo's current branch
  git branch --set-upstream-to=origin/<BRANCH_NAME>
  # Push to remote
  git push
  
  # -*-*-*-*-*-*-*-* Choice 2-*-*-*-*-*-*-*-*
  # Or directly set upstream when pushing for the first time
  git push --set-upstream origin master
  ```

  

- Still create some files, delete some files, edit some files, ... and commit them to this local repository, **and** push them to the remote just added as shown above, repeat again and again, until you don't want to do anymore.

- Now here's the funny part, link this local repository (which already has one remote) to another different   remote repository (e.g., Gitee), by `git remote add <repo_name> <url>`. Of course, this different remote repository should be just created and keep empty.

  ```sh
  # Command
  git remote add <repo_name> <url>
  # For example, here now I'm in a local git repo,
  # and I've already linked it to a remote repo named multi_remote_repo_test in Github,
  # then I link this local git repo to another remote by sepcifying the name and its URL
  git remote add origin git@github.com:Pyrad/multi_remote_repo_test.git
  ```

  

- xx

- xx

- xx

- xx

- 