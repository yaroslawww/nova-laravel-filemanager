# Laravel nova file selector form laravel filemanager

[![Packagist License](https://img.shields.io/packagist/l/yaroslawww/nova-laravel-filemanager?color=%234dc71f)](https://github.com/yaroslawww/nova-laravel-filemanager/blob/master/LICENSE.md)
[![Packagist Version](https://img.shields.io/packagist/v/yaroslawww/nova-laravel-filemanager)](https://packagist.org/packages/yaroslawww/nova-laravel-filemanager)
[![Total Downloads](https://img.shields.io/packagist/dt/yaroslawww/nova-laravel-filemanager)](https://packagist.org/packages/yaroslawww/nova-laravel-filemanager)
[![Build Status](https://scrutinizer-ci.com/g/yaroslawww/nova-laravel-filemanager/badges/build.png?b=master)](https://scrutinizer-ci.com/g/yaroslawww/nova-laravel-filemanager/build-status/master)
[![Code Coverage](https://scrutinizer-ci.com/g/yaroslawww/nova-laravel-filemanager/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/yaroslawww/nova-laravel-filemanager/?branch=master)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/yaroslawww/nova-laravel-filemanager/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/yaroslawww/nova-laravel-filemanager/?branch=master)

Simple package adds the ability to select an image from [UniSharp/laravel-filemanager](https://github.com/UniSharp/laravel-filemanager)

| Nova | Package |
|------|---------|
| V1   | V1      |
| V4   | V2      |

## Usage

```injectablephp
NLFMImage::make( 'Image', 'image' );
NLFMImage::make( 'Image', 'image' )
    ->filemanagerPath('/custom-link/files');
```

You can specify filemanagerPath in the main laravel-filemanager config file by adding the **filemanager_path** key
```
'filemanager_path' => '/custom-link/files'
```

## Installation

You can install the package via composer:

```bash
composer require unisharp/laravel-filemanager
# please check guide https://unisharp.github.io/laravel-filemanager/installation

composer require yaroslawww/nova-laravel-filemanager
```

## Routes

```injectablephp
Route::group([
    'prefix'     => config('lfm.filemanager_path'),
    'middleware' => [ 'web', 'auth' ],
], function () {
    \UniSharp\LaravelFilemanager\Lfm::routes();
});
```

## Credits

- [![Think Studio](https://yaroslawww.github.io/images/sponsors/packages/logo-think-studio.png)](https://think.studio/)
