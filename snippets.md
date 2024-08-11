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

`functions.php`
```
<?php

<?php

// to call wordpres hooks.
add_action('wp_enqueue_scripts', 'add_css');
function add_css()
{
    wp_enqueue_style(
        'bootstrap-css',
        get_parent_theme_file_uri('/assets/css/bootstrap.min.css'),
        [],
        '1.0',
        'all'
    );
}


// to call wordpres hooks.
add_action('wp_enqueue_scripts', 'add_javascript');

function add_javascript()
{
    wp_enqueue_style(
        'bootstrap-js',
        get_parent_theme_file_uri('/assets/js/bootstrap.bundle.min.js'),
        [],
        '1.0',
        'all'
    );
}
```

`header.php`
```
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8"/>
    <meta content="width=device-width, initial-scale=1.0" name="viewport"/>
    <title>Training</title>
    <?php wp_head(); ?>
</head>

````


`index.php`
```
<?php get_header(); ?>

<body class="bg-body-tertiary">

<div class="container">
    <div class="row bg-body">
        <header class="border-bottom lh-1 py-3">
            <div class="row flex-nowrap justify-content-center align-items-center">
                <div class="col-4 text-center">
                    <a class="blog-header-logo text-body-emphasis text-decoration-none" href="<?php home_url(); ?>">
                        Training
                    </a>
                </div>
            </div>
        </header>
    </div>

    <div class="row bg-body">
        <div class="nav-scroller py-1 mb-3 border-bottom">
            <nav class="nav nav-underline justify-content-start">
                <a class="nav-item nav-link link-body-emphasis active" href="index.html">Home</a>
                <a class="nav-item nav-link link-body-emphasis" href="contact.html">Contact</a>
            </nav>
        </div>
    </div>

    <div class="row bg-body-secondary">
        <div class="p-4 mb-4 text-body-emphasis">
            <h1 class="display-4 fst-italic">
                "Neque porro quisquam est qui dolorem ipsum quia dolor sit amet,
                consectetur, adipisci velit..."
            </h1>
            <p class="h6">What is Lorem Ipsum?</p>
            <p class="lead my-3">
                Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the
                industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type
                and scrambled it to make a type specimen book. It has survived not only five centuries, but also the
                leap into electronic typesetting, remaining essentially unchanged. It was popularized in the 1960s
                with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop
                publishing software like Aldus PageMaker including versions of Lorem Ipsum.
            </p>
        </div>
    </div>


    <div class="row bg-body-secondary">

        <div class="col-6">
            <div class="container">
                <div class="row g-0 border rounded mb-4 shadow-sm bg-body">
                    <div class="col-8 p-4">
                        <strong class="d-inline-block mb-2 text-success-emphasis">Design</strong>
                        <h3 class="mb-0">Lorem Ipsum</h3>
                        <div class="mb-1 text-body-secondary">Aug 11</div>
                        <p class="mb-auto">
                            Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci
                            velit...
                        </p>
                        <a class="text-decoration-none gap-1 " href="blog.html">
                            Continue reading
                        </a>
                    </div>
                    <div class="col-4 p-4  border-start">
                        <img alt="small pug" class="img-fluid w-100" src="small.jpg"/>
                    </div>
                </div>
            </div>

        </div>


        <div class="col-6">

            <div class="row g-0 border rounded mb-4 shadow-sm bg-body">
                <div class="col-8 p-4">
                    <strong class="d-inline-block mb-2 text-success-emphasis">Design</strong>
                    <h3 class="mb-0">Lorem Ipsum</h3>
                    <div class="mb-1 text-body-secondary">Aug 11</div>
                    <p class="mb-auto">
                        Neque porro quisquam est qui dolorem ipsum quia dolor sit amet, consectetur, adipisci
                        velit...
                    </p>
                    <a class="text-decoration-none gap-1 " href="blog.html">
                        Continue reading
                    </a>
                </div>
                <div class="col-4 p-4  border-start">
                    <img alt="small pug" class="img-fluid w-100 " src="small.jpg"/>
                </div>
            </div>
        </div>

    </div>

</div>

<footer class="py-5 text-center text-body-secondary bg-body-tertiary">
    <p>Blog template built for Wordpress theme development training.</p>
    <p class="mb-0">&copy; Sabhriti 2024</p>
</footer>

<?php get_footer(); ?>
```









