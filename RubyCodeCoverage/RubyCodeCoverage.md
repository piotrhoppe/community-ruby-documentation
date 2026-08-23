# RubyCodeCoverage

# RubyCodeCoverage

    
    
    
    
    
    
    
    ## Code Coverage Support

    
     
      
       
        ## Contents

       
       - [1
          
          
           Code Coverage Support](#Code_Coverage_Support)
         
          
           [1.1
            
            
             Usage](#Usage)
- [1.2
            
            
             RSpec](#RSpec)
- [1.3
            
            
             More information](#More_information)

        
       
      
     
    
    
     if (window.showTocToggle) { var tocShowText = "show"; var tocHideText = "hide"; showTocToggle(); }
    
    

    
    
    ### Usage

    
Code coverage is fully integrated with the editor: When coverage data is enabled coverage data
is shown in the editor you're working in:

    
[http://blogs.sun.com/tor/resource/rails-coverage2.png](https://web.archive.org/web/20111127133322/http://blogs.sun.com/tor/resource/rails-coverage2.png)

    
You can also view a coverage report with statistics for the whole project (and double click
to jump to the relevant file). On JDK 6, you can click on table headers to sort by that column:

    
[http://blogs.sun.com/tor/resource/ruby-coveragereport.png](https://web.archive.org/web/20111127133322/http://blogs.sun.com/tor/resource/ruby-coveragereport.png)

    
    
    ### RSpec

    
To use the code coverage support with rspec instead of test/unit tests you need add the following either to project.properties or private.properties (located at /nbproject):

    
```

code.coverage.test.action=rspec-all

```

    
There is one catch though: unlike the RSpec Test action in the project node, the code coverage test action will never 
invoke the spec task, but runs all the spec files in the test roots of the project, i.e. something like

    
```

'spec spec/**spec.rb' 

```

    
-- essentially the same what the RSpec Test action does when there is no 'spec' task in the project. This is 
because our rcov wrapper can't handle the spec task as it is; the spec task provides its own means for rcov 
integration. In the future I need to change the wrapper to better hook into rcov so that it could handle this case as 
well, then we should be able to run also the spec task for code coverage.

    
    
    ### More information

    
More information as well as videos showing code coverage in action is available from these
two blog entries:

    - [http://blogs.sun.com/tor/entry/netbeans_screenshot_of_the_week6](https://web.archive.org/web/20111127133322/http://blogs.sun.com/tor/entry/netbeans_screenshot_of_the_week6)
- [http://blogs.sun.com/tor/entry/ruby_code_coverage_in_the](https://web.archive.org/web/20111127133322/http://blogs.sun.com/tor/entry/ruby_code_coverage_in_the)
- [http://www.youtube.com/watch?v=Sj8lIKoCctU](https://web.archive.org/web/20111127133322/http://www.youtube.com/watch?v=Sj8lIKoCctU)

    
    
     Retrieved from "
     [http://wiki.netbeans.org/RubyCodeCoverage](../RubyCodeCoverage/RubyCodeCoverage.md)
     "
