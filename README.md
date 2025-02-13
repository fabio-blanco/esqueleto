Esqueleto
========

Hi. I'm a WordPress starter theme called `Esqueleto`. I'm a theme meant for hacking so don't use me as a Parent Theme. 
Instead try turning me into the next, most awesome, WordPress theme out there. That's what I'm here for.


My ultra-minimal CSS might make me look like theme tartare but that means less stuff to get in your way when you're 
designing your awesome theme. Here are some of the other more interesting things you'll find here:

* A modern workflow with a pre-made command-line interface to turn your project into a more pleasant experience.
* A just right amount of lean, well-commented, modern, HTML5 templates.
* A custom header implementation in `inc/custom-header.php`. Just add the code snippet found in the comments of `inc/custom-header.php` to your `header.php` template.
* Custom template tags in `inc/template-tags.php` that keep your templates clean and neat and prevent code duplication.
* Some small tweaks in `inc/template-functions.php` that can improve your theming experience.
* A script at `js/navigation.js` that makes your menu a toggled dropdown on small screens (like your phone), ready for CSS artistry. It's enqueued in `functions.php`.
* 2 sample layouts in `sass/layouts/` made using CSS Grid for a sidebar on either side of your content. Just uncomment the layout of your choice in `sass/style.scss`.
Note: `.no-sidebar` styles are automatically loaded.
* Smartly organized starter CSS in `style.css` that will help you to quickly get your design off the ground.
* Full support for `WooCommerce plugin` integration with hooks in `inc/woocommerce.php`, styling override woocommerce.css with product gallery features (zoom, swipe, lightbox) enabled.
* Licensed under GPLv2 or later. :) Use it to make something cool.

## Important note

**With the new full site editing feature that will be bundled with WordPress 5.9 release, you should probably
use a Block Theme (e.g. 
[Gutenberg Starter Theme Blocks](https://github.com/WordPress/theme-experiments/tree/master/gutenberg-starter-theme-blocks), 
[Varia](https://github.com/Automattic/themes/tree/trunk/varia) and others), you can also learn about [block themes
development](https://developer.wordpress.org/block-editor/how-to-guides/themes/block-theme-overview/) 
(take a look at [Theme Experiments](https://github.com/WordPress/theme-experiments)). Esqueleto is a regular theme designed 
to be used by power users and developers who do have the need to create themes by directly working with php, javascript, 
sass, css, node scripts and other advanced tools.** 

Installation
---------------

### Requirements

`Esqueleto` requires the following dependencies:

- [Node.js](https://nodejs.org/) (It is recommended to use [nvm](https://github.com/nvm-sh/nvm) to manage node and npm 
versions)
- [Composer](https://getcomposer.org/)

### Quick Start

Clone the repository to a directory with your desired theme name (like, say, `encarnado`):
```shell
$ git clone --single-branch https://github.com/fabio-blanco/esqueleto.git encarnado
```

**Note:** You probably want to do this from inside a local WordPress theme folder (e.g: `/path/to/wordpress/wp-content/themes`)

Enter the new theme directory:

```shell
$ cd encarnado
```

To start using all the tools that come with `Esqueleto`  you need to install the necessary Node.js and Composer 
dependencies :

```sh
$ composer install
$ npm install
```

Just run the startup script from inside the theme project directory:

```sh
$ npm run startup
```

In order to generate the updated pot translation template, compile the css and generate the pot file:

```sh
$ npm run compile:css
$ composer make-pot
```

If necessary, you can adjust the css header by changing the sass file `_theme-header.scss` and recompiling the css
(See the Available CLI commands section below).

Then, update the links in `footer.php` with your own information. Next, update or delete this readme.

Now just run the watch script and start working on your theme.

```sh
$ npm run watch
```

### Manual Quick Start

This manual quick start is meant for he who doesn't want to run the startup script.
Clone or download this repository, change its name to something else (like, say, `megatherium-is-awesome`), and then you'll 
need to do a six-step find and replace on the name in all the templates.

1. Search for `'esqueleto'` (inside single quotations) to capture the text domain and replace with: `'megatherium-is-awesome'`.
2. Search for `esqueleto_` to capture all the functions names and replace with: `megatherium_is_awesome_`.
3. Search for `Text Domain: esqueleto` in `style.css` and replace with: `Text Domain: megatherium-is-awesome`.
4. Search for <code>&nbsp;esqueleto</code> (with a space before it) to capture DocBlocks and replace with: <code>&nbsp;Megatherium_is_Awesome</code>.
5. Search for `esqueleto-` to capture prefixed handles and replace with: `megatherium-is-awesome-`.
6. Search for `ESQUELETO_` (in uppercase) to capture constants and replace with: `MEGATHERIUM_IS_AWESOME_`.

Then, update the stylesheet header in `style.css`, the links in `footer.php` with your own information and rename 
`esqueleto.pot` from `languages` folder to use the theme's slug. Next, update or delete this readme.

#### Setup

To start using all the tools that come with `Esqueleto`  you need to install the necessary Node.js and Composer dependencies :

```sh
$ composer install
$ npm install
```

### Available CLI commands

`Esqueleto` comes packed with CLI commands tailored for WordPress theme development :

- `composer lint:wpcs` : checks all PHP files against [PHP Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/php/).
- `composer lint:php` : checks all PHP files for syntax errors.
- `composer make-pot` : generates a .pot file in the `languages/` directory.
- `npm run compile:css` : compiles SASS files to css.
- `npm run compile:rtl` : generates an RTL stylesheet.
- `npm run watch` : watches all SASS files and recompiles them to css when they change.
- `npm run lint:scss` : checks all SASS files against [CSS Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/css/).
- `npm run lint:js` : checks all JavaScript files against [JavaScript Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/javascript/).
- `npm run bundle` : generates a .zip archive for distribution, excluding development and system files.
- `npm run startup` : prepare the theme to use the chosen name.

Now you're ready to go! The next step is easy to say, but harder to do: make an awesome WordPress theme. :)

Good luck!

### Esqueleto origin

My name is [Fábio](https://github.com/fabio-blanco) and this is a modified version from the original 
[underscores](https://github.com/Automattic/_s) that I've made for my personal use. Since I've discovered
that the original Underscores project was [no longer been maintained](https://github.com/Automattic/_s/issues/1511#issuecomment-987450782) 
I decided to polish things a little, update the dependencies and release it with a new name.
Feel free to use it too if it fits your needs.
