# TimThumb

TimThumb is a simple, flexible, PHP script that resizes images.

My intention is to have an updated repo which works with composer on all my known LAMP server configurations because the only timthumb repo on packagist is out of date (2.8.11) which doesn't works for me.


## Installing with composer

To use this repo on you composer proyect, simply add an *vcs* repository pointing to this GitHub repo and require it on your composer.json file:

```json
{
	"repositories": [
		{
			"type": "vcs",
			"url": "https://github.com/GabrielGil/TimThumb"
		}
	],
	"require": {
		"gabrielgil/timthumb": "2.*"
	}
}
```

### A better way to use TimThumb

I think it's a good way of using timthumb, to store it on a non-public folder (Like the whole composer *vendor* folder) and then create your **own** resizer endpoint. If you use it with composer (as this repo is intended to), hide your vendor folder (Just an advice).

How you create your own app structure depends on you, or on your team. If your desired resize endpoint points to a specific file, you can use this code there.

```php
	
/* Redefine your with own defaults here.
 * This are just examples, no one is required. */

// Set the time the cache is cleaned (Since the image generation) to one month (2592000/60/60/24=30)
define ('FILE_CACHE_MAX_FILE_AGE', 2592000);
// Use the default system cache dir so your project's folder stays clean.
define ('FILE_CACHE_DIRECTORY', sys_get_temp_dir());
// Quality set to 100%
define ('DEFAULT_Q', 100);

// Start timthumb.
timthumb::start();

```

After this is set up, you can use all the parameters shown in the [official documentation](http://binarymoon.co.uk/projects/timthumb).

## Documentation

You can also check the original documentation at [binarymoon.uk](http://binarymoon.co.uk/projects/timthumb)