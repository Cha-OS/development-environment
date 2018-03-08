# Multi-cursor

+ [multi cursor in Atom with TypeScript and Angular](https://www.youtube.com/watch?v=PuZMbzvNgTg)

# Settings/Customization

+ https://atom.io/docs/latest/using-atom-basic-customization
+ Soft wrapping
  + https://github.com/atom/atom/issues/7668
  + Single
    + View > Toggle Soft Wrap
  + Global
    + Atom > Open Your Config
      + editor: `softWrap: true`
+ make .gitignore files visible
  + http://blog.lukebennett.com/2015/09/21/show-hidden-files-in-atom-sidebar/
  + https://stackoverflow.com/questions/36253907/dont-ignore-node-modules-in-atom
  + In Atom main settings, uncheck "Exclude VCS ignored Paths"
+ Keyboard (keymap.cson), not working well :(
```json
'body':
  'ctrl-pagedown': 'pane:show-next-recently-used-item'
'body':
  'ctrl-pageup': 'pane:show-previous-recently-used-item'
'body':
  'ctrl-tab': 'pane:show-next-item'
'body':
  'ctrl-shift-tab': 'pane:show-previous-item'
```

# Packages

+ install
  + https://atom.io/docs/latest/using-atom-atom-packages
  + `apm install --check`
+ https://codeforgeek.com/2014/09/5-must-have-packages-atom-editor/
+ Projects
  + http://stackoverflow.com/questions/22835375/create-project-in-atom-editor
+ project-manager
  + https://atom.io/packages/project-manager
  + ALT+CMD+P
+ https://atom.io/packages/file-icons


## Autocompletition

+ https://discuss.atom.io/t/what-can-we-do-to-improve-autocomplete/13001/7
+ https://discuss.atom.io/t/announce-autocomplete-v2-0-0-is-released/14541/15
+ http://stackoverflow.com/questions/30954674/atom-javascript-autocomplete
+ packages
  + https://atom.io/packages/autocomplete-plus
  + http://blog.atom.io/2015/05/15/new-autocomplete.html
  + https://github.com/atom/autocomplete-plus/wiki/Autocomplete-Providers

### Typescript

#### IDE-TypeScript package

+ ide-typescript
+ https://atom.io/packages/ide-typescript
+ This package is currently an **early access release**.
+ You should **also install** the [atom-ide-ui](https://atom.io/packages/atom-ide-ui) package to expose the functionality within Atom
  + atom-ide-ui
+ Features
  - Auto completion
  - Diagnostics (errors & warnings)
  - **Document outline**
  - Find references
  - **Go to definition**
  - Hover
  - Signature help
+ **PROBLEMS**: 
  + If one of imports in a file is not correct (wrong path or error with imports of that import) then all imports in the file are reported as not correct

##### atom-ide-ui

+ atom-ide-ui
+ https://atom.io/packages/atom-ide-ui
+ A collection of Atom UIs to support language services as part of Atom IDE, designed for use with packages built on top of [atom-languageclient](https://github.com/atom/atom-languageclient)
+ NOTE: It will ask you

#### Atom TypeScript

- atom-typescript
- https://atom.io/packages/atom-typescript
- JavaScript developers can now just open a .ts file and start hacking away like they are used to. No grunt no Visual Studio. Just pure coding
- Features
  - **Autocomplete**
  - Live error analysis
  - Type information on hover
  - Compile on save
  - **Project Context Support (`tsconfig.json`)**
  - Project Build Support
  - `package.json` Support
  - **Goto Declaration**
  - **Find References**
  - Block comment and uncomment
  - **Rename refactoring**
  - Common Snippets

#### TypeScript language support in Atom

+ language-typescript
+ https://atom.io/packages/language-typescript
+ Adds syntax highlighting and snippets for TypeScript in Atom

#### Jasmine for Atom

+ atom-jasmine-typescript
+ https://atom.io/packages/atom-jasmine-typescript
+ Easily write Jasmine tests for your project in Atom.

#### Atom TSD

+ atom-tsd
+ https://atom.io/packages/atom-tsd
+ Install and update DefinitelyTyped typescript typings using [TSD](https://github.com/DefinitelyTyped/tsd) with [Atom](https://atom.io/)

#### atom-deepscan

+ atom-deepscan
+ https://atom.io/packages/atom-deepscan
+ Atom package to detect bugs and quality issues in JavaScript, TypeScript and React. Works with [DeepScan](https://deepscan.io/).
  + DeepScan is a cutting-edge JavaScript code inspection tool that helps you to find bugs and quality issues more precisely by data-flow analysis. You can also use it for React because DeepScan delivers [React specific rules](https://deepscan.io/docs/rules/#react)

#### typescript-modules-helper

+ typescript-modules-helper
+ https://atom.io/packages/typescript-modules-helper
+ Adds "import Foo from '../bar'" statements for you
+ Adds "go to declaration" that works with modules declared elsewhere, and fallbacks to atom-typescript go to declaration, just ctrl/cmd click an indexed symbol

#### Atom-Typescript-React-Redux-Snippets

+ atom-typescript-react-redux-snippets
+ https://atom.io/packages/atom-typescript-react-redux-snippets
+ Typescript, React and Redux snippets for Atom (followed ES6 standard)

### Angular

####Angular2 Component Generation Extension for Atom

+ angular2-component-generator
+ https://atom.io/packages/angular2-component-generator
+ Extension automatically creates folder for angular2 component containing :
  - `component.ts`
  - `module.ts`
  - `component.html`
  - `component.scss`

#### atom-angular-2

+ angular-2
+ https://atom.io/packages/angular-2
+ Currently supports angular-cli projects only
+ Features
  + Syntax highlighting for Typescript
  + Autocompletes
    - Typescript
    - Angular
    - Your App classes
  + **Resolves Imports**
  + Snippets

####Angular 2 TypeScript Snippets for Atom

+ angular-2-typescript-snippets
+ https://atom.io/packages/angular-2-typescript-snippets
+ This extension for Atom adds snippets for Angular 2 for TypeScript and HTML
+ It seems that **<u>you need to have</u>** a `tsconfig.json` to get the TypeScript snippets to work.

Type part of a snippet, press `enter`, and the snippet unfolds.

##### TypeScript Snippets

| snippet                                  | explanation                |
| ---------------------------------------- | -------------------------- |
| [ng2-bootstrap](https://atom.io/packages/angular-2-typescript-snippets#ng2-bootstrap) | bootstrap a module         |
| [ng2-module](https://atom.io/packages/angular-2-typescript-snippets#ng2-module) | create a module            |
| [ng2-component](https://atom.io/packages/angular-2-typescript-snippets#ng2-component) | create a component         |
| [ng2-input](https://atom.io/packages/angular-2-typescript-snippets#ng2-input) | create an input property   |
| [ng2-output](https://atom.io/packages/angular-2-typescript-snippets#ng2-output) | create an output event     |
| [ng2-directive](https://atom.io/packages/angular-2-typescript-snippets#ng2-directive) | create a directive         |
| [ng2-pipe](https://atom.io/packages/angular-2-typescript-snippets#ng2-pipe) | create a pipe              |
| [ng2-routes](https://atom.io/packages/angular-2-typescript-snippets#ng2-routes) | setup routes               |
| [ng2-route-path](https://atom.io/packages/angular-2-typescript-snippets#ng2-route-path) | configure single           |
| [ng2-service](https://atom.io/packages/angular-2-typescript-snippets#ng2-service) | create a service           |
| [ng2-subscribe](https://atom.io/packages/angular-2-typescript-snippets#ng2-subscribe) | subscribe to an observable |
| [ng2-rx-map](https://atom.io/packages/angular-2-typescript-snippets#ng2-rx-map) | import map-operator        |

##### HTML Snippets

| snippet                                  |
| ---------------------------------------- |
| [ng2-ngClass](https://atom.io/packages/angular-2-typescript-snippets#ng2-ngclass) |
| [ng2-ngFor](https://atom.io/packages/angular-2-typescript-snippets#ng2-ngfor) |
| [ng2-ngIf](https://atom.io/packages/angular-2-typescript-snippets#ng2-ngif) |
| [ng2-ngModel](https://atom.io/packages/angular-2-typescript-snippets#ng2-ngmodel) |
| [ng2-property](https://atom.io/packages/angular-2-typescript-snippets#ng2-property) |
| [ng2-event](https://atom.io/packages/angular-2-typescript-snippets#ng2-event) |
| [ng2-routerLink](https://atom.io/packages/angular-2-typescript-snippets#ng2-routerlink) |
| [ng2-ngStyle](https://atom.io/packages/angular-2-typescript-snippets#ng2-ngstyle) |
| [ng2-ngSwitch](https://atom.io/packages/angular-2-typescript-snippets#ng2-ngswitch) |

Alternatively, press `Ctrl`+`Space` (Windows, Linux) or `Cmd`+`Space` (OSX) to activate snippets from within the editor.

#### Other snippets

##### angular2-snippets-atom

+ angular2-snippets-atom package
+ https://atom.io/packages/angular2-snippets-atom
+ Angular 2 - Typescript snippets for Atom

##### angular2-snippets

+ Angular 2 Snippets for Atom
+ https://atom.io/packages/angular2-snippets
+ A collection of common Angular 2 snippets for Dart and Typescript

#### nativescript-ng2-atom-snippets

+ NativeScript + Angular 2 Snippets for Atom
+ https://atom.io/packages/nativescript-ng2-atom-snippets
+ Snippets for all NativeScript UI components and some frequently used attributes specifically for use with [nativescript-angular](https://github.com/NativeScript/nativescript-angular)
+ Have used styling from John Papa's course and material - Thanks [@John_Papa](https://twitter.com/John_Papa).
  - ngComponent - Angular 2 new Component
  - ngService - Angular 2 new Service,
  - ngPipe - Angular 2 new Pipe
  - ngImport - Import Statement
  - ngImportComponent - Angular 2 import statement for Component from angular core
  - ngImportRouter - Angular 2 import Router
  - ngImportHttp - Angular 2 Http
  - ngImportRx - Observable and Subject from Rx

#### Angular material

##### autocomplete-angular-material

+ Angular Material Autocomplete Package
+ It is for the old angular.js (1) material, but it seems to be possible to extend it to work with ng2
+ https://atom.io/packages/autocomplete-angular-material
+ [Angular Material](https://material.angularjs.org/#/) tag and attribute autocompletions in Atom. Install [autocomplete-plus](https://github.com/atom-community/autocomplete-plus) before installing this package.
+ This is powered by the list of HTML tags [here](https://raw.githubusercontent.com/chrisgriffith/Angular-Material-Brackets-Extension/master/HtmlTags.json) and HTML attributes [here](https://raw.githubusercontent.com/chrisgriffith/Angular-Material-Brackets-Extension/master/HtmlAttributes.json)
+ You can update the prebuilt list of tags and attributes names and values by running the `update.coffee` file at the root of the repository and then checking in the changed `completions.json` file.

### Express

#### express-complete

+ Express Autocomplete
+ https://atom.io/packages/express-complete
+ Collection of Express snippets for Atom. Contributions encouraged

### SASS

#### Sass/SCSS language support in Atom

+ language-sass
+ https://atom.io/packages/language-sass
+ Adds syntax highlighting and snippets to Sass/SCSS files in Atom

#### Compass Framework Snippets for Atom Editor

+ compass
+ https://atom.io/packages/compass
+ So far, CSS3, Layout and Typography are done [See TODOs](https://atom.io/packages/compass#todo)

### ternjs

+ https://atom.io/packages/atom-ternjs
+ https://github.com/mprinc/atom-ternjs
+ node-express
  + https://github.com/angelozerr/tern-node-express
```sh
cd ~/.atom/packages/atom-ternjs
npm install tern-node-express
```
+ Problems:
  + if node_modules is included it might hang completely auto-complete
  + best is to remove it
+ fixes
  + atom-ternjs-server.js
```js
      this.config.loadEagerly.forEach((pat) => {


        glob.sync(pat, { cwd: this.projectDir }).forEach(function(file) {
            if(file.indexOf("node_modules")<0) files.push(file);
        });
      });
```

```json
{
  "ecmaVersion": 6,
  "libs": [
    "browser",
    "jquery"
  ],
  "loadEagerly": [
    "src/js/**/*.js",
    "src/bower_components/**/*.js"
  ],
  "dontLoad": [
    "wikipedia/**/node_modules/**/*.js",
  ],
  "plugins": {
    "complete_strings": {},
    "node": {},
    "lint": {},
    "angular": {},
    "requirejs": {},
    "modules": {},
    "es_modules": {},
    "doc_comment": {
      "fullDocs": true
    },
    "node-express": {}
  }
}
```

### Text

#### sort-lines

+ sort-lines
+ https://atom.io/packages/sort-lines
+ Sorts your lines in Atom. Never gets tired.
+ **select** lines you want to sort
+ `CMD+SHIFT+P`
  + type: `sort`
  + press ENTER

### Files

####split-diff

+ split-diff
+ https://atom.io/packages/split-diff
+ Diffs text between two split panes. New panes are created if less than two panes exist upon run of the package.
+ ** **Supports diffing recent git changes!** **

#### minimap-split-diff

+ minimap-split-diff
+ https://atom.io/packages/minimap-split-diff
+ A plugin that adds [Split Diff's](https://github.com/mupchrch/split-diff) highlighting to the [Minimap](https://github.com/atom-minimap/minimap) view, making it easier to find differences throughout file versions in Atom.

#### compare-files

+ compare-files
+ https://atom.io/packages/compare-files
+ Compares two files and shows the diff


#### Local History for Atom

+ local-history
+ https://atom.io/packages/local-history
+ Atom package for maintaining a local history of files (history of your changes to the code files).
+ https://discuss.atom.io/t/local-history-of-file-changes/1090/9

### Code Overview

- [Feature Request: Source Code Navigator for classes, methods, variables etc](https://discuss.atom.io/t/feature-request-source-code-navigator-for-classes-methods-variables-etc/11225)

### Symbols view

#### Symbols View package

+ symbols-view
+ https://atom.io/packages/symbols-view
+ Display the list of functions/methods in the editor.
+ Problems with TypeScript:
  + https://github.com/atom/symbols-view/issues/9
  + https://atom.io/packages/symbol-gen

#### symbols-tree-view package

- symbols-tree-view
- https://atom.io/packages/symbols-tree-view
- Symbols Tree View for Atom.io, just like taglist or tagbar for VIM.
- Problems with TypeScript:
  - https://github.com/xndcn/symbols-tree-view/issues/101

### Cursor

- https://discuss.atom.io/t/multiple-selections/755/47
- https://github.com/atom/atom/issues/1365
- https://github.com/atom/atom/issues/6909
- https://github.com/atom/atom/pull/7225
- Packages
  - https://atom.io/packages/cursor-indicator
  - https://atom.io/packages/multi-cursor-plus
  - https://atom.io/packages/cursor-history
  - https://atom.io/packages/last-cursor-position
  - https://atom.io/packages/minimap-cursorline
  - https://atom.io/packages/multi-cursor
    - Creating cursors
      - alt + up = Create cursor above
      - alt + down = Create cursor under
    - Moving the last cursor that has been created
      - ctrl + alt + up = Move the last-created cursor up
      - ctrl + alt + down = Move the last-created cursor down
      - ctrl + alt + left = Move the last-created cursor left
      - ctrl + alt + right = Move the last-created cursor right

### Markdown

+ [Atom.io for Markdown editing](https://blogs.msdn.microsoft.com/silverlining/2015/05/18/atom-io-for-markdown-editing/)
+ https://atom.io/packages/markdown-preview-plus
  + need to disable “markdown-preview”
  + https://atom.io/packages/markdown-preview-plus-opener

#### Markdown-Writer for Atom

+ markdown-writer

+ https://atom.io/packages/markdown-writer

+ Adds tons of features to make [Atom](https://atom.io/) an even better Markdown/AsciiDoc editor!

  Works great with static blogging as well. Try it with [Jekyll](http://jekyllrb.com/), [Octopress](http://octopress.org/), [Hexo](http://hexo.io/) or any of your favorite static blog engines.

#### Markdown Preview Enhanced

+ markdown-preview-enhanced
+ https://atom.io/packages/markdown-preview-enhanced
+ Markdown Preview Enhanced is an extension that provides you with many useful functionalities such as automatic scroll sync, [math typesetting](https://shd101wyy.github.io/markdown-preview-enhanced/#/math), [mermaid](https://shd101wyy.github.io/markdown-preview-enhanced/#/diagrams?id=mermaid), [PlantUML](https://shd101wyy.github.io/markdown-preview-enhanced/#/diagrams?id=plantuml), [pandoc](https://shd101wyy.github.io/markdown-preview-enhanced/#/pandoc), PDF export, [code chunk](https://shd101wyy.github.io/markdown-preview-enhanced/#/code-chunk), [presentation writer](https://rawgit.com/shd101wyy/markdown-preview-enhanced/master/docs/presentation-intro.html), etc. A lot of its ideas are inspired by [Markdown Preview Plus](https://github.com/atom-community/markdown-preview-plus) and [RStudio Markdown](http://rmarkdown.rstudio.com/).

#### Markdown Preview Plus (MPP)

+ markdown-preview-plus
+ https://atom.io/packages/markdown-preview-plus
+ Markdown Preview Plus (MPP) is a fork of [Markdown Preview](https://github.com/atom/markdown-preview) that provides a real-time preview of markdown documents.

#### markdown-scroll-sync Atom editor 

+ markdown-scroll-sync
+ https://atom.io/packages/markdown-scroll-sync
+ Auto-scroll markdown-preview tab to match markdown source

### Preview

+ https://atom.io/packages/atom-html-preview
+ https://atom.io/packages/preview-plus
+ https://atom.io/packages/browser-plus

### Documentation

+ https://github.com/tgandrews/atom-easy-jsdoc


+ printing support
  + https://discuss.atom.io/t/printing-support/760/41
  + https://github.com/postcasio/atom-printer
+ console
  + CMD+ALT+I
+ fixing

```sh
rm /usr/local/bin/atom
ln -s '/Applications/Atom.app/Contents/Resources/app/atom.sh' '/usr/local/bin/atom'
ln -s '/Applications/Atom.app/Contents/Resources/app/apm/node_modules/.bin/apm' '/usr/local/bin/apm'
```

#### Docblockr

+ docblockr
+ https://atom.io/packages/docblockr
+ DocBlockr is a package for [Atom](http://atom.io/) which is designed to make writing documentation faster and easier.
+ Pressing **enter** or **tab** after <u>**/****</u> (or <u>**###***</u> for Coffee-Script) will yield a new line and will close the comment
+ The package currently supports the following languages:
  - **C, C++, Cuda-C++**
  - **CoffeeScript**
  - Groovy
  - Haxe
  - **Java**
  - **JavaScript**
  - ObjC, ObjC++
  - PHP
  - Processing
  - **SASS**
  - **TypeScript**

### Editor

#### Color

+ https://atom.io/packages/an-color-picker
+ https://atom.io/packages/color-picker
+ https://atom.io/packages/webbox-color

####  Misc

+ https://atom.io/packages/indentation-indicator
+ https://atom.io/packages/file-icons
+ https://atom.io/packages/atom-beautify
+ https://atom.io/packages/sort-lines
+ https://atom.io/packages/wordcount

##### Text Pastry

+ text-pastry
+ https://atom.io/packages/text-pastry
+ A package for the [atom.io](https://atom.io/) editor advanced pasting operations.

### Timetracking

#### wakatime

- https://atom.io/packages/wakatime
- Fitbit for programmers. Get automated metrics and insights about your programming
- https://wakatime.com/dashboard

#### punchclock

+ https://atom.io/packages/punchclock
+ Punchclock allows you to track time spent on projects, and provides (or rather will provide) ways to view the data in different ways as well as the ability to export and integrate this data with external endpoints.
+ Punchclock tracks time on projects, forked from Timekeeper

#### timekeeper

+ https://atom.io/packages/timekeeper
+ Timekeeper handles all of your time tracking needs from within Atom.
+ Timekeeper allows you to track time spent on projects, and provides (or rather will provide) ways to view the data in different ways as well as the ability to export and integrate this data with external endpoints.

#### break-time

+ https://atom.io/packages/break-time
+ Reminds/Forces you to take a break

#### atometer

+ A package for Atom to measure how many keys you type each day.
+ https://atom.io/packages/atometer

#### editor-stats

+ View a graph of your mouse and keyboard activity for the last 6 hours
+ https://atom.io/packages/editor-stats




Timekeeper

### Git

+ Core
  + [Git Integration](http://blog.atom.io/2014/03/13/git-integration.html)

#### Git-Plus package

+ git-plus
+ https://atom.io/packages/git-plus
+ vim-fugitive like package for atom. make commits and other git things without the terminal
+ Cmd-Shift-H


#### git-blame

+ git-blame
+ https://atom.io/packages/git-blame
+ Toggle git-blame annotations in Atom


#### Git History Package for Atom

+ git-history
+ https://atom.io/packages/git-history
+ View previous versions of any file known to git. By default, the plugin will now show a diff with the selected version. This can be disabled in the settings.
+ crashing on our OSX machine

#### git-time-machine package

+ git-time-machine
+ https://atom.io/packages/git-time-machine
+ git-time-machine is a package for [Atom](https://atom.io/) that allows you to travel back in time! It shows visual plot of commits to the current file over time and you can click on it on the timeplot or hover over the plot and see all of the commits for a time range.

#### Git Log Package

+ git-log
+ https://atom.io/packages/git-log
+ Git-log is a package for [Atom](http://atom.io/) that creates a graph of your git commits and shows commit related information for you on the editor.

#### Tree View Git Status package

+ tree-view-git-status
+ https://atom.io/packages/tree-view-git-status
+ Show the Git repository status in the Atom tree-view.

#### Other

+ https://atom.io/packages/better-git-blame
+ https://atom.io/packages/git-status
+ https://atom.io/packages/git-diff-details
+ Discussion
  + [Displaying code changes from last commit in IDE](https://discuss.atom.io/t/displaying-code-changes-from-last-commit-in-ide/26890)



# Development examples

## General

`cd /Users/sasha/.atom/packages`

## CoffeeScript

+ https://atom.io/packages/colorful-cursor
+ https://github.com/tanukiti1987/colorful-cursor

## JS

+ https://atom.io/packages/minimap-cursorline
+ https://github.com/atom-minimap/minimap-cursorline

## Debugging

+ https://discuss.atom.io/t/how-to-debug-a-new-package/3290
+ https://github.com/tststs/atom-ternjs/issues/175
+ https://atom.io/docs/latest/hacking-atom-debugging

## Workflow

+ http://stackoverflow.com/questions/32429076/develop-and-debug-atom-package



# Problems

## TypeScript config

### Grave Accent

http://unicode-table.com/en/#0060
https://github.com/atom/language-html/issues/59
https://github.com/atom/atom/issues/6940





# Interaction

## Search

### through new line

- https://stackoverflow.com/questions/41497325/multiline-search-and-replace-in-atom-editor
  - `(.|\r?\n)*?`
- https://github.com/atom/find-and-replace/issues/303