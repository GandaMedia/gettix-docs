# GetTix Core

Core is the engine of the GetTix system. It runs as a package within Laravel and provides the core functionality of the system.


## Requirements
- PHP 8.3 or higher
- Laravel 11.0
- MySql 8.0+ higher / PostgreSQL 9.2+
- exif PHP extension (on most systems it will be installed by default)
- intl PHP extension (on most systems it will be installed by default)
- bcmath PHP extension (on most systems it will be installed by default)
- GD PHP extension (used for image manipulation)

## Packages
We use various open source packages to provide the functionality of GetTix. During the installation process we may add migrations, config files or views. Here are some of the packages we use that you may want to alter the configuration of, especially if you are using them in your own project:

### Laravel Auditing
We use the Laravel Auditing package to track changes to models.  

[You can find the documentation for this package here](https://laravel-auditing.com/guide/introduction.html).

### Spatie Media Library
We use the Spatie Media Library package to manage media files within the core. You may wish to alter the configuration of this package to customise your file storage locations.

[You can find the documentation for this package here](https://spatie.be/docs/laravel-medialibrary/v11/introduction).
