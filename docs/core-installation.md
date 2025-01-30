# GetTix Core - Installation

## Composer Require Package

```bash
composer require gandamedia/gettix-core
```

> **TIP**
> 
> You may need to update your app's composer.json to set "minimum-stability": "dev",

## Install the Package
To install all the necessary files and migrations, run the following command:
```bash
php artisan gettix-core:install
```


## Add the GetTixOwner Trait
Brands and Events should be owned by models such as a Team (or User). To setup the relationship, add the `GetTixOwner` trait to the model.

```php
use GetTix\Traits\GetTixOwner;
use GetTix\GetTixOwner as GetTixOwnerInterface;
// ...

class Team implements GetTixOwnerInterface
{
    use GetTixOwner;
    // ...
}
```

## Add the GetTixUser Trait
The User model requires certain relationships to be defined. Add the `GetTixUser` trait to the User model, or any other model that represents a user.

```php
use GetTix\Traits\GetTixUser;
use GetTix\GetTixUser as GetTixUserInterface;
// ...

class User extends Authenticatable implements GetTixUserInterface
{
    use GetTixUser;
    // ...
}
```

## Publish Configuration
Before running the installer command, you should publish the configuration file.

```bash
php artisan vendor:publish --tag="gettix-core"
```
