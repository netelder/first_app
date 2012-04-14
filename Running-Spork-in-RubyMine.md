# Running Spork #

The `sample_app` application in [Ruby on Rails Tutorial] recommends running [spork] when doing TTD based on [rspec].  The [RubyMine] IDE comes bundled with a [Spork RDb server] an includes directions for its setup and use. Just be sure to include the proper gems in your `Gemfile`.  I am not sure but I think you don't need to use [spork and guard] together if you have the IDE running the Spork RDb server since guard is a command line tool for controlling spork.

![Spork Server]

![Spork Server Options]

![Spork Server Log]

[Spork Server]: images/RunSporkDRbServer.png

[Spork Server Options]: images/RunSporkDRbServerOptions.png

[Spork Server Log]: images/RunSporkDRbServerLog.png


[Ruby on Rails Tutorial]: http://ruby.railstutorial.org/ruby-on-rails-tutorial-book?version=3.2 "Second Edition"
[spork]:http://rubygems.org/gems/spork
[rspec]:http://rspec.info/
[RubyMine]: http://www.jetbrains.com/ruby/
[Spork RDb server]:http://www.jetbrains.com/ruby/webhelp/using-drb-server.html
[Spork and Guard]:http://blog.carbonfive.com/2010/12/10/speedy-test-iterations-for-rails-3-with-spork-and-guard/