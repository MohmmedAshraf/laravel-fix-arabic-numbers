# Laravel - Auto Fix Arabic Numbers

This package allows you to auto fix Arabic numbers form inputs.

## Installation

This package can be used in Laravel 5.4 and up.

You can install the package via composer:

``` bash
composer require outhebox/laravel-fix-arabic-numbers
```

## Usage

### Laravel
In `app/Http/Kernel.php`, register the middleware:

```php
protected $middleware = [
    //...
    \OutheBox\FixArabicNumbers\Http\Middleware\FixArabicNumbers::class,
]
```

### Lumen

In `bootstrap/app.php`, register the middleware:

```php
$app->middleware([
    \OutheBox\FixArabicNumbers\Http\Middleware\FixArabicNumbers::class,
]);
```

## Extending

If you need to EXTEND the existing `FixArabicNumbers` middleware note that:

- Your `FixArabicNumbers` middleware needs to extend the `OutheBox\FixArabicNumbers\Http\Middleware\FixArabicNumbers` middleware
- Add the fields you want to except form the middle ware to
```php
    /**
     * The attributes that should not be trimmed.
     *
     * @var array
     */
    protected $except = [
        //
    ];
```

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
