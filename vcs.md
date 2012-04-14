# Using Git Version Control System #

[RubyMine] handles several different version control system including [CVS], [Mercurial], [Subversion], [Perforce] and [Git].  Help can be found at the [RubyMine git reference].

Here we setup a [git] repository and then create and push updates to a [GitHub] repository all inside the [RubyMine] IDE.

## Git ##

You can put the project under `git` from within the IDE. Select **Import into Version Control** under the **VCS** menubar item and pick **Create Git Repository**.

![git init]

Make sure you have the correct directory entered. 

![git init select directory]

In the bottom part of the [RubyMine] IDE is the version control console. This shows just how `git` was used.

![git init log]

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


## GitHub ##

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

