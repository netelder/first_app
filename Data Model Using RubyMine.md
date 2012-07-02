# Data Model Using RubyMine #

<a name="modeldiagrams"></a>
## Model Dependency Diagrams ##

It is easy to create a data model diagram with [RubyMine].  Here I'll do the model for the **demo_app** in the [Ruby on Rails Tutorial] in [chapter 2].  This app has just 2 models: `user` and `micropost`.  Just pick the **View** item in the RubyMine menu bar (shown below).

![Menu Bar](images/rubymine_menubar.png)

Then select **Show Model Dependency Diagram** **&#8963;&#8997;D** from the drop down menu.

![ModelMenu](images/ShowModelMenu.png)

The diagram is displayed in its own sub window.  There are a number of display options that let you see more or less information and on applications with more models there are various layout options. See the [Model Dependency Diagram video].

![Demo Project Model Diagram](images/DemoProjectModel.png)

The diagram can be exported to a number of different formats.  

![Export Model Diagram Dialog](images/ExportModelDiagramDialog.png)

The PNG format is shown below. **Note:** the **Powered by yFiles** label on the PNG.  This can be removed from the SVG output by using an editor.  But, unfortunately SVG can not be displayed on [GitHub] 

![Exported Demo Model Diagram](images/DemoExportDiagram.png)

If you export with SVG option you should be able to remove the **Powered by yFile** label.  I removed it using [Inkscape].  SVG image may not appear on this wiki so download the [SVG](images/ExportedDemoModelProjectSvg.svg) here.  Here it is converted to PNG

![SVG Converted to PNG](images/g3646.png)

<a name="ch06"></a>
## Chapter 6 User Data Model ##

This is the `User` data model show in [figure 6.2](http://ruby.railstutorial.org/chapters/modeling-users#fig:user_model_initial) in tutorial. On the left from RubyMine, on the right from figure 6.2.

![User Data  Model](images/UserDataModel6.2.png)  ![](http://ruby.railstutorial.org/images/figures/user_model_initial.png)

Structure of the Postgres table `users` (using [pgAdmin] tool) you can compare with [figure 6.3](http://ruby.railstutorial.org/chapters/modeling-users#fig:sqlite_database_browser) for sqlite3 database browser.

![Postgres Query Tool](images/PostgresQueryTool6.3.png)

Data Model after adding password  in section 6.3 (and )including `timestamp` columns in display).

![Data Model with Password](images/UserModelWithPassword.png)

<a name="ch10"></a>
## Chapter 10 Micropost Data Model ##

Model showing just the user specified fields.  When the cursor is over a relationship brings up a popup window with more information.  Here is shows both sides, from the **User** and from **Micropost**.

![Data Model with Microposts](images/chapter10model.png)

This diagram shows all the columns of the tables including the **id** and **timestamp** columns. 
![Data Model with Microposts - all columns](images/chapter10modelall.png)

<a name="ch11"></a>
## Chapter 11 Relationship Data Model ##

This is the final model for the tutorial.  The two diagrams below are the same diagram but the the lower one shows the **followers** and **followed** users uses the **Relationship** class.

![Datamodel with Relationships](images/FinalDataModel.png)

![Datamodel with popup annotation of relationship](images/FinalDataModelAnnotate.png)

[Ruby on Rails Tutorial]:http://ruby.railstutorial.org/
[chapter 2]:http://ruby.railstutorial.org/chapters/a-demo-app#top
[RubyMine]: http://www.jetbrains.com/ruby/
[GitHub]:http://github.com
[pgAdmin]:http://www.pgadmin.org/