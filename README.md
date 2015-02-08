# fileMenu
A jQuery plugin to create a file dropdown menu like most OS windows

### Dependencies

fileMenu depends on this to work.

- [jQuery](http://www.jquery.com)

### Soft Dependencies

These css libs are not required for fileMenu to work. They just add a nice look to the menu. The example makes use of these libs.

- [normalize.css](https://github.com/necolas/normalize.css/)
- [FontAwesome](http://fortawesome.github.io/Font-Awesome/)


### Usage

Make sure the filMenu js and css files are loaded. Create a menu using an unordered list. Then call `fileMenu()` on it.

**HTML**
```
<ul id="menu">
    <li>
        File
        <ul>
            <li><i class="fa fa-fw fa-file"></i> Open<kbd>Ctrl+N</kbd></li>
            <li class="disabled"><i class="fa fa-fw fa-folder-open"></i> Open<kbd>Ctrl+O</kbd></li>
            <li class="sub">
                <i class="fa fa-fw"></i> Open Recent...
                <ul>
                    <li><i class="fa fa-fw fa-file"></i> File A</li>
                    <li><i class="fa fa-fw fa-file"></i> File B</li>
                    <li><i class="fa fa-fw fa-file"></i> File C</li>
                </ul>
            </li>
            <li class="divider"></li>
            <li><i class="fa fa-fw"></i> Quit<kbd>Ctrl+Q</kbd></li>
        </ul>
    </li>
    <li>
        Help
        <ul>
            <li class="toggle"><i class="fa fa-fw"></i> Toggle me</li>
            <li><i class="fa fa-fw fa-question-circle"></i> About<kbd>F1</kbd></li>
        </ul>
    </li>
</ul>
```

**JS**
```
$(document).ready(function() {
    $('#menu').fileMenu();
});
```

### Options

fileMenu accepts a javascript object as its first argument.

**slideSpeed** (`int`)
the slide speed of the menu in ms. Default is 100


### Features

- ** Disabled state **
  
  Just add the class `disabled` to a li to disable it.

- ** Keyboard shortcut class **

    To style a nice keyboard shortcut just use the `<kbd>` tag in the `<li>`

- ** Toggle items **

    Make a menu item toggable by adding the `toggle` class to the li. When toggled on the li has the class `active`.

- ** AMD compatible **

    fileMenu works out of the box with AMD compatible loaders like requireJs. 