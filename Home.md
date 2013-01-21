# Using RubyMine IDE for Hartl's Rails Tutorial #


This is about how to use [RubyMine] as your editor for the [Ruby on Rails Tutorial] version 3.2 by Michael Hartl. The tutorial covers three applications.  The **first_app** is very simple, the second, **demo_app** has some active record stuff but the third **sample_app** is a full blown application with lots of good stuff to learn from. I highly recommend Michael's work over any other tutorial that I have seen especially because of the depth it goes into as well as breadth.

I have updated these directions after I updated my MacBook Pro to run Mountain Lion.  I did a clean install and copied over just the user files.  This left me with a  pretty clean slate to start over with.

When I worked though Hartl's applications using [RubyMine] I ended project names with **_project** instead of **_app**.  I do this because I worked the tutorial with Sublime Text 2 and wanted to  distinguish easily between the applications.

Table of Contents

* [RVM and Ruby Installation]
* [Setting up RubyMine IDE][Rails Tutorial Notes]
* [Version Control with Git using RubyMine]
* [Running Spork Server inside RubyMine]
* [Convert to PostgreSQL for development and testing]
* [Data Model] for Sample App starting in chapter 6.
* [Rails Console] running inside [RubyMine]
* [Extras]
* [Additional References]

What editors have I tried?  Well, [Aquamacs] was my first choice because I am a long time emacs user (since 1980 with [Multics emacs]).  I did a lot of work setting up the environment and it works pretty well.  But it is still an editor and does not have as much knowledge other tools used like SCSS.  Another was [MacVim] with a ton of rails extensions. Very nice editor and like it almost as much as [Aquamacs].  I even wrote some extensions for [BBEdit] but it was much harder to extend and I gave up. The old gold standard, [textmate] was used for part of 3.0 version of [Ruby on Rails Tutorial] but since I did not purchase version 1.5 I could not try out version 2. So I took a pass on it this time around.  [Sublime Text 2] is great and I would recommend it over [textmate] now.


[Additional References]: https://github.com/perfectionist/sample_project/wiki/AdditionalReferences
[Version Control with Git using RubyMine]:https://github.com/perfectionist/sample_project/wiki/Using-Git-In-RubyMine
[RVM and Ruby Installation]: https://github.com/perfectionist/sample_project/wiki/Ruby-Version-Manager-in-Mountain-Lion
[Running Spork Server]: https://github.com/perfectionist/sample_project/wiki/Running-Spork-in-RubyMine
[Convert to PostgreSQL for development and testing]:  https://github.com/perfectionist/sample_project/wiki/Convert-to-PostgreSQL 
[Data Model]:https://github.com/perfectionist/sample_project/wiki/Data-Model-Using-RubyMine
[Rails Console]:https://github.com/perfectionist/sample_project/wiki/Rails-Console
[Rails Tutorial Notes]: https://github.com/perfectionist/sample_project/wiki/Using-RubyMine-IDE-for-Ruby-on-Rails-Tutorial
[extras]:https://github.com/perfectionist/sample_project/wiki/extras

[Multics emacs]:http://en.wikipedia.org/wiki/Multics_Emacs "Yes I knew Bernie"

[Ruby on Rails Tutorial]: http://ruby.railstutorial.org/ruby-on-rails-tutorial-book?version=3.2 "Second Edition"
[RubyMine]: http://www.jetbrains.com/ruby/
[Ruby on Rails]: http://rubyonrails.org/
[Aquamacs]:http://aquamacs.org/
[MacVim]:http://code.google.com/p/macvim/
[textmate]:http://macromates.com/
[Sublime Text 2]:http://www.sublimetext.com/2
[BBEdit]:http://www.barebones.com/products/bbedit