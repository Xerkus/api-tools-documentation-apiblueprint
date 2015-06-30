API Blueprint Documentation Provider for Apigility
==================================================

Introduction
------------

This module provides Apigility the ability to show API documentation through a
[Apiary](https://apiary.io/) documentation.

In addition to providing Apiary documentation, module also plugs in the original Apigility documentation and provides content negotiated response with raw [API Blueprint](https://apiblueprint.org).

Requirements
------------
  
Please see the [composer.json](composer.json) file.

Installation
------------

Run the following `composer` command:

```console
$ composer require "zfcampus/zf-apigility-documentation-apiblueprint"
```

Alternately, manually add the following to your `composer.json`, in the `require` section:

```javascript
"require": {
    "zfcampus/zf-apigility-documentation-apiblueprint": "~1.0-dev"
}
```

And then run `composer update` to ensure the module is installed.

Finally, add the module name to your project's `config/application.config.php` under the `modules`
key:

```php
return array(
    /* ... */
    'modules' => array(
        /* ... */
        'ZF\Apigility\Documentation\ApiBlueprint',
    ),
    /* ... */
);
```

Usage
-----
Apiary documentation can be found on `/apigility/blueprint/:api` uri and is accessible from the Apigility welcome page.

Querying API Blueprint
---------------------
When raw API Blueprint is needed, request can be done via content negotiation. Target uri is `/apigility/blueprint/:api` and Accept header is `text/vnd.apiblueprint+markdown`.

To learn more about API Blueprint language, please check its [specification](https://github.com/apiaryio/api-blueprint/blob/master/API%20Blueprint%20Specification.md).
