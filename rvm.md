# Ruby Version Manager #

Use of RVM (Ruby Version Manager) allows us to work several Ruby and Rails projects that may require different versions ruby, rails and gems. One interesting thing happened while I was working on the tutorial.  Michael changed the version of Rails to 3.2.3 and there is a trick with RVM that makes this easy to do.

[[#foo|install]]
## Installing RVM ##


To [install RVM] on my Mac I followed the directions on the [RVM] site. Since I already had RVM installed I just asked RVM to install the `head` version then reload itself.

```bash
    $ rvm get head && rvm reload
```

The version of [RVM] installed is:
 
```bash
    rvm 1.11.3 () by Wayne E. Seguin <wayneeseguin@gmail.com>, Michal Papis <mpapis@gmail.com> 
```

<a name="ruby"/>
## Install Ruby ##


Now to install [Ruby].  The default ruby version is 1.9.3-p0 but I wanted the latest (at the time of this writing).

```bash
    $ rvm install 1.9.3-p125
    $ ruby --version
    ruby 1.9.3p125 (2012-02-16 revision 34643) [x86_64-darwin11.3.0]
```

Now check the ruby gems that you get by default

```bash
    $ gem list	
		*** LOCAL GEMS ***		
	bundler (1.1.3)
	rake (0.9.2.2, 0.9.2)
	rubygems-bundler (0.2.8)
	rvm (1.11.3.3)
```

Now a quick check of the latest version at [RubyGems]

```ruby
	bundler          => 1.1.3
	rake             => 0.9.2.2
	rubygems-bundler => 0.2.8
	rvm              => 1.11.3.3
 ```


<a name="gemset"/>
## Define Gemset ##


Setup a gem set

```bash
	$ rvm use 1.9.3-p125@rails3tutorial2ndEd --create --default
	Using /Users/loeffler/.rvm/gems/ruby-1.9.3-p125 with gemset rails3tutorial2ndEd
```

Checking the version and location of `gem`

```bash

	$ which gem
	gem is /Users/loeffler/.rvm/rubies/ruby-1.9.3-p125/bin/gem
	$ gem --version
	1.8.21

```

<a name="installrails"/>
## Install Rails ##


Now to install `rails` (after turning off ri and rdoc documentation)

```bash

	$ gem install rails -v 3.2.2
	Fetching: i18n-0.6.0.gem (100%)
	Fetching: multi_json-1.2.0.gem (100%)
	Fetching: activesupport-3.2.2.gem (100%)
	Fetching: builder-3.0.0.gem (100%)
	Fetching: activemodel-3.2.2.gem (100%)
	Fetching: rack-1.4.1.gem (100%)
	Fetching: rack-cache-1.2.gem (100%)
	Fetching: rack-test-0.6.1.gem (100%)
	Fetching: journey-1.0.3.gem (100%)
	Fetching: hike-1.2.1.gem (100%)
	Fetching: tilt-1.3.3.gem (100%)
	Fetching: sprockets-2.1.2.gem (100%)
	Fetching: erubis-2.7.0.gem (100%)
	Fetching: actionpack-3.2.2.gem (100%)
	Fetching: arel-3.0.2.gem (100%)
	Fetching: tzinfo-0.3.32.gem (100%)
	Fetching: activerecord-3.2.2.gem (100%)
	Fetching: activeresource-3.2.2.gem (100%)
	Fetching: mime-types-1.18.gem (100%)
	Fetching: polyglot-0.3.3.gem (100%)
	Fetching: treetop-1.4.10.gem (100%)
	Fetching: mail-2.4.4.gem (100%)
	Fetching: actionmailer-3.2.2.gem (100%)
	Fetching: thor-0.14.6.gem (100%)
	Fetching: rack-ssl-1.3.2.gem (100%)
	Fetching: json-1.6.6.gem (100%)
	Building native extensions.  This could take a while...
	Fetching: rdoc-3.12.gem (100%)
	Depending on your version of ruby, you may need to install ruby rdoc/ri data:
	
	<= 1.8.6 : unsupported
	 = 1.8.7 : gem install rdoc-data; rdoc-data --install
	 = 1.9.1 : gem install rdoc-data; rdoc-data --install
	>= 1.9.2 : nothing to do! Yay!
	Fetching: railties-3.2.2.gem (100%)
	Fetching: rails-3.2.2.gem (100%)
	Successfully installed i18n-0.6.0
	Successfully installed multi_json-1.2.0
	Successfully installed activesupport-3.2.2
	Successfully installed builder-3.0.0
	Successfully installed activemodel-3.2.2
	Successfully installed rack-1.4.1
	Successfully installed rack-cache-1.2
	Successfully installed rack-test-0.6.1
	Successfully installed journey-1.0.3
	Successfully installed hike-1.2.1
	Successfully installed tilt-1.3.3
	Successfully installed sprockets-2.1.2
	Successfully installed erubis-2.7.0
	Successfully installed actionpack-3.2.2
	Successfully installed arel-3.0.2
	Successfully installed tzinfo-0.3.32
	Successfully installed activerecord-3.2.2
	Successfully installed activeresource-3.2.2
	Successfully installed mime-types-1.18
	Successfully installed polyglot-0.3.3
	Successfully installed treetop-1.4.10
	Successfully installed mail-2.4.4
	Successfully installed actionmailer-3.2.2
	Successfully installed thor-0.14.6
	Successfully installed rack-ssl-1.3.2
	Successfully installed json-1.6.6
	Successfully installed rdoc-3.12
	Successfully installed railties-3.2.2
	Successfully installed rails-3.2.2
	29 gems installed

```

Check version of `rails`:

```bash

	$ rails -v
	Rails 3.2.2

```

Now we are ready to create our applications.

<a name="update"/>
## Update Rails (March 31, 2012) ##

Michael has updated the [Ruby on Rails Tutorial] to use [Rails 3.2.3] for reasons given in this [posting](http://news.ycombinator.com/item?id=3781233  "accessible via mass assignment") .

This is not a problem since we are using [RVM].  We could use **[delete][rvm delete]** or **[empty][rvm empty]** with [RVM].  I am going to use **empty** and then try to load up [Rails 3.2.3].  This will remove all the gems installed when we added rails 3.2.2.  

```bash

    $ rvm gemset empty rails3tutorial2ndEd
    Are you SURE you wish to remove the installed gems for gemset 'ruby-1.9.3-p125@rails3tutorial2ndEd' (/Users/loeffler/.rvm/gems/ruby-1.9.3-p125@rails3tutorial2ndEd)?
    (anything other than 'yes' will cancel) > yes
    $ gem list

    *** LOCAL GEMS ***

    bundler (1.1.3)
    rake (0.9.2.2)
    rubygems-bundler (0.2.8)
    rvm (1.11.3.3)

```

Now to install rails 3.2.3.

```bash

    $ gem install rails -v 3.2.3
	Fetching: activesupport-3.2.3.gem (100%)
	Fetching: activemodel-3.2.3.gem (100%)
	Fetching: actionpack-3.2.3.gem (100%)
	Fetching: activerecord-3.2.3.gem (100%)
	Fetching: activeresource-3.2.3.gem (100%)
	Fetching: actionmailer-3.2.3.gem (100%)
	Building native extensions.  This could take a while...
	Depending on your version of ruby, you may need to install ruby rdoc/ri data:
	
	<= 1.8.6 : unsupported
	 = 1.8.7 : gem install rdoc-data; rdoc-data --install
	 = 1.9.1 : gem install rdoc-data; rdoc-data --install
	>= 1.9.2 : nothing to do! Yay!
	Fetching: railties-3.2.3.gem (100%)
	Fetching: rails-3.2.3.gem (100%)
	Successfully installed i18n-0.6.0
	Successfully installed multi_json-1.2.0
	Successfully installed activesupport-3.2.3
	Successfully installed builder-3.0.0
	Successfully installed activemodel-3.2.3
	Successfully installed rack-1.4.1
	Successfully installed rack-cache-1.2
	Successfully installed rack-test-0.6.1
	Successfully installed journey-1.0.3
	Successfully installed hike-1.2.1
	Successfully installed tilt-1.3.3
	Successfully installed sprockets-2.1.2
	Successfully installed erubis-2.7.0
	Successfully installed actionpack-3.2.3
	Successfully installed arel-3.0.2
	Successfully installed tzinfo-0.3.32
	Successfully installed activerecord-3.2.3
	Successfully installed activeresource-3.2.3
	Successfully installed mime-types-1.18
	Successfully installed polyglot-0.3.3
	Successfully installed treetop-1.4.10
	Successfully installed mail-2.4.4
	Successfully installed actionmailer-3.2.3
	Successfully installed thor-0.14.6
	Successfully installed rack-ssl-1.3.2
	Successfully installed json-1.6.6
	Successfully installed rdoc-3.12
	Successfully installed railties-3.2.3
	Successfully installed rails-3.2.3
	29 gems installed

```
[install RVM]:http://beginrescueend.com/rvm/install/
[RVM]:http://beginrescueend.com/
[Rails 3.2.3]: http://weblog.rubyonrails.org/2012/3/30/ann-rails-3-2-3-has-been-released/
[rubygems]: http://rubygems.org/
[rvm delete]:http://beginrescueend.com/gemsets/deleting/
[rvm empty]:http://beginrescueend.com/gemsets/emptying/
[Ruby]: http://www.ruby-lang.org/
