# Extras #

## Model Diagrams ##

It is easy to create a data model diagram with [RubyMine].  Here I'll do the model for the **demo_app** in the [Ruby on Rails Tutorial] in [chapter 2].  This app has just 2 models: `user` and `micropost`.  Just pick the **View** item in the RubyMine menu bar (shown below).

![Menu Bar](images/rubymine_menubar.png)

Then select **Show Model Dependency Diagram** from the drop down menu.

![ModelMenu](images/ShowModelMenu.png)

The diagram is displayed in its own sub window.  There are a number of display options that let you see more or less information and on applications with more models there are various layout options. See the [Model Dependency Diagram video].

![Demo Project Model Diagram](images/DemoProjectModel.png)

The diagram can be exported to a number of different formats.  

![Export Model Diagram Dialog](images/ExportModelDiagramDialog.png)

The PNG format is shown below. **Note:** the **Powered by yFiles** label on the PNG.  This can be removed from the SVG output by using an editor.  But, unfortunately SVG can not be displayed on [GitHub] 

![Exported Demo Model Diagram](images/DemoExportDiagram.png)

SVG (remove yFile using Inkscape)

![SVG](images/ExportedDemoModelProjectSvg.svg)

<object data="images/ExportedDemoModelProjectSvg.svg" type="image/svg+xml" width="100%"/> 


[RubyMine]: http://www.jetbrains.com/ruby/ "Ruby on Rails IDE"
[Ruby on Rails Tutorial]: http://ruby.railstutorial.org/ "Rails Tutorial"
[chapter 2]: http://ruby.railstutorial.org/chapters/a-demo-app?version=3.2#top
[Model Dependency Diagram video]: http://www.jetbrains.com/ruby/demos/rubymine_model_diagram.html
[GitHub]: http://www.github.com/ "GitHub"