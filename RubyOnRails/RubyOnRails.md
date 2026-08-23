# RubyOnRails

# RubyOnRails

    
    
    
    
    
    
This document describes using Ruby On Rails in the NetBeans IDE 6.1.

    

    
The IDE comes bundled with JRuby. You can configure the IDE to use other Ruby platforms that are installed on your computer. You can use Tools > Ruby Platforms to register the other Ruby Platforms. You can choose the platform when you create the project or use the Project Properties dialog box to change it later.

    
To create a Rails project, choose New Project from the pop-up menu. Then select
Ruby from the Categories pane, and 
select either Ruby on Rails Application or Ruby on Rails 
Application With Existing Sources from the
Projects pane.

    
After you click Finish, the IDE runs Rails code generator and produces a logical
view on top of the Rails file structure. The project view separates controllers from models,
views, database migrations, and so on.

    
[http://wiki.netbeans.org/wiki/attach/RubyOnRails/rails-2_RubyOnRails.png](https://web.archive.org/web/20111127133640/http://wiki.netbeans.org/wiki/attach/RubyOnRails/rails-2_RubyOnRails.png)

    
The most important operation we'll be doing is running the Rails code generator.
Right-click on the project (or one of the project nodes) and choose Generate.

    
[http://wiki.netbeans.org/wiki/attach/RubyOnRails/rails-0_RubyOnRails.png](https://web.archive.org/web/20111127133640/http://wiki.netbeans.org/wiki/attach/RubyOnRails/rails-0_RubyOnRails.png)

    
You can
then choose what to generate, as well as how to deal with file conflicts.

    
[http://wiki.netbeans.org/wiki/attach/RubyOnRails/extra-generators_RubyOnRails.png](https://web.archive.org/web/20111127133640/http://wiki.netbeans.org/wiki/attach/RubyOnRails/extra-generators_RubyOnRails.png)

    
Usage information for each generator is displayed in the dialog box.

    
You can also directly install additional code generators (such as the login generator) from this
panel by clicking the Install button.

    
The output of the code generator is shown in the Output window. The output is also processed
so that you can click directly on created files and skipped files in order to display them in the source editor, as shown below.

    
[http://wiki.netbeans.org/wiki/attach/RubyOnRails/rails-5_RubyOnRails.png](https://web.archive.org/web/20111127133640/http://wiki.netbeans.org/wiki/attach/RubyOnRails/rails-5_RubyOnRails.png)

    
When editing ERB files, the HTML, the ERB directives, and the
embedded Ruby code are highlighted

    
You can jump between actions and views using the "Goto Action/View" item, which is available
in the context menu for both Ruby and ERB files, as well as bound to Ctrl-Shift-A (Command-Shift-A
on the Mac).

    
WEBrick, the built-in Ruby web server, is automatically started on project creation (as well as on Run, if not already running).
There is a WEBrick console window which shows the output of the web server. It will list the requests it has processed,
which works similar to the Memory Monitor in NetBeans as it lets you watch your requests fly by.

    
You can use the Mongrel server as well, just install it via the Gem Manager. You can use the Project Properties dialog box to specify which server to use for a project.

    
[http://wiki.netbeans.org/wiki/attach/RubyOnRails/mongrel_RubyOnRails.png](https://web.archive.org/web/20111127133640/http://wiki.netbeans.org/wiki/attach/RubyOnRails/mongrel_RubyOnRails.png)

    
When you Run your project, the Run action will open the browser on the welcome page of your Rails application. There
is no deployment step; the application is already deployed in place. If you click on Run File, it will open
the browser on a more specific page; for example, the view page corresponding to the controller you are editing.

    
[http://wiki.netbeans.org/wiki/attach/RubyOnRails/rails-6_RubyOnRails.png](https://web.archive.org/web/20111127133640/http://wiki.netbeans.org/wiki/attach/RubyOnRails/rails-6_RubyOnRails.png)

    
Hint:
     
     Hitting Shift-F6 on any file "executes" it. In Rails, it will open the most relevant URL to the 
controller, action, view, or helper you are editing. For unit tests, it will execute the unit test. For
database migrations, it will migrate to the level of the migration file.

    

    
You can run Rake Targets by using the Rake Target context menu. The target descriptions are tooltips
on the menu items. To refresh the list of targets (if you have installed additional plugins or have edited
your Rakefiles), select the Refresh Targets item.

    
[http://wiki.netbeans.org/wiki/attach/RubyOnRails/rake-targets_RubyOnRails.png](https://web.archive.org/web/20111127133640/http://wiki.netbeans.org/wiki/attach/RubyOnRails/rake-targets_RubyOnRails.png)

    
To run Rake Migrations, select "Migrate Database" in the context menu as shown above. Choose
"To Current Version" to migrate the database to the most recent level, or choose one of the explicit versions
listed.

    
For more informationon using Ruby on Rails 2.0 in NetBeans IDE 6.1, see the
     [Creating a Rails 2.0 Ruby Weblog in 10 Minutes](https://web.archive.org/web/20111127133640/http://www.netbeans.org/kb/61/ruby/rapid-ruby-weblog.html)
     tutorial (NetBeans IDE 6.1 / Rails 2.0 version).

    
For additional Ruby support information, view this
     [wiki page](../Ruby/Ruby.md)
     .

    
    
     Retrieved from "
     [http://wiki.netbeans.org/RubyOnRails](../RubyOnRails/RubyOnRails.md)
     "
