# RubyProjects

# RubyProjects

    
    
    
    
    
    
     
      
       
        ## Contents

       
       - [1
          
          
           Gem Support](#Gem_Support)
- [2
          
          
           File Type Recognition](#File_Type_Recognition)
- [3
          
          
           Project Support](#Project_Support)
- [4
          
          
           Unit Tests](#Unit_Tests)
- [5
          
          
           IRB - Interactive Ruby Shell](#IRB_-_Interactive_Ruby_Shell)

      
     
    
    
     if (window.showTocToggle) { var tocShowText = "show"; var tocHideText = "hide"; showTocToggle(); }
    
    

    
    
    #### Gem Support

    
There is a Gem Manager which lets you see which gems you have installed, and install new gems
or update your existing gems.

    
When you open the Gem Manager from the Tools menu, you see your installed gems:

    
[http://wiki.netbeans.org/wiki/attach/RubyProjects/localgems_RubyProjects.png](https://web.archive.org/web/20111127132905/http://wiki.netbeans.org/wiki/attach/RubyProjects/localgems_RubyProjects.png)

    
(These screenshots are old; I recently modified the UI to be similar to the IDE Plugin Manager. Note also that there
is a Rails Plugin manager now, available from the Rails project context menu.)

    
If you click on install new, you see the gems available from the remote repository:

    
[http://wiki.netbeans.org/wiki/attach/RubyProjects/remotegems_RubyProjects.png](https://web.archive.org/web/20111127132905/http://wiki.netbeans.org/wiki/attach/RubyProjects/remotegems_RubyProjects.png)

    
You can filter the list by typing in the filter box - any regular expression will do.

    
    
    #### File Type Recognition

    
Ruby files are recognized in the file system, assigned some default actions, etc.

    
[http://wiki.netbeans.org/wiki/attach/RubyProjects/file-recognition_RubyProjects.png](https://web.archive.org/web/20111127132905/http://wiki.netbeans.org/wiki/attach/RubyProjects/file-recognition_RubyProjects.png)

    
    
    #### Project Support

    
A Ruby project type provides basic projects support: a logical project representation, built in execution
using Ruby or Rake, run profiles, etc. Build errors are hyperlinked to editor source. Basic file skeletons
for simple scripts, classes and modules are provided.

    
[http://wiki.netbeans.org/wiki/attach/RubyProjects/ruby-new-project_RubyProjects.png](https://web.archive.org/web/20111127132905/http://wiki.netbeans.org/wiki/attach/RubyProjects/ruby-new-project_RubyProjects.png)

    
Here's how it looks in the Projects window:

    
[http://wiki.netbeans.org/wiki/attach/RubyProjects/ruby-projects_RubyProjects.png](https://web.archive.org/web/20111127132905/http://wiki.netbeans.org/wiki/attach/RubyProjects/ruby-projects_RubyProjects.png)

    
You can configure the projects to execute with either JRuby (the builtin default), or any other Ruby
installation on your system. Go to the Miscellaneous tab of the Options Panel and point to your Ruby
and Rake binaries. (NOTE - there is a bug which currently blocks native Ruby output from working
correctly in the Output window.)

    
[http://wiki.netbeans.org/wiki/attach/RubyProjects/ruby-home_RubyProjects.png](https://web.archive.org/web/20111127132905/http://wiki.netbeans.org/wiki/attach/RubyProjects/ruby-home_RubyProjects.png)

    
    
    #### Unit Tests

    
Ruby Unit tests are supported; there's is a new unit test template, and when executing unit tests
failures are linked to the editor source.

    
[http://wiki.netbeans.org/wiki/attach/RubyProjects/ruby-unittests_RubyProjects.png](https://web.archive.org/web/20111127132905/http://wiki.netbeans.org/wiki/attach/RubyProjects/ruby-unittests_RubyProjects.png)

    
    
    #### IRB - Interactive Ruby Shell

    
You can open up an interactive IRB shell session from the Windows menu. The IRB window has
lets you interact with JRuby directly. Use arrow keys for command history etc.

    
[http://wiki.netbeans.org/wiki/attach/RubyProjects/irb_RubyProjects.png](https://web.archive.org/web/20111127132905/http://wiki.netbeans.org/wiki/attach/RubyProjects/irb_RubyProjects.png)

    
    
     Retrieved from "
     [http://wiki.netbeans.org/RubyProjects](../RubyProjects/RubyProjects.md)
     "
