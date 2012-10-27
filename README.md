# React/Curry

Partial function application.

[![Build Status](https://secure.travis-ci.org/reactphp/curry.png?branch=master)](http://travis-ci.org/reactphp/curry)

## Install

The recommended way to install react/curry is [through composer](http://getcomposer.org).

```JSON
{
    "require": {
        "react/curry": "dev-master"
    }
}
```

## Example

```php
<?php

use React\Curry\Util as Curry;

$add = function ($a, $b) {
    return $a + $b;
};

$addOne = Curry::bind($add, 1);

echo sprintf("%s\n", $addOne(5));
// outputs 6
```

## Tests

To run the test suite, you need PHPUnit.

    $ phpunit

## License

MIT, see LICENSE.

## Credits

* Thank you, Moses Schönfinkel (1889-1942).
* Thank you, Haskell B. Curry (1900-1982).
