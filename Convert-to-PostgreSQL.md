# Converting to PostgreSQL #

In chapter 3 exercise 3 Michael challenges us to use [PostgreSQL] in development and testing environments since that is what [Heroku] uses in production. 

The Heroku [instructions] use **Homebrew** or **MacPorts** to install [PostgreSQL]. I have used these installers in the past for other software but not for the last few releases of OS X.  Instead I got an installer that works like installing any other Macintosh application from [PostgreSQL for Mac]

I used postgres for several projects in the past.  I used to download installers from the official [PostgreSQL] site but one time I got the *commercial* version by mistake and it caused me some confusion and wasted time trying to back out.  I found another site, [PostgreSQL for Mac], and provides an installer. `pg4mac_912-r2c.dmg` ([download]) which is PostgreSQL  version 9.1.2 plus some utitlities.  

This is the version after installing:

```
$ psql --version
psql (PostgreSQL) 9.1.2
contains support for command-line editing
```

I did not set a password for `postgres` since this is my personal machine and I don't have anything sensitive stored in the database.  This is my `database.yml` after I made the change to the `Gemfile` suggested by Michael.  

```ruby
development:
  host: localhost
  adapter: postgresql
  encoding: utf8
  database: sample_project_development
  pool: 5
  username: 
  password: 

test:
  host: localhost
  adapter: postgresql
  encoding: utf8
  database: sample_project_test
  pool: 5
  username: 
  password: 

production:
  adapter: postgresql
  encoding: utf8
  database: sample_project_production
  pool: 5
  username:
  password:
```

Accessing the development database from the command line:

```
$ psql -U postgres sample_project_development
psql (9.1.2)
Type "help" for help.

sample_project_development=# \d
                List of relations
 Schema |       Name        |   Type   |  Owner   
--------+-------------------+----------+----------
 public | schema_migrations | table    | loeffler
 public | users             | table    | loeffler
 public | users_id_seq      | sequence | loeffler
(3 rows)

sample_project_development=# \l
    List of databases
            Name            |  Owner   |   
----------------------------+----------+
 postgres                   | postgres | 
 sample_project_development | loeffler |  
 sample_project_test        | loeffler |  
 template0                  | postgres | 
 template1                  | postgres |
(5 rows)
```
And here is the first 10 users (at the end of chapter 9)

```sql
SELECT name,email,admin FROM users LIMIT 10;   
```

| name         |            email            | admin |
| -------------------- 	| ---------------------------- 	| :--: 	|
|  Example User         | example@railstutorial.org   | t |
| Dr. Abel Jacobs      | example-1@railstutorial.org | f |
| Silas Kertzmann      | example-2@railstutorial.org | f |
| Krystina Osinski     | example-3@railstutorial.org | f |
| Melvina Lind         | example-4@railstutorial.org | f |
| Kathryn Ward         | example-5@railstutorial.org | f |
| Antwon Berge DVM     | example-6@railstutorial.org | f |
| Dallin Kuhlman PhD   | example-7@railstutorial.org | f |
| Alphonso Stoltenberg | example-8@railstutorial.org | f |
|  Iva Erdman II        | example-9@railstutorial.org | f |
                                                                        

[PostgreSQL for Mac]: http://www.postgresqlformac.com/
[PostgreSQL]:http://www.postgresql.org/
[download]:http://www.postgresqlformac.com/lists/downloads/unified_installer_disk_imag/
[Heroku]:http://www.heroku.com/
[instructions]:https://devcenter.heroku.com/articles/local-postgresql