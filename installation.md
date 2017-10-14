# Installation

Install via composer; in console: 
```bash
composer require reliqarts/doc-weaver
``` 
or require in *composer.json*:
```javascript
{
    "require": {
        "reliqarts/doc-weaver": "^1.0"
    }
}
```
then run `composer update` in your terminal to pull it in.

Once this has finished, you will need to add the service provider to the providers array in your app.php config as follows:
*(n.b. This package supports Laravel's package auto-discovery; if you are using Laravel 5.5 or above you can skip this step.)*

```php
ReliQArts\DocWeaver\DocWeaverServiceProvider::class,
```

Finally, publish package resources and configuration:

```bash
php artisan vendor:publish --provider="ReliQArts\DocWeaver\DocWeaverServiceProvider"
``` 

You may opt to publish only configuration by using the `doc-weaver:config` tag:

```bash
php artisan vendor:publish --provider="ReliQArts\DocWeaver\DocWeaverServiceProvider" --tag="doc-weaver:config"
``` 