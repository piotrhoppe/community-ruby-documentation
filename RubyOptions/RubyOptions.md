# RubyOptions

# RubyOptions

    
    
    
    
    
    
    
    ### Ruby Options

    
This document lists the various command-line options you can start NetBeans with to affect features. These are typically options we've added for experimental features, or perhaps features that we aren't sure about yet - in particular how they're going to show up in the UI.  These flags control functionality that may be broken, and might change from release to release. The below is accurate as of 6.0 (after beta2, although some of the flags apply to beta2 as well.)

    
    
    #### Camel-case navigation

    
By default, word-navigation (delete previous word, jump to previous word, jump to next word, etc.) will navigate by "CamelCase".
For example, if you have "FooControllerTest", delete word will first remove "Test", then "Controller", then "Foo". Similarly,
foo_controller_test will first remove "_test", then "_controller", then "foo".

    
You can turn this off by running NetBeans with this flag:

    
```

-J-Dno-ruby-camel-case-style-navigation=true

```

    
    
    #### Auto-wrapping Comments

    
You can press Ctrl-Shift-P (Command-Shift-P on the Mac) to reformat the current RDoc comment. If you want comments to be automatically reflown as you're editing them, start NetBeans with this flag:

    
```

 -J-Druby.autowrap.comments=true 

```

    

    
    
    #### Auto-continuing Comments

    
Pressing newline -within- a comment will insert a new line as a comment. However, pressing Return at the -end- of a comment
will insert a blank line. The following option will make newlines at the end of comments continue the comment (unless the comment
is on a line with code, where the comment is assumed to just be a single line comment referring to something earlier on the line) :

    
```

-J-Druby.cont.comment=true

```

    
    
    #### Avoiding Parentheses

    
In Ruby, parentheses are optional in method calls - and usage varies. NetBeans tries to be smart and looks at the documentation
for the method you're calling to see if it should use parentheses or not. For example, if you're calling the "render" method
in Rails, it will skip parentheses, but if you call File.exists, it will not.   If you clearly prefer to avoid parentheses even
when spaces are there in the documentation, use the following option. NetBeans will check to see if the expression looks ambiguous,
and will insert parens if necessary, but otherwise prefers spaces:

    
```

-J-Druby.complete.spaces=true

```

    
    
    #### Don't Show Browser

    
As part of starting the Rails server, NetBeans also automatically starts your browser and shows the application url.  If you don't
want this, you can turn it off with

    
```

-J-Drails.nobrowser=true

```

    
(This works in NetBeans 6.5 and up only)

    

    
    
    #### I Feel Lucky!

    
When you control-click (or Command-click on OSX) on a method or class, NetBeans will jump to the declaration unless there are
many possible declaration classes. This happens frequently with classes which in Ruby are "open".  In these scenarios, NetBeans
will pop up a dialog asking you which location to jump to (with its best guess listed first). If you want NetBeans to always
just jump to this location, run with the following option:

    
```

-J-Dgsf.im_feeling_lucky=true

```

    
    
    #### Filtering Gems

    
By default, in a Rails project, NetBeans will make ALL installed gems available to your files - for code completion, go to declaration, etc. Ruby projects include all gems, except for the Rails ones (although ActiveRecord -is- included).  By changing this filtering, you can remove gems that add methods to core classes like Object and Module if you don't want these methods showing up in completion in your own files.

    
You can tweak how gems are included or excluded yourself, through the use of regular expressions. To change it globally, for all Ruby projects (not Rails projects), as follows:

    
```

-J-Druby.prj.includegems=all
-J-Druby.prj.excludegems=^(rails|action[AZ]+|activesupport)-d+.d+.d+(-S+)?$

```

    
The regular expression is matched against the gem file names (e.g. activesupport-1.3.5 or foo-bar-1.2.3-ruby) and if the file is in the includegems pattern it is included, else if it is in the exclude filter, it is excluded, else it is included.

    
For Rails projects, use the same approach except the property names are slightly different:
     
      rails.prj.excludegems
     
     and
     
      rails.prj.includegems
     
     .

    
You can also set these filters on a per-project basis. Edit the
     
      nbproject/project.properties
     
     file in your project, and add these lines:

    
```

ruby.includegems=actionpack
ruby.excludegems=rspec

```

    
(where again, these are regular expressions as shown above.)

    
    
    #### Choosing Ruby Interpreter

    
You can obviously choose your Ruby interpreter through the UI - but if you want to invoke the IDE and force it to use
a particular Ruby interpreter, use the following setting:

    
```

-J-Druby.interpreter=/Applications/Locomotive2/Bundles/standardRailsMar2007.locobundle/i386/bin/ruby

```

    
(Obviously, put your own path to the ruby interpreter binary above)

    
    
    #### Enabling JRuby Fast Debugging (6.1 only)

    
This feature is brand new and requires very fresh JRuby and ruby-debug gem bits.

    
```

-J-Dorg.netbeans.modules.ruby.debugger.force.rdebug=true
-J-Dorg.netbeans.modules.ruby.debugger.fast.not.required=true

```

    
    
    #### Opening a File

    
...and while we're on the topic of startup flags - you can open files in a running NetBeans from other terminal/console windows by running

    
```

$ netbeans --open foo.rb

```

    
This will connect to the running NetBeans, ask it to open the given file and front the IDE.  (P.S. This
     [may be broken](https://web.archive.org/web/20111127132519/http://www.netbeans.org/issues/show_bug.cgi?id=113903)
     on OSX)

    
    
    #### IRB

    
The IRB Console in the Windows | Output menu is hardcoded to always run with JRuby. There are some technical reasons for this;
the colorized prompt, the tab-completion etc. won't work in the current output window.  However, in Rails projects, there is a "Rails Console"
which runs in the output window (albeit without colorized prompts or completion).  This Rails Console is using your own configured
Ruby interpreter.

    
You can get the same behavior (a new menu item in the projects context menu for Ruby projects) which runs IRB in the plain Output window with your chosen Ruby interpreter, by starting the IDE with this flag:

    
-J-Druby.irbconsole=true

    
Note - this doesn't change the behavior of the item in the Windows menu, it adds a new item in the projects context menu.

    
    
    #### Rails Plugins: Including Non-Lib Dirs

    
When indexing your Rails projects, NetBeans only includes the lib/ portion of your Rails plugins. This works well for most plugins, but I've been told there are a couple of plugins that have other important directories, such as the RailsEngine plugin. To make NetBeans scan ALL the directories in the vendor/plugin/ directories, run with this option:

    
```

-J-Druby.include_nonlib_plugins=true

```

    
NOTE: This option was added AFTER the 6.0 code freeze so only works in current dev builds.

    
    
     Retrieved from "
     [http://wiki.netbeans.org/RubyOptions](../RubyOptions/RubyOptions.md)
     "
