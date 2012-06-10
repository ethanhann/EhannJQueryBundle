# Installation

## Add EhannJQueryBundle to your vendor/bundles/ directory

### Using the vendors script

Add the following lines in your ``deps`` file

```
[EhannJQueryBundle]
    git=http://github.com/ethanhann/EhannJQueryBundle.git
    target=/bundles/Ehann/JQueryBundle
```

Run the vendors script

    ./bin/vendors install

### Using submodules

``` bash
$ git submodule add http://github.com/ethanhann/EhannJQueryBundle.git vendor/bundles/Ehann/JQueryBundle
```

## Add the Ehann namespace to your autoloader

``` php
<?php
// app/autoload.php

$loader->registerNamespaces(array(
    'Ehann' => __DIR__.'/../vendor/bundles',
    // ...
);
```

## Add the EhannJQueryBundle to your application kernel

``` php
<?php
// app/AppKernel.php

public function registerBundles()
{
    return array(
        new Ehann\JQueryBundle\EhannJQueryBundle(),
        // ...
    );
}
```

## Populate the assets

Run the symfony command

``` bash
$ php app/console assets:install web
```

Next : [Usage](http://github.com/ethanhann/EhannJQueryBundle/blob/master/Resources/doc/usage.md)
