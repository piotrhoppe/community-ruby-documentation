# RubyTesting

# RubyTesting

    
    
    
    
    
    
     
      
       The information on
       
        this page pertains to NetBeans IDE 6.5 and later
       
       . If you are looking for information about
       
        Ruby Testing in 6.1
       
       ,
       [look here](../RubyTesting61/RubyTesting61.md)
       .
      
     
    
    

    
     
      
       
        ## Contents

       
       - [1
          
          
           Test::Unit](#Test::Unit)
- [2
          
          
           RSpec](#RSpec)
- [3
          
          
           AutoTest](#AutoTest)
- [4
          
          
           Running All Tests](#Running_All_Tests)
- [5
          
          
           Running Current Test](#Running_Current_Test)
- [6
          
          
           Rake integration](#Rake_integration)

      
     
    
    
     if (window.showTocToggle) { var tocShowText = "show"; var tocHideText = "hide"; showTocToggle(); }
    
    

    
    
    ### Test::Unit

    
The built-in testing framework in Ruby,
     
      Test::Unit
     
     , is supported directly. You can create new unit tests from the New menu. You run your unit tests by just invoking Run File (Shift-F6) on files. This opens a test results window with the output from executing the unit tests and test result statistics. Double-clicking the nodes in the statistics panel takes you to the corresponding declaration location in the editor, and you can navigate to the next/previous failure using the arrow buttons.

    
[File:Http://wiki.netbeans.org/attach/RubyTesting/testrunner-1 .png](/web/20111127133248/http://wiki.netbeans.org/wiki/index.php?title=Special:Upload&wpDestFile=Http://wiki.netbeans.org/attach/RubyTesting/testrunner-1_.png)

    
You can see the output from executing the tests also in the output window.

    
[http://wiki.netbeans.org/attach/RubyTesting/testrunner-2_RubyTesting.png](https://web.archive.org/web/20111127133248/http://wiki.netbeans.org/attach/RubyTesting/testrunner-2_RubyTesting.png)

    
The editor context menu has a "Goto Test" action which lets you jump quickly between a class and its corresponding test cases. This action is aware of Rails conventions, RSpec conventions, ZenTest conventions and obviously Test::Unit conventions. It is bound to Ctrl-Shift-T on the Mac; check your context menu to see the keybinding on your system.

    
[http://wiki.netbeans.org/wiki/attach/RubyTesting/goto-test_RubyTesting.png](https://web.archive.org/web/20111127133248/http://wiki.netbeans.org/wiki/attach/RubyTesting/goto-test_RubyTesting.png)

    
    
    ### RSpec

    
RSpec is a framework that provides you a domain specific language for specifying the behavior of your Ruby code in your Ruby and Rails applications. It can help serve as verification, running tests, as well as documentation for what you have written in your application. You may find additional information at
     [Rspec.info](https://web.archive.org/web/20111127133248/http://rspec.info/)
     .

    
If you install the "Rspec" Ruby Gem (use Tools | Ruby Gems), your Rails projects will contain a
     
      spec
     
     directory which can contain specification files. If you open one of these (you can use the Goto Test action described above), you can run the specs by using Run File (Shift F6). This will run the current spec file under rspec. It will obey the file
     
      spec/spec.opts
     
     , but if you want to use a separate set of options when running under the IDE (for example, turning off the red/green colorization flags which don't work well under the IDE), create a file named
     
      spec/spec.opts.netbeans
     
     instead.

    
View the
     [Using RSpec with NetBeans screencast](https://web.archive.org/web/20111127133248/http://www.netbeans.tv/screencasts/Nick-Sieger-Uses-RSpec-with-the-NetBeans-Ruby-Support-305/)
     for a demonstration of behavior driven development using RSpec in the NetBeans Ruby support.

    
    
    ### AutoTest

    
If you install the "ZenTest" Ruby Gem (use Tools | Ruby Gems), your projects will have an "AutoTest" menu item in their context menu. If you invoke it, it will launch AutoTest on your project, which will run unit tests automatically whenever you modify a file. AutoTest can in many cases figure out which unit tests need to be run - this is especially true for Rails projects.  If not, it will run all unit tests.

    
[http://wiki.netbeans.org/wiki/attach/RubyTesting/autotest-menuitem_RubyTesting.png](https://web.archive.org/web/20111127133248/http://wiki.netbeans.org/wiki/attach/RubyTesting/autotest-menuitem_RubyTesting.png)

    
    
    ### Running All Tests

    
By default, the Test and RSpec Test actions in the project context menu try to invoke the corresponding Rake task and run that. So if your project has a 'test' Rake task, that will be run by the Test action. For RSpec Test action the respective Rake task is 'spec'. So in effect these actions are just shortcuts for rake 'test' and 'spec' tasks, if the project has such tasks. If not, they will run all tests found in the test folders of the project; the RSpec Test actions runs all *spec.rb files in those folders and the Test action in turn all *test.rb and test*.rb files.

    
    
    ### Running Current Test

    
You can also run/debug just a single test method. These actions are available both for Test::Unit and RSpec tests.

    - Run Focused Test. Runs the test around the caret in the editor. The default shorcut for this is Alt-Shift-F6.
- Debug Focused Test.  Same as Run Focused Test, but it runs the test under the debugger. The default shorcut is Alt-Shift-F5.

    
If you want to change the default keyboard shortcuts, you'll need to go to Tools > Options > Keymap, locate the actions (under Other, named "Run/Debug Focused Test") and pick something suitable.

    
Note: Running the focused RSpec test does not work with JRuby currently. See this
     [issue](https://web.archive.org/web/20111127133248/http://jira.codehaus.org/browse/JRUBY-3092)
     for more info.

    
    
    ### Rake integration

    
By default the Test Results UI is shown after running the following rake tasks:

    
```
  * Test::Unit: test, and for all tasks starting with test:

```

    
```
  * RSpec: spec

```

    
If you have a rake task that runs tests, but doesn't follow the above naming conventions, you can specify additional task names in the
     
      project.properties
     
     file (or in
     
      private.properties
     
     ). For Test::Unit, you need to specify a property named
     
      test.tasks
     
     and for RSpec
     
      spec.tasks
     
     . So for example if you have the following lines in your
     
      project.properties
     
     :

    
test.tasks=test,my_tests

    
spec.tasks=spec,another_spec_task

    
the Test Result window will be shown when running
     
      test, my_tests, spec
     
     or
     
      another_spec
     
     task. (see also this
     [blog entry](https://web.archive.org/web/20111127133248/http://blogs.sun.com/emononen/entry/update_on_test_runner)
     for an alternative explanation).

    
    
     Retrieved from "
     [http://wiki.netbeans.org/RubyTesting](../RubyTesting/RubyTesting.md)
     "
