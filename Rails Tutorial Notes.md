# Using RubyMine IDE for Ruby on Rails Tutorial #

## Creating First App in RubyMine ##

These are notes about using RubyMIne to setup the **first_app** of Michael Hartl's [Ruby on Rails Tutorial] 2nd edition.  The intend is to show how to use [RubyMine] version 4 as the editor (and more) for the tutorial. 

This is the [RubyMine] menubar:

![Figure 1. RubyMine Menubar][RubyMine Menubar]

I will be referring to menubar items below, especially the **RubyMine**, **File** , **Run**, **Tools**, and **VCS** tabs.

### Setup IDE ###

The first step is to setup the [RubyMine] IDE to use the RVM defined ruby and gemset. Open the **Preferences** under the **RubyMine** in the menubar. The **Ruby Interpreter** has a drop down menu with RVM gemsets defined on your system.  Pick the that was defined for the tutorial.  

![Figure 2. Setting Ruby version and Gemset in Preferences][Setting Ruby and Gems]

To see the gem sets defined on your system use `rvm gemset list`:

	$ rvm gemset list
	
	gemsets for ruby-1.9.3-p125 (found in /Users/loeffler/.rvm/gems/ruby-1.9.3-p125)
	   global
	=> rails3tutorial2ndEd
	   sasbook

The `rail3tutorial2ndEd` was defined following directions in [Ruby on Rails Tutorial].
	
### Create First Application ###

Unlike the tutorial a new Rails application can be created inside the IDE.  I use `first_project` instead of `first_app`. This was done to keep the work with [Sublime] separate from [RubyMine].

To create a new project select **New Project…** under the **File** menubar item.  Fill in the **Project name** and you can change **Location** but you need to select **Rails application** for the **Project type**.

![New Project Dialog]

After creating a new rails application you can see the output that would normally see if you ran `rails new first_project` at the command line of the terminal window.

![First Project]

### Modify Gemfile ###

Default `Gemfile`

```ruby

	source 'https://rubygems.org'
	
	gem 'rails', '3.2.3'
	
	# Bundle edge Rails instead:
	# gem 'rails', :git => 'git://github.com/rails/rails.git'
	
	gem 'sqlite3'
	
	
	# Gems used only for assets and not required
	# in production environments by default.
	group :assets do
	  gem 'sass-rails',   '~> 3.2.3'
	  gem 'coffee-rails', '~> 3.2.1'
	
	  # See https://github.com/sstephenson/execjs#readme for more supported runtimes
	  # gem 'therubyracer', :platform => :ruby
	
	  gem 'uglifier', '>= 1.0.3'
	end
	
	gem 'jquery-rails'
	
	# To use ActiveModel has_secure_password
	# gem 'bcrypt-ruby', '~> 3.0.0'
	
	# To use Jbuilder templates for JSON
	# gem 'jbuilder'
	
	# Use unicorn as the app server
	# gem 'unicorn'
	
	# Deploy with Capistrano
	# gem 'capistrano'
	
	# To use debugger
	# gem 'ruby-debug19', :require => 'ruby-debug' #
```
**Note:** The file generated is slightly different that the one in the [rails tutorial][ruby on rails tutorial].

After editing the `Gemfile` is:

	source 'https://rubygems.org'
	
	gem 'rails', '3.2.3'
	
	group :development do
	  gem 'sqlite3', '1.3.5'
	end
	
	group :assets do
	  gem 'sass-rails',   '3.2.4'
	  gem 'coffee-rails', '3.2.2'
	
	  gem 'uglifier', '1.2.3'
	end
	
	gem 'jquery-rails', '2.0.0'
	

### Run Bundler	 ###

To run the **bundler** select it under the **Tools** menubar item.

![Bundler]

The installer will present another dialog for additional arguments to run with **bundle install**. 

![Bundler install dialog]

In our case there are no additional arguments.


### Run Server ###

The rails server can be started from inside [RubyMine]. Just select **Run** from menubar and then either select **Run 'Development: first_project'** or **Run…**.  (Remember I named my app `first_project` not `first_app`.)  Here I chose the later.

![Rails Server]

This brings up a selection where you can create custom run configurations or pick one already defined. I chose a predefined one for development.

![Rails Server Dialog]

The web site for `localhost:3000` shows the **Welcome aboard** page indicating success.

![first project web site]

The bottom section of the [RubyMine] IDE displays the server log file.

![Rails Server Log]

### Git ###

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


### GitHub ###

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


[RubyMine Menubar]:images/rubymine_menubar.png "Menubar"
[Setting Ruby and Gems]:images/first_project_settings.png
[New Project Dialog]:images/first_project.png
[First Project]:images/first_project_create_log.png
[Bundler]:images/first_project_bundler.png
[Bundler install dialog]:images/first_project_bundler_args.png
[Rails Server]:images/first_project_server_run.png
[Rails Server log]:images/first_project_server_run_log.png
[Rails Server Dialog]:images/first_project_server_run_selection.png
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
[first project web site]:images/first_project_web_site.png

[RVM]: http://beginrescueend.com/ "Ruby Version Manager"
[Ruby]: http://www.ruby-lang.org/
[install RVM]: https://rvm.beginrescueend.com/rvm/install/
[RubyGems]: http://rubygems.org/
[Ruby on Rails Tutorial]: http://ruby.railstutorial.org/ruby-on-rails-tutorial-book?version=3.2 "Second Edition"
[Sublime]: http://www.sublimetext.com/2 "Sublime Text 2"
[Rails 3.2.3]: http://weblog.rubyonrails.org/2012/3/30/ann-rails-3-2-3-has-been-released/
[rvm delete]: http://beginrescueend.com/gemsets/deleting/
[rvm empty]: http://beginrescueend.com/gemsets/emptying/
[RubyMine]: http://www.jetbrains.com/ruby/
[GitHub]: http://github.com "GitHub"
