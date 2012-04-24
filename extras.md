# Extras #

<a name="modeldiagrams"></a>
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

If you export with SVG option you should be able to remove the **Powered by yFile** label.  I removed it using Inkscape.  SVG image may not appear on this wiki.

![SVG](images/ExportedDemoModelProjectSvg.svg)



<a name="keys"></a>
## Keyboard Mapping ##

Keymap for Mac, to be nice, is *odd*, for example:

* **&#8984; P** is Parameter info (within method call arguments) not Print
* **&#8984; N** is Go to Class not New File 
* **^N** is New File not Next Line

To name just a couple.  

Mac Keymap ([PDF](http://www.jetbrains.com/ruby/docs/RubyMine_ReferenceCard_Mac.pdf))

Windows Keymap ([PDF](http://www.jetbrains.com/ruby/docs/RubyMine_ReferenceCard.pdf))

<a name="help"></a>
## Online Help ##

http://www.jetbrains.com/ruby/webhelp/getting-help.html

<a name="reformat"></a>
## Reformat Code ##

![Reformat Menu](images/ReformatCodeMenu.png)

![Reformat Menu](images/ReformatCodeDialog.png)

![Reformat Menu](images/ReformatCodeFinished.png)


[RubyMine]: http://www.jetbrains.com/ruby/ "Ruby on Rails IDE"
[Ruby on Rails Tutorial]: http://ruby.railstutorial.org/ "Rails Tutorial"
[chapter 2]: http://ruby.railstutorial.org/chapters/a-demo-app?version=3.2#top
[Model Dependency Diagram video]: http://www.jetbrains.com/ruby/demos/rubymine_model_diagram.html
[GitHub]: http://www.github.com/ "GitHub"