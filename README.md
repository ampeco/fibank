Fibank
======

Fibank Ecomm Service for Laravel

Installation
------------

Installation using composer:

```
composer require gentor/fibank
```


Add the service provider in `config/app.php`:

```php
Gentor\Fibank\ServiceProvider::class,
```

Add the facade alias in `config/app.php`:

```php
Gentor\Fibank\Facade\Fibank::class,
```

Configuration
-------------

Convert .pfx certificate to .pem:

```php
openssl pkcs12 -in <cert.pfx> -out <cert.pem> -passin pass:<password> -passout pass:<password>
```

Change your default settings in `app/config/fibank.php`:

```php
<?php
return [
    'certificate' => env('FIBANK_CERTIFICATE_PEM'),
    'password' => env('FIBANK_CERTIFICATE_PASSWORD'),
    'live_mode' => env('FIBANK_LIVE_MODE'),
];
```


Documentation
-------------

[Fibank](https://www.fibank.bg/)

