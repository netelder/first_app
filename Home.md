Author: David Loeffler

# Using RubyMine IDE for Hartl's Ruby on Rails Tutorial #

This is about how to use [RubyMine] as your editor for the [Ruby on Rails Tutorial] version 3.2 by Michael Hartl. The tutorial covers three applications.  The `first_app` is very simple, the second, `demo_app` has some active record stuff but the third `sample_app` is a full blown application with lots of good stuff to learn from. I highly recommend Michael's work over any other tutorial that I have seen especially because of the depth it goes into as well as breadth.

Some of the discussion I have here is for the earlier apps but it is extremely easy to extend to other apps where easy is just change the app name when filling in new project dialog.  When I work his applications using [RubyMine] I end with `_project` instead of `_app`.  I do this because I worked the tutorial with Sublime Text 2 and wanted to  distinguish easily between them.

* [Setting up RubyMIne IDE][Rails Tutorial Notes]. 
* [Version Control] with Git using [RubyMine]
* [RVM] easy to upgrade to newer version of [Rails on Rails].
* [Running Spork Server] inside [RubyMine]
* [Convert to PostgreSQL] for development and testing
* [Data Model] for Sample App starting in chapter 6.
* [Rails Console] running inside [RubyMine]
* [Extras](wiki/extras)
* [Additional References]

What editors have I tried?  Well, [Aquamacs] was my first choice because I am a long time emacs user (since 1980 with [Multics emacs]).  I did a lot of work setting up the environment and it works pretty well.  But it is still and editor and not as much knowledge other tools used like SCSS.  Another was [MacVim] with a ton of rails extensions. Very nice editor and like it almost as much as [Aquamacs].  I even wrote some extensions for [BBEdit] but it was much harder to extend and I gave up. The old gold standard, [textmate] was used for part of 3.0 version of [Ruby on Rails Tutorial] but since I did not purchase version 1.5 I could not try out version 2. So I took a pass on it this time around.  [Sublime Text 2] is great and I would recommend it over [textmate] now.

### FLASH ###
* **04/20/2012** [RubyMine] version 4.0.3 released and includes several [bug fixes].
* **05/06/2012** [RVM] updated to 1.13.4 and everything working fine. Took [RubyMine] down before upgrade.
* **05/06/2012** Updated Ruby to 1.9.3-p194 and redid the install of rails after setting default ruby to 1.9.3-p194.
    Then `cd` to project directory and run `bundle install` and 
    be sure to update Ruby and Gemset in [RubyMine]. To be on the safe side run the bundler in there as well.
* **05/11/2012** Added Ruby version to `Gemfile` to set [ruby version on heroku](http://blog.heroku.com/archives/2012/5/9/multiple_ruby_version_support_on_heroku/).  `heroku run 'ruby -v'` yields `ruby 1.9.3p194 (2012-04-20 revision 35410) [x86_64-linux]` for this project now.
* **05/20/2012** Upgraded [RubyMine] to version 4.5 EAP. Some new stuff is support for PIK and rbenv in addition to [RVM]. Also several [bug fixes](http://youtrack.jetbrains.com/releaseNotes?q=fixed+in%3A+%7BRubyMine+4.5+EAP+%28build+118.472%29%7D+state%3A+Fixed+state%3A+Verified+state%3A+Obsolete+sort+by%3A+priority&token=1klvqpw64f9t19dm1l149grqe&verbose=false)  See [release notes](http://confluence.jetbrains.com/display/RUBYDEV/RubyMine+4.5+EAP+%28build+118.472%29+Release+Notes) for more details of updates from version 4.0.3. 


[Additional References]: https://github.com/perfectionist/sample_project/wiki/AdditionalReferences
[Version Control]: https://github.com/perfectionist/sample_project/wiki/vcs
[RVM]: https://github.com/perfectionist/sample_project/wiki/rvm
[Running Spork Server]: https://github.com/perfectionist/sample_project/wiki/Running-Spork-in-RubyMine
[Convert to PostgreSQL]:  https://github.com/perfectionist/sample_project/wiki/Convert-to-PostgreSQL "COMING SOON!"
[Data Model]:https://github.com/perfectionist/sample_project/wiki/datamodel
[Rails Console]:https://github.com/perfectionist/sample_project/wiki/railsConsole
[Rails Tutorial Notes]: https://github.com/perfectionist/sample_project/wiki/Rails-Tutorial-Notes

[Multics emacs]:http://en.wikipedia.org/wiki/Multics_Emacs "Yes I knew Bernie"

[Ruby on Rails Tutorial]: http://ruby.railstutorial.org/ruby-on-rails-tutorial-book?version=3.2 "Second Edition"
[RubyMine]: http://www.jetbrains.com/ruby/
[Ruby on Rails]: http://rubyonrails.org/
[Aquamacs]:http://aquamacs.org/
[MacVim]:http://code.google.com/p/macvim/
[textmate]:http://macromates.com/
[Sublime Text 2]:http://www.sublimetext.com/2
[BBEdit]:http://www.barebones.com/products/bbedit/index.html?utm_source=df&utm_medium=banner&utm_campaign=bbedit
[bug fixes]:http://youtrack.jetbrains.com/releaseNotes?q=fixed+in%3A+%7BRubyMine+4.0.3+RC+%28build+117.159%29%7D+fixed+in%3A+%7BRubyMine+4.0.3%7D+state%3A+Fixed+state%3A+Verified+state%3A+Obsolete+sort+by%3A+priority&token=1iose10go2jemmny1xrhcsdo2&verbose=false
