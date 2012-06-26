# Data Model Using RubyMine #

[RubyMIne] has a neat tool for visualizing the data model. Under the **View** menu select 
**Show Model Dependency Diagram** &#8963;&#8997;D. Below are diagrams from the evolution of the model from just the `User` to when it includes `User`, `Micropost`, and `Relationship`. 

![View Menu](images/ViewMenuDataModel.png)

<a name="ch06"></a>
## Chapter 6 User Data Model ##

This is the `User` data model show in figure 6.2 in tutorial.

![User Data  Model](images/UserDataModel6.2.png)

Structure of the Postgres table `users` you can compare with [figure 6.3](http://ruby.railstutorial.org/chapters/modeling-users#fig:sqlite_database_browser) for sqlite3 database browser.

![Postgres Query Tool](images/PostgresQueryTool6.3.png)

Data Model after adding password  in section 6.3 (and )including `timestamp` columns in display).

![Data Model with Password](images/UserModelWithPassword.png)

<a name="ch10"></a>
## Chapter 10 Micropost Data Model ##

![Data Model with Microposts](images/chapter10model.png)

![Data Model with Microposts - all columns](images/chapter10modelall.png)

<a name="ch11"></a>
## Chapter 11 Relationship Data Model ##

![Datamodel with Relationships](images/FinalDataModel.png)

![Datamodel with popup annotation of relationship](images/FinalDataModelAnnotate.png)

[RubyMine]: http://www.jetbrains.com/ruby/