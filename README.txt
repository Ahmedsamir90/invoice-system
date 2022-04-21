kindly noted: 

package was developed on PHP 7.3.11 and Laravel 6.2, but should work on lower versions too

Features


Taxes - fixed or rate - for item or for invoice
Discounts - fixed or by percentage - for item or for invoice
Shipping - add shipping price to your invoices
Automatic calculation - provide minimal set of information, or calculate yourself and provide what to print
Due date
Easy to customize currency format
Serial numbers as you like it
Templates
Translations
Global settings and overrides on-the-fly

Installation
Via Composer

Laravel version <= 9
$ composer require laraveldaily/laravel-invoices:^3.0
Laravel version <= 8
$ composer require laraveldaily/laravel-invoices:^2.0
Laravel version <= 7
$ composer require laraveldaily/laravel-invoices:^1.3
After installing Laravel Invoices, publish its assets, views, translations and config using the invoices:install Artisan command:

$ php artisan invoices:install
Updates
Since it is evolving fast you might want to have latest template after update using Artisan command:

$ php artisan invoices:update
It will give a warning if you really want to override default resources

Or alternatively it can be done separately.

$ php artisan vendor:publish --tag=invoices.views --force
$ php artisan vendor:publish --tag=invoices.translations --force
For Laravel version < 5.5
If you don't use auto-discovery, add the ServiceProvider to the providers array in config/app.php

LaravelDaily\Invoices\InvoiceServiceProvider::class,
If you want to use the facade to generate invoices, add this to your facades in config/app.php

'Invoice' => LaravelDaily\Invoices\Facades\Invoice::class
