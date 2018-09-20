LARAVEL 5.5.* XSS Protection
===========

A port of CodeIgniter Security Library to Laravel for XSS prevention

Installation
------------

Include the package in your composer file

    "require": {
        "Anspectoryno/laravel-xss": "dev-master"
    }
    

Run composer update

Add the service provider in you app.php config file in the 'providers' array

    Anspectoryno\LaravelXss\LaravelXssServiceProvider::class

and add the alies also in the app.php config file in the 'aliases' array

    'Xss'			  => Anspectoryno\LaravelXss\LaravelXssFacade::class


Usage
-----

Use the Xss::clean($str, $is_image = FALSE) to clean user input. For example:

    $cleaned = Xss::clean(Input::get('comment');

or for use with images

    $cleaned = Xss::clean(Input::file('profile'), TRUE);
