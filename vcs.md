# Using Git Version Control System #

[RubyMine] handles several different version control system including [CVS], [Mercurial], [Subversion], [Perforce] and [Git].  Help can be found at the [RubyMine git reference].

Here we setup a [git] repository and then create and push updates to a [GitHub] repository all inside the [RubyMine] IDE.

## Git ##

### Initial Setup ###


You can put the project under `git` from within the IDE. Select **Import into Version Control** under the **VCS** menubar item and pick **Create Git Repository**.

![git init]

Make sure you have the correct directory entered. 

![git init select directory]

In the bottom part of the [RubyMine] IDE is the version control console. This shows just how `git` was used.

![git init log]

### Adding Changes ###


Once we have setup the initial git repository the **VCS** menubar menu selections change. Now there is a **Git** entry and we can use this to add files to the repository.  This is especially useful for adding individual files.

![git add]

In the bottom of the IDE you can select **Version Control** and see all the files that have been added and those that are still unversioned.  Select all the unversioned files and right click and select **Add to VCS**. 

![git add all]

Once all files are added you can select **Commit Changes** from the **VCS** menubar item.

![git commit]

Now you have another option to remove files from this commit by unchecking the appropriate box. There are a number of other options. I have unchecked **Perform code analysis** and **Check TODO (Show All)**

![git commit message]

The **Version Control Console** shows the result of the commit.

![git commit log]

### Creating a Branch ###

### Merging Branch in Master ###

In git you should do your work in a branch then switch back to the master branch and merge your changes.  In my opinion this is a good idea even if you are working alone. See [Ruby on Rails Tutorial git Merge notes] and [Pro Git rebase] for more info on `merge` and the alternative `rebase`.  See [RubyMine rebase support] in their online help for 

![Merge Branches](images/GitBranchMerge1.png)

Then select **master -> origin/master > Checkout** option from **Git Branches** popup menu. This will set you back on the master branch.

![Checkout Master Branch](images/GitBranchMerge2.png)

Then select the **VCS** menubar item and then the **Git > Merge Changes...** dropdown menu item.

![Merge1](images/GitBranchMerge3.png)

This brings up a dialog box showing the current branch and a list of branches to merge.  You can hold cursor over different strategy opptions to get a short description.

![Merge1](images/GitBranchMerge4.png)

After the merge you can see a summary of the merge operation. In this part of the tutorial we deleted the `index.html` file.

![Merge1](images/GitBranchMerge5.png)

### Delete Branch ###

I find it useful to create a branch, make my changes then merge back into master. Afterward I usually clean up the repository by deleting the branch. See [Ruby on Rails Tutorial git Merge notes].

Deleting a branch is very simple.  Just click on **VCS** menubar item then select **Git > Branches**. 

![Delete git branch] (images/DeletingBranchStep1.png)

You will be presented a list of branches.  In this case we want to remove the `static-pages`.

![Delete git branch] (images/DeletingBranchStep2.png)

## GitHub ##

### Initial Setup ###


It is possible to create new repositories on your [GitHub] account. Under the **VCS** menubar item select **Import into Version Control >> Share project on GitHub**

![github share]

You will then be prompted for your [GitHub] password.

![github password]

Then enter the name of the new repository and a description.

![github description]

Then you may be prompted for the passphrase for your SSH key. 

![github passphrase]

It will then do the first push of the project up to [GitHub] and the transactions are logged in the Version Control Console.

![Version Control Console][github push log]

### Pushing to GitHub ###



## Heroku ##

### Initial Setup ###

### Pushing to Heroku ###



[RVM]: http://beginrescueend.com/ "Ruby Version Manager"
[Ruby]: http://www.ruby-lang.org/
[install RVM]: https://rvm.beginrescueend.com/rvm/install/
[RubyGems]: http://rubygems.org/
[Ruby on Rails Tutorial]: http://ruby.railstutorial.org/ruby-on-rails-tutorial-book?version=3.2 "Second Edition"
[RubyMine]: http://www.jetbrains.com/ruby/
[GitHub]:http/github.com
[rubymine git reference]:http://www.jetbrains.com/ruby/webhelp/git-reference.html
[cvs]:http://en.wikipedia.org/wiki/Concurrent_Versions_System
[Mercurial]:http://en.wikipedia.org/wiki/Mercurial
[subversion]:http://en.wikipedia.org/wiki/Subversion
[perforce]:http://en.wikipedia.org/wiki/Perforce
[git]:http://en.wikipedia.org/wiki/Git_(software)
[Ruby on Rails Tutorial git Merge notes]:http://ruby.railstutorial.org/chapters/beginning#sec:git_merge
[Pro Git rebase]:http://progit.org/book/ch3-6.html
[RubyMine rebase support]:http://www.jetbrains.com/ruby/webhelp/rebasing-branches.html

[git init]:images/first_project_git_init.png
[git init select directory]:images/first_project_git_init_select.png
[git init log]:images/first_project_git_log.png
[git add]:images/first_project_git_add.png
[git add all]:images/first_project_git_add_all.png
[git commit]:images/first_project_git_commit.png
[git commit message]:images/first_project_git_commit_message.png
[git commit log]:images/first_project_git_commit_log.png
[github password]:images/first_project_github_password.png
[github description]:images/first_project_github_description.png
[github passphrase]:images/first_project_github_passphrase.png
[github share]:images/first_project_git_push.png
[github push log]:images/first_project_push_log.png

