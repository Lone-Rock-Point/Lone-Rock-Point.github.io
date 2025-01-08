---
layout: page
title: Code
permalink: /code/
---

## WordPress
We build web-based solutions using WordPress as a CMS. We avoid using headless setups whenever possible, as they add a layer of complexity, code libraries, and additional requirements that are a barrier to development.

### WordPress Themes
All WordPress sites require a theme to load. The focus of the theme is to handle appearance, design, and layout, while abstracting the required functionality into dedicated plugins. When appropriate, we use our in-house [CivicPress Theme](https://civicpress.us/) as a starting point, as it complies with the requirements listed in the [Integrated Digital Experience Act and OMB M-23-22](https://digital.gov/resources/delivering-digital-first-public-experience/).

### WordPress Plugins
Plugins are intended to provide the required functionality for a project. The goal is to isolate the requirements as much as possible and build dedicated plugins to handle them, avoiding large "monolithic" plugins.

#### Code Structure
Plugins must be in a folder - single file plugins are not allowed. The folder should be named for the plugin (capitalization matters). The main file should be named the same as the folder. For example, if you are working on a plugin called `client-function`, the folder should be `client-function` and the main file should be `client-function.php`.

_An exception to the single file plugin rule is if the plugin is a mu-plugin. In that case, the file should be named the same as the plugin and the file should be in the `mu-plugins` folder._


#### Folder Structure
The plugin should have the following structure unless there is a specific need otherwise:

```
client-function/
    index.php
    client-function.php
    assets/
        css/
        js/
        images/
    includes/
```

#### Namespaces
When working in plugins you must use namespaces. The namespace should be the same as the plugin name. For example, if you are working in the `client-function` plugin, the namespace should be `ClientFunction`.

That means the top of your file should look like this:

```php
<?php

/**
 * Plugin Name: Client Function
 * Description: A bespoke plugin to handle client functionality
 * Version:     0.0.1
 * Author:      Lone Rock Point
 * Author URI:  https://lonerockpoint.com/
 * Text Domain: client-function
 * Domain Path: /languages
 * License:     MIT
 * License URI: https://opensource.org/licenses/MIT
 */

namespace ClientFunction;
```

#### Third Party Plugins
Some situations require the use of open-source plugins developed by a third party. Some examples would include form building, managing SEO settings, or user-provided redirects. These plugins are only used on an as-needed basis and are vetted for security and reliability before use.

## PHP
### Coding Standards
When possible, use the [WordPress Coding Standards](https://github.com/WordPress/WordPress-Coding-Standards) in 
[PHP_Codesniffer](https://github.com/squizlabs/PHP_CodeSniffer) to format your code. We use only modern versions of PHP (8.2 and above) and all code is developed to avoid deprecated functions.


## Javascript
WordPress relies heavily on Javascript in the admin experience, both in the standard admin screens and in the block editor. WordPress provides many internal APIs to use and extend this functionality. Refer to the [Block Editor Handbook](https://developer.wordpress.org/block-editor/) for more information regarding how React is used in the larger WordPress environment.


## CSS
All CSS is written using SCSS files and compiled. Both the theme and plugins often contain dedicated CSS for the functionality they provide, and are intended to only be loaded when required. Most government sites are built on top of the [US Web Design System (USWDS)](https://designsystem.digital.gov/) for accessibility and consistency purposes.


## HTML
We strive to build clean and readable HTML when used. We use blocks and template tags to abstract layout pieces to allow them to be shared throughout the site to keep fragmentation at a minimum.

## Accessibility
Accessibility (a11y) is a requirement for all government sites, and all best practices are adhered to.