# RubyShortcuts

# RubyShortcuts

    
    
    
    
    
    
    
    ### Ruby Shortcuts

    
    
    #### Recent Changes

    - You can run and debug the current test (the one around the caret) with Alt-Shift-F6 (run) or F5 (debug) (and on the Mac, Alt-Shift F6 or F5)
- Generate (Rails Generator Wizard) is bound to Alt-Insert (Ctrl-I on the Mac) when pressed in a .rb file.
- Reformat Comment Paragraph was bound to Ctrl-Shift-P (Command-Shift-P on the Mac)
- Go to test was recently switched from Alt-Shift-E to Ctrl-Shift-T
- Go to declaration was recently switched from Alt-G to Ctrl-B

    
    
    #### Keybindings

    
This is not a complete list of keyboard shortcuts applicable to Ruby development in NetBeans; it is instead a list of some of the most important ones. For a complete set, consult
     [KeymapProfileFor60](/web/20111026065521/http://wiki.netbeans.org/KeymapProfileFor60)
     . A handy but perhaps not as accurate PDF table is
     [here](https://web.archive.org/web/20111026065521/http://wiki.netbeans.org/wiki/attach/HelpSetForAllSeasons/shortcuts.pdf)
     .

    
     
      
       Action
      
      
       Shortcut
      
      
       Mac Shortcut
      
     
     
      
       Show code completion alternatives
      
      
       Ctrl-Space
      
      
       Ctrl-Space
      
     
     
      
       Show documentation for the method, class or field under the caret. (Doesn't always work given Ruby's dynamic nature.)
      
      
       Ctrl-Shift-Space
      
      
       Command-Shift-Space
      
     
     
      
       Show quick and short documentation, hold Ctrl key down and hover your mouse pointer over the method
      
      
       Ctrl- mousepointer
      
      
       Command - mousepointer
      
     
     
      
       Show name of current parameter (when editing an argument list for a method call). (Doesn't always work given Ruby's dynamic nature.)
      
      
       Ctrl-P
      
      
       Command-P
      
     
     
      
       Select applicable quickfix (when a lightbulb is showing next to the current line)
      
      
       Alt-Enter
      
      
       Alt-Enter
      
     
     
      
       Jump between a Rails action (a method in a
       
        controller
       
       file) and its corresponding view (a
       
        .rhtml
       
       or
       
        .erb
       
       file).
      
      
       Ctrl-Shift-A
      
      
       Command-Shift-A
      
     
     
      
       Jump between a test file and its tested file.
      
      
       Ctrl-Shift-T
      
      
       Command-Shift-T
      
     
     
      
       Select the next enclosing block (hit repeatedly to select the surrounding statement, if block, method block, class, etc.)
      
      
       Alt-Shift-. (dot)
      
      
       Ctrl-Shift-.
      
     
     
      
       Opposite of Ctrl-Shift-. in that it selects progressively smaller blocks around the caret.
      
      
       Alt-Shift-, (comma)
      
      
       Ctrl-Shift-,
      
     
     
      
       Rename the symbol under the caret
      
      
       Ctrl-R
      
      
       Ctrl-R for 6.5, Command-R for earlier releases
      
     
     
      
       Go to the declaration of the symbol under the caret
      
      
       Ctrl-B
      
      
       Command-B
      
     
     
      
       Comment or uncomment (toggle comments) for the selected lines or the line containing the caret
      
      
       Ctrl-/ (slash)
      
      
       Command-/
      
     
     
      
       Reformat the code (selection or full file)
      
      
       Alt-Shift-F
      
      
       Ctrl-Shift-F
      
     
     
      
       Reformat the current comment paragraph (word wrapping the text according to rdoc conventions for bulleted lists, preformatted content, etc)
      
      
       Ctrl-Shift-P
      
      
       Command-Shift-P
      
     
     
      
       Indent or Outdent the selected lines
      
      
       Tab/Shift-Tab
      
      
       Tab/Shift-Tab
      
     
     
      
       Go to line (by line number)
      
      
       Ctrl-G
      
      
       Ctrl-G
      
     
     
      
       Toggle Breakpoint on current line
      
      
       Ctrl-F8
      
      
       Command-F8
      
     
     
      
       Hippie-expand / complete the current word by inserting the next matching word from open buffers. (Hit repeatedly to cycle through matches).
      
      
       Ctrl-K
      
      
       Command-K
      
     
     
      
       Open Type (go to a class in open projects or in the Ruby libraries)
      
      
       Ctrl-O
      
      
       Command-O
      
     
     
      
       Open File by name prefix (not path)
      
      
       Alt-Shift-O
      
      
       Ctrl-Shift-O
      
     
     
      
       Jump to other open documents (in LIFO order). Hold control key and tap the Tab key to see the list; press Tab repeatedly to cycle.
      
      
       Ctrl-Tab
      
      
       Ctrl-Tab
      
     
     
      
       Run the current file. In a Rails project, this will open up the browser on the URL relevant to the file (unless it's a rakefile or a test file.)
      
      
       Shift-F6
      
      
       Shift-F6
      
     
     
      
       Test File (runs the unit test associated with the given file, or if not found the file itself as a test)
      
      
       Ctrl-F6
      
      
       Command-F6
      
     
     
      
       Run the current test (the test method surrounding the editor caret
      
      
       Alt-Shift-F6
      
      
       Option-Shift-F6
      
     
     
      
       Debug the current test (the test method surrounding the editor caret
      
      
       Alt-Shift-F5
      
      
       Option-Shift-F5
      
     
     
      
       Jump to matching parenthesis / brace / bracket, or other matching symbol (such as class, def, if, end, etc.)
      
      
       Ctrl-[[
      
      
       Command-[[
      
     
     
      
       Maximize the current window (typically the editor), temporarily docking all other windows (hover over to expose), press again to un-maximize
      
      
       Shift-Escape
      
      
       Shift-Escape
      
     
     
      
       Open Rails Code Generator
      
      
       Ctrl-Insert
      
      
       Command-I
      
     
     
      
       Select the currently edited file in the project view
      
      
       Ctrl-Shift-1
      
      
       Command-Shift-1
      
     
     
      
       Select the currently edited file in the files view
      
      
       Ctrl-Shift-2
      
      
       Command-Shift-2
      
     
    
    

    
    
    #### Snippets

    
See the
     [RubyCodeTemplates](../RubyCodeTemplates/RubyCodeTemplates.md)
     document for more details.

    
There's a large number of code templates bundled with NetBeans. The following brief list just summarizes a few you might find convenient. To use, type the abbreviation in the editor and then hit Tab. Use the Tab key or Enter to finish each "section" in the template (if there are multiple). Shift-Tab will cycle backwards. The current editing section is shown in a blue highlight.

    
     
      
       Abbreviation
      
      
       Description
      
     
     
      
       :
      
      
       Insert a hash entry of the form :key => "value"
      
     
     
      
       l
      
      
       Insert =>
      
     
     
      
       do
      
      
       Insert a do block with an unused block iterator variable
      
     
     
      
       r
      
      
       In an RHTML file: Insert <%  %>
      
     
     
      
       re
      
      
       In an RHTML file, insert a Ruby Expression:  <%= %>
      
     
     
      
       jc
      
      
       For JRuby, require java and import a class by fully qualified name
      
     
     
      
       ife
      
      
       If-else block
      
     
     
      
       begin
      
      
       Begin-rescue-end block
      
     
    
    

    
    
    #### Other Tips

    - In the "Open Type" dialog (Command-O, Ctrl?-O) you can enter
      
       #
      
      to jump to methods, e.g.
      
       #to_s
      
      . Also, you can use camel-case to jump to classes. For example,
      
       AC::B
      
      will list
      
       ActionController::Base
      
      references.
- If you are doing a lot of Rails development, you may want to bind the Rails code generator action (which appears in the project's context menu) to a keyboard action such as alt-shift-g (or ctrl-shift-g on the Mac). To do that, open the Options, select the Keymaps category, and look for "Generate..." under the "Other" category to bind it. (
      [issue 104379](https://web.archive.org/web/20111026065521/http://www.netbeans.org/issues/show_bug.cgi?id=104379)
      tracks adding a default keybinding for this)
- You can also enable automatic word wrapping in comments by running the IDE with
      
       -J-Druby.autowrap.comments=true
      
      (which you can also add to your
      
       netbeans.conf
      
      or
      
       nbrubyide.conf
      
      file.
- Pressing "#" inside a double quoted string will insert #{ } with the caret in the middle
- Pressing "#" in a string when there is a text selection will surround the text selection with #{ }.
- Similarly, pressing left parenthesis, left bracket, left brace, single quote or double quote when there is a text selection in Ruby code will surround the text selection with

    
```
  the opposite character (e.g. insert right parenthesis, right bracket, ... etc on the opposite end as well.

```

    - Pressing ", + or _ in a comment when there is a selected word will surround the word with the same character (useful for rdoc formatting).
- NetBeans by default will use "camel case navigation" for delete word, next word, previous word etc. caret navigation. By "camel case"

    
```
 I mean that for a WordLikeThis it will jump from the W to the L to the T. And for a word_like_this it will jump from the w to the l to the t.
 You can turn this behavior off (such that it deletes whole words, or jumps across whole words) by running NetBeans with

```

    
```

-J-Dno-ruby-camel-case-style-navigation=true

```

    - See the
      [RubyOptions](../RubyOptions/RubyOptions.md)
      page for additional options you can tweak!

    
    
Note that  is a workaround for the bug where  in an RHTML file inserts the linefeed after a %> marker. --PhlIp

    
    
     Retrieved from "
     [http://wiki.netbeans.org/RubyShortcuts](../RubyShortcuts/RubyShortcuts.md)
     "
