---
layout: page
title: Code
permalink: /code/
---

## PHP
### Coding Standards
When possible, use the [WordPress Coding Standards](https://github.com/WordPress/WordPress-Coding-Standards) in 
[PHP_Codesniffer](https://github.com/squizlabs/PHP_CodeSniffer) to format your code.

### WordPress Plugin Structure
Plugins must be in a folder - single file plugins are not allowed. The folder should be named for the plugin (capitalization matters). The main file should be named the same as the folder. For example, if you are working on a plugin called `nasa-history`, the folder should be `nasa-history` and the main file should be `nasa-history.php`.

_An exception to the single file plugin rule is if the plugin is a mu-plugin. In that case, the file should be named the same as the plugin and the file should be in the `mu-plugins` folder._

### Plugin Structure
The plugin should have the following structure unless there is a darn good reason not to:

```
plugin/
    plugin.php
    assets/
        css/
        js/
        images/
    includes/
```

### Namespaces
When working in plugins you must use namespaces. The namespace should be the same as the plugin name. For example, if you are working in the `nasa-history` plugin, the namespace should be `NasaHistory`.

That means the top of your file should look like this:

```php
<?php

/**
 * Plugin Name: Nasa History
 * Description: A plugin to display NASA history
 * Version:     0.0.1
 * Author:      Lone Rock Point
 * Author URI:  https://lonerockpoint.com/
 * Text Domain: nasa-hds
 * Domain Path: /languages
 * License:     MIT
 * License URI: https://opensource.org/licenses/MIT
 */

namespace NasaHistory;
```



## Javascript

## CSS

## HTML
