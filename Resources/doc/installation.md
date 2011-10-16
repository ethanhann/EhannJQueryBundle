# Installation

## Add IvoryJQueryBundle to your vendor/bundles/ directory

### Using the vendors script

Add the following lines in your ``deps`` file

```
[IvoryJQueryBundle]
    git=http://github.com/egeloen/IvoryJQueryBundle.git
    target=/bundles/Ivory/JQueryBundle
```

Run the vendors script

    ./bin/vendors update

### Using submodules

``` bash
$ git submodule add http://github.com/egeloen/IvoryJQueryBundle.git vendor/bundles/Ivory/JQueryBundle
```

## Add the Ivory namespace to your autoloader

``` php
<?php
// app/autoload.php

$loader->registerNamespaces(array(
    'Ivory' => __DIR__.'/../vendor/bundles',
    // ...
);
```

## Add the IvoryJQueryBundle to your application kernel

``` php
<?php
// app/AppKernel.php

public function registerBundles()
{
    return array(
        new Ivory\JQueryBundle\IvoryJQueryBundle(),
        // ...
    );
}
```

## Populate the assets

Run the symfony command

``` bash
$ php app/console assets:install web
```

Next : [Usage](http://github.com/egeloen/IvoryJQueryBundle/blob/master/Resources/doc/usage.md)
