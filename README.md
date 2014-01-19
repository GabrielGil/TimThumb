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

### Good way to use `timthumb.php`

#### Pending stuff

## Documentation

You can also check the original documentation at [binarymoon.uk](http://binarymoon.co.uk/projects/timthumb)