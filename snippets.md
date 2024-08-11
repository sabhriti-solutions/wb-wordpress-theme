vs code download: [vscode download](https://code.visualstudio.com/download)

COntent of `style.css`
```
/*
Theme Name: Training Theme
Author: Your name
Author URI: http://www.hostinger.com/tutorials
Description: My first responsive HTML5 theme
Version: 1.0
License: GNU General Public License v3 or later
License URI: http://www.gnu.org/licenses/gpl-3.0.html
*/

```
content of `index.php`
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Trainign theme</title>
</head>
<body>
Hello World
</body>
</html>
```

Link to index.html file: [`index.html`](https://github.com/sabhriti-solutions/wb-wordpress-theme/blob/initial/index.html)

link to bootstrap [css](https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css) 

link to bootstrap [js](https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js)

`function.php`
```
<?php

function add_css()
{
    wp_enqueue_style('bootstrap-css', get_template_directory(). '/assets/css/bootstrap.min.css');
}

// to call wordpres hooks.
add_action('wp_enqueue_style', 'add_css');


function add_javascript()
{
    wp_enqueue_style('bootstrap-js', get_template_directory(). 'assets/js/bootstrap.bundle.min.js');
}

// to call wordpres hooks.
add_action('wp_enqueue_scripts', 'add_javascript');

```




