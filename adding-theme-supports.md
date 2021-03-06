---
extends: docs
title: "Adding theme supports"
group: "Basics"
subgroup: "Setup"
prev: theme-filters
next: handling-translations
order: 3
---

## Configuration

Theme supports have to be registered inside `app/Setup/supports.php` file on `after_setup_theme` action hook. Most common supports are already enabled. However, feel free to add or remove entries there.

> Take a look at [Codex](//developer.wordpress.org/reference/functions/add_theme_support/#more-information) for all available support options.

Simply call `add_theme_support()` function with choosen option inside hooked function.

```php
namespace Tonik\Theme\App\Setup;

use function Tonik\Theme\App\config;

function add_theme_supports()
{
  add_theme_support('post-thumbnails');
}
add_action('after_setup_theme', 'Tonik\Theme\App\Setup\add_theme_supports');
```
