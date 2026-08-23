# RubyCodeTemplates

# RubyCodeTemplates

    
    
    
    
    
    
    
    #### Code Templates

    
NetBeans supports "live code templates"; abbreviations that expand into snippets of code when the Tab key is pressed after typing the snippet name in the editor. (The key used for expansion is configurable).

    
For example, typing "class" and pressing Tab will insert a skeleton class declaration, first letting you type in the class name, then putting the caret in the method body. Press Tab or Enter to jump from one live code template parameter to the next.

    
Code templates are assigned per mime type. Thus, a different set of templates apply in a Ruby file than those in RHTML files. (However, we plan to make it work such that within a Ruby section in RHTML, the Ruby abbreviations will apply.)

    
A number of code templates are built-in and can be used directly (such as the TextMate snippets; see below). You can also define your own code templates.

    
[http://wiki.netbeans.org/attach/RubyCodeTemplates/icon-screencast_RubyCodeTemplates.png](https://web.archive.org/web/20111127133159/http://wiki.netbeans.org/attach/RubyCodeTemplates/icon-screencast_RubyCodeTemplates.png)
     Video:
     [Using Live Code Templates](https://web.archive.org/web/20111127133159/http://www.netbeans.tv/screencasts/Tor-Norbye-Uses-Live-Code-Templates-in-the-NetBeans-Ruby-Support-256/)
     .

    
    
    #### Available Code Templates

    
The following two tables list the available code templates:

    
[Ruby](https://web.archive.org/web/20111127133159/http://ruby.netbeans.org/codetemplates-ruby.html)

    
[RHTML](https://web.archive.org/web/20111127133159/http://ruby.netbeans.org/codetemplates-rhtml.html)

    
(These are available as separate HTML files rather than in the wiki because I wasn't sure about the wiki syntax to generate colors for syntax tokens etc.)

    
NOTE:  The templates were updated AFTER beta1 so the above lists may differ from what you're using if you're not on a daily build.

    
    
    #### Bugs

    
Please note that you cannot retype part of a template and then expand it; that's
     [issue 114921](https://web.archive.org/web/20111127133159/http://www.netbeans.org/issues/show_bug.cgi?id=114921)
     .

    
    
    #### Parameters

    
The following table lists the currently supported parameters:

    
     
      
       Parameter Name
      
      
       Explanation
      
     
     
      
       
        ${cursor}
       
      
      
       Defines a position where the caret will be located after the editing of the code template values finishes.
      
     
     
      
       
        ${selection}
       
      
      
       Defines a position for pasting a content of the editor selection. Used by so called 'selection templates' that appear as hints whenever user selects some text in the editor. (See the "Surround With" section below.)
      
     
     
      
       
        ${param_name default="value"}
       
      
      
       Defines the parameter's default value. Set to empty to create a tab stop.
      
     
     
      
       
        ${param_name editable=false}
       
      
      
       Can be used to disable user's editing of the parameter. Useful for creating caret locations (tab stops).
      
     
     
      
       
        ${class}
       
      
      
       Expands to the name of the class surrounding the template expansion location, such as
       
        Foo
       
      
     
     
      
       
        ${classfqn}
       
      
      
       Same as
       
        ${class}
       
       , but instead of just the class name expands to the fully qualified class name, such as
       
        Bar::Baz::Foo
       
      
     
     
      
       
        ${superclass}
       
      
      
       Expands to the name of the superclass of the class surrounding the template expansion location, such as
       
        SuperFoo
       
      
     
     
      
       
        ${method}
       
      
      
       Expands to the name of the method surrounding the template expansion location, such as
       
        foo
       
      
     
     
      
       
        ${methodfqn}
       
      
      
       Same as
       
        ${method}
       
       , but instead of just the class method expands to the fully qualified name, such as
       
        Bar::Baz::Foo#foo
       
      
     
     
      
       
        ${file}
       
      
      
       Expands to the name of the current file, such as
       
        foo_bar.rb
       
      
     
     
      
       
        ${path}
       
      
      
       Expands to the name of the current full file path, such as
       
        /foo/bar/baz.rb
       
      
     
     
      
       
        ${var unusedlocal defaults="i,j,k"}
       
      
      
       Picks the name of an unused local variable in the current scope. It will first try each of the candidates listed in the
       
        defaults
       
       attribute, and if none of those succeed, create another unique name.
      
     
    
    
I'd like to add some additional logical parameters and attributes based on useful code templates you'd like to see. One plausible such parameter would ensure that a particular file is required. If you have ideas in this area, please share.

    
    
    #### Creating & Editing Templates

    
To create or edit a code template, go to the Options/Preferences dialog, and choose Editor | Code Templates.  Select one of the Ruby options from the Language drop-down list to display the code template list. To
     
      edit
     
     a code template, select a code template from the list and edit the Expanded Text field. To
     
      create
     
     a new code template, click New.

    
Examples

    
Let's define the following snippet:

    
[http://wiki.netbeans.org/wiki/attach/RubyEditing/create-template.png](https://web.archive.org/web/20111127133159/http://wiki.netbeans.org/wiki/attach/RubyEditing/create-template.png)

    
(Note - the above screenshot shows an older version of the code template format.
     
      unusedlocal
     
     is no longer a key name, it's an attribute, so the correct
template format should be do |${1 unusedlocal defaults="i,j,k"}| )

    
This snippet is named "dob".  If you type "dob" followed by tab, you end up with a do block.  Notice how at expansion time
the live code template picked an unused variable name among the candidates;
the NetBeans live templates can use semantic program information.

    
[http://wiki.netbeans.org/wiki/attach/RubyEditing/find-unused-local.png](https://web.archive.org/web/20111127133159/http://wiki.netbeans.org/wiki/attach/RubyEditing/find-unused-local.png)

    
Here's another logical snippet using semantic information:

    
[http://wiki.netbeans.org/wiki/attach/RubyEditing/create-ctx-template.png](https://web.archive.org/web/20111127133159/http://wiki.netbeans.org/wiki/attach/RubyEditing/create-ctx-template.png)

    
The screenshot below displays what it expands to. Note that when determining the superclass it doesn't
necessarily just look at the current file. If you were just adding a method to the
     
      Integer
     
     class, it would correctly report
     
      Numeric
     
     as the superclass:

    
[http://wiki.netbeans.org/wiki/attach/RubyEditing/ctx-expansion.png](https://web.archive.org/web/20111127133159/http://wiki.netbeans.org/wiki/attach/RubyEditing/ctx-expansion.png)

    
    
    #### Surround With

    
Some templates can be used as "surround with" templates. When there is an editor selection, a light bulb is presented to the user, and all the surround-with code templates are listed as possible fixes. A code template is considered a surround-with template if it contains both a reference to the ${selection} and contains the parameter "allowSurround":

    
```

${selection line allowSurround}

```

    
    
    #### TextMate Snippets

    
Most of the TextMate snippets have been converted into NetBeans code templates and are now built-in. However, some of them were dropped during the import for various reasons.

    
Here's a list of the snippets which were dropped or modified.  I would really appreciate some help from people familiar with these snippets to report whether there are unexpected behaviors with any of the snippets, or how any of the snippets which were modified or dropped during import should work so that I can write proper NetBeans templates for these.

    
Please edit this wiki if you have additional information, or
     [send information](../RubyFeedback/RubyFeedback.md)
     .

    
Update Sep 23 2007: The templates were updated to the latest .tmbundle versions.

    
```

IMPORT SUMMARY - Ruby.tmbundle
------------------------------

The following snippets were skipped because they were all
assigned to the same tab trigger:
[Eac-] : each_cons(..) { |group| .. }, each_char { |chr| .. }
[Cla] : class ,InsertERb’sOr]
The following  2 snippets were skipped because they are already included in the IDE:
[Begin,{]
The following  18 snippets were skipped because they use regular expression
transformations which is not yet supported:
[Array,Cla,Cla-,Do,Dow,Fet,Fil,Gsu,Inj,Lam,Ope,Opt,Optp,Ste,Sub,Tim,Tra,Upt]
The following  1 snippets were skipped because they use shell commands which is not yet supported:
[=b]

Imported 102 snippets.
Skipped 24 snippets.

Details on modified snippets:
tc: Stripped out tabStop 2 - contains nested evaluation
Dir: Stripped out tabStop 1 - contains nested evaluation
File: Stripped out tabStop 1 - contains nested evaluation
gre: Stripped out tabStop 1 - contains nested evaluation
:: Stripped out tabStop 2 - contains nested evaluation
Md: Stripped out tabStop 1 - contains nested evaluation
Ml: Stripped out tabStop 1 - contains nested evaluation
ope: Stripped out tabStop 1 - contains nested evaluation
Pn-: Stripped out tabStop 1 - contains nested evaluation
Yd-: Stripped out tabStop 1 - contains nested evaluation
Yl-: Stripped out tabStop 1 - contains nested evaluation

IMPORT SUMMARY - Rails on Rails.tmbundle
------------------------------

The following snippets were skipped because they were all
assigned to the same tab trigger:
[Log] : logger.info, logger.fatal, logger.debug, logger.warn, logger.error
[Mcol] : Rename Column, Add Column, Remove Column, Remove / Add Column, Create Column in Table
[Mtab] : Drop Table, Create Table, Drop / Create Table, Rename Table
[Verify] : verify — render, verify — redirect
The following  2 snippets were skipped because they were not bound to the Tab key:
[[Params[… | params[…]], session[…]

Imported 58 snippets.
Skipped 2 snippets.

Details on modified snippets:
bt: Stripped out tabStop 2 - contains nested evaluation
habtm: Stripped out tabStop 2 - contains nested evaluation
hm: Stripped out tabStop 2 - contains nested evaluation
ho: Stripped out tabStop 2 - contains nested evaluation
va: Stripped out tabStop 2 - contains nested evaluation
vaif: Stripped out tabStop 2 - contains nested evaluation
vc: Stripped out tabStop 2 - contains nested evaluation
vcif: Stripped out tabStop 2 - contains nested evaluation
ve: Stripped out tabStop 2 - contains nested evaluation
veif: Stripped out tabStop 2 - contains nested evaluation
vl: Stripped out tabStop 3 - contains nested evaluation
vp: Stripped out tabStop 2 - contains nested evaluation
vpif: Stripped out tabStop 2 - contains nested evaluation
vu: Stripped out tabStop 2 - contains nested evaluation
vuif: Stripped out tabStop 2 - contains nested evaluation
```

    
    
     Retrieved from "
     [http://wiki.netbeans.org/RubyCodeTemplates](../RubyCodeTemplates/RubyCodeTemplates.md)
     "
