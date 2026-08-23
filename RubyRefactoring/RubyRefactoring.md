# RubyRefactoring

# RubyRefactoring

    
    
    
    
    
    
     
      
       
        ## Contents

       
       - [1
          
          
           Current Release (6.1)](#Current_Release_.286.1.29)
         
          
           [1.1
            
            
             Find Usages](#Find_Usages)
- [1.2
            
            
             Rename](#Rename)
- [1.3
            
            
             Extract Method](#Extract_Method)
- [1.4
            
            
             Introduce Variable, Introduce Field, Introduce Constant](#Introduce_Variable.2C_Introduce_Field.2C_Introduce_Constant)
- [1.5
            
            
             Other Refactorings](#Other_Refactorings)

        
        
         [2
          
          
           Work in Progress (6.5)](#Work_in_Progress_.286.5.29)
        
       
      
     
    
    
     if (window.showTocToggle) { var tocShowText = "show"; var tocHideText = "hide"; showTocToggle(); }
    
    

    
    
    ### Current Release (6.1)

    
This documents describes refactoring support in NetBeans
     [Ruby](../Ruby/Ruby.md)
     .

    
    
    #### Find Usages

    
Right-click on a symbol and choose Find Usages (or use the keyboard shortcut). For this example, I searched for the usages of the
     
      UserMail
     
     class in the Mephisto Rails blogging application (click the image to view full size):

    
[http://blogs.sun.com/tor/resource/ref1.png](https://web.archive.org/web/20111127132911/http://blogs.sun.com/tor/resource/ref1-small.png)

    
This feature also knows about .rhtml and .erb files - it parses the embedded Ruby and analyzes it. Here's an example where I've searched for the usages of a @comments field in a controller, notice the .rhtml matches:

    
[http://blogs.sun.com/tor/resource/ref6.png](https://web.archive.org/web/20111127132911/http://blogs.sun.com/tor/resource/ref6.png)

    
In the Find usages dialog I can also find subtypes of the class rather than usages. Here's an example of what is displayed when I search for subclasses of the
     
      ApplicationController
     
     class:

    
[http://blogs.sun.com/tor/resource/ref4.png](https://web.archive.org/web/20111127132911/http://blogs.sun.com/tor/resource/ref4.png)

    
TODO:

    - Implement optional search in Other Files

    
    
    #### Rename

    
For this example, we will rename the
     
      @comments
     
     field in the Rails application controller. Right-click on it, enter a new name and click OK. Next, click "Preview". The bottom window displays a list of refactoring operations, along with diffs for the currently selected item. You can walk through the changes with the Up/Down arrows, and unselect any changes that you do not like before clicking the Refactor button to apply the changes. Click on the image to view full size (both the dialog and the results window are displayed here as an example). In NetBeans, the dialog box will be displayed first. After clicking Preview, the dialog is removed and you will only see the bottom window.

    
[http://blogs.sun.com/tor/resource/ref2.png](https://web.archive.org/web/20111127132911/http://blogs.sun.com/tor/resource/ref2-small.png)

    
Again, notice how the renaming operation includes changes in .rhtml files. The advantage of this approach over a regular Search/Replace editor operation is that by using parse trees, we have a lot more confidence in the matches. The IDE will not confuse a local variable reference to foo with a method named foo. It does however still have difficulties knowing whether symbols and method names that occur in multiple places refer to say the same method, so at this point it errs on the side of optimism and presents them all as potential uses.

    
TODO:

    - When renaming methods, offer to leave a delegating method which forwards the call
- Implement optional search/replace in Other Files

    
    
    #### Extract Method

    
This refactoring is implemented as a quickfix -- just select the code fragment to be extracted and a light bulb will show up in the left margin. Click on it (or press Alt-Enter) and you will be allowed to extract the selection into a method:

    
[http://blogs.sun.com/tor/resource/extract_method3.png](https://web.archive.org/web/20111127132911/http://blogs.sun.com/tor/resource/extract_method3.png)

    
NOTE: The Refactoring menu has an Extract Method item that is always grayed out in Ruby files. This is because that particular action is hardcoded to the Java refactoring for extract method. We will fix that in an upcoming release.

    
(This refactoring was added in NetBeans 6.1)

    
    
    #### Introduce Variable, Introduce Field, Introduce Constant

    
This refactoring is implemented as a quickfix -- just select the code fragment to be extracted and a light bulb will show up in the left margin. Click on it (or press Alt-Enter) and you will be allowed to extract the selection into a variable/field/constant:

    
[http://blogs.sun.com/tor/resource/introduce2.png](https://web.archive.org/web/20111127132911/http://blogs.sun.com/tor/resource/introduce2.png)

    
NOTE: The Refactoring menu has an Introduce... item that is always grayed out in Ruby files. This is because that particular action is hardcoded to the Java refactoring for introduce variable. We will fix that in an upcoming release.

    
(This refactoring was added in NetBeans 6.1)

    
    
    #### Other Refactorings

    
There are MANY other refactorings. These are all provided as quickfixes (like extract method above) - a lightbulb appears in the left margin when the caret is near some refactorable code.
For example, if you place the caret at the beginning of a block, you get options to convert between do-end and {} blocks, collapse and expand the block between single-line and multi-line
blocks, etc.:

    
[http://wiki.netbeans.org/wiki/attach/RubyHints/convert-collapse.png](https://web.archive.org/web/20111127132911/http://wiki.netbeans.org/wiki/attach/RubyHints/convert-collapse.png)

    
Go to the
     [Ruby Hints](../RubyHints/RubyHints.md)
     page for a list of the current quickfixes.

    
Here's a list of other refactorings we could provide (feel free to edit this wiki page and add your own, or add information on any of these):

    - Inline Method (opposite of Extract Method)
- Inline Local Variable (opposite of Extract Local Variable)
- Inline Constant (opposite of Extract Constant)

    
    
    ### Work in Progress (6.5)

    
Information to be posted soon.

    
    
     Retrieved from "
     [http://wiki.netbeans.org/RubyRefactoring](../RubyRefactoring/RubyRefactoring.md)
     "
