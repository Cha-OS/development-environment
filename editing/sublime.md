# Install

## Plugins

+ Once: install "**Package Controll**"
  + Go to Package Control’s [installation page](https://packagecontrol.io/installation) and copy the Sublime Text 3 python code.
  + In Sublime Text 3, press "**ctrl+`**"  or go to *View*, *Show Console*. 
  + Paste in the python code and hit *Enter*
+ Every time: **install package**
  + Press ***CMD+SHIFT+P*** to bring up the [Command Palette](https://packagecontrol.io/docs/usage).
  + Type in “Package Control” and select *Package Control: **Install Package***.
  + Type in and then select the **package name** you want when you get to the following window
+ **Uninstall package**
  + Sublime Text > Preferences > Package controll
    + type: Remove Package
    + choose package
+ Package Settings
  + Sublime Text > Preferences > Package Settings > &lt;**choose your package & follow sub settings**" >

# Plugins

## Files Diff and Compare

+ [SO - Comparing the contents of two files in Sublime Text](https://stackoverflow.com/questions/25874018/comparing-the-contents-of-two-files-in-sublime-text)


## Packages

### Compare Side-By-Side

+ https://packagecontrol.io/packages/Compare%20Side-By-Side
+ no way to accept and merge difference

### Sublimerge Pro

+ https://packagecontrol.io/packages/Sublimerge%20Pro
+ https://www.sublimerge.com/
+ https://www.sublimerge.com/sm3/

### Sublimerge 3

+ config
  + https://www.sublimerge.com/sm3/docs/configuration.html
+ info
  + [Sublimerge: 'Merge: left to right' grayed out, but 'Merge all: left to right' available](https://stackoverflow.com/questions/23027264/sublimerge-merge-left-to-right-grayed-out-but-merge-all-left-to-right-av)
+ shourtcuts
  + CTRL+ALT+D

    + opens menu


      [alt]+[down]                          - select next change
          [alt]+[up]                            - select previous change
        * [alt]+[left]                          - copy selected change (or active line) to left from right
        * [alt]+[right]                         - copy selected change (or active line) to right from left
          [alt]+[shift]+[left]                  - copy all changes to left from right
          [alt]+[shift]+[right]                 - copy all changes to right from left
          
          Common:
          
          [f3]                                  - swap panels
          [f4]                                  - show changes navigator
          [f5]                                  - recompare buffers
        
        * - if change is selected the command will copy its whole contents, otherwise will copy only the focused line

### Sublimerge Pro

+ **Earlier** version than Sublimerge 3

### FileDiffs

+ https://packagecontrol.io/packages/FileDiffs
+ Shows diffs between the current file, or selection(s) in the current file, and clipboard, another file, or unsaved changes. With contributions from Sebastian Pape (spape) and Jiri Urban (jiriurban)
+ no way to accept and merge difference




# Interaction

## Search

### through new line

+ modifiers
  + https://stackoverflow.com/questions/26124314/sublime-text-regex-not-detecting-multiline-tags
    + `(?s)`
    + `(?s)\[sometag\](.*?)\[\/sometag\]`
+ https://gist.github.com/Claymm/5677097
  + `((?!</head>).|\n)`
  + `<head>((?!</head>).|\n)+</head>`
+ ​