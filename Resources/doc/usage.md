# Usage

The Ivory JQuery bundle provides full JQuery & JQuery UI ressources.
For understanding the following explanation, please read this article first : http://symfony.com/doc/current/book/templating.html#including-stylesheets-and-javascripts-in-twig

## JQuery

The JQuery script doesn't need to be minify by assetic because it is already minify.

```
{% javascripts "@IvoryJQueryBundle/Resources/public/js/jquery-1.5.1.min.js" %}
    <script type="text/javascript" src="{{ asset_url }}"></script>
{% endjavascripts %}
```

## JQuery UI

Like the JQuery script, the JQuery UI script doesn't need to be minify for the same reason.

```
{% javascripts "@IvoryJQueryBundle/Resources/public/js/*" %}
    <script type="text/javascript" src="{{ asset_url }}"></script>
{% endjavascripts %}
```

## JQuery themes

The Ivory JQuery bundle provides all the JQuery themes.
Warning, the JQuery themes are not minimified.

To add the ``black-tie`` theme, you just need to do that:

### Not minimified

```
{% stylesheets "@IvoryJQueryBundle/Resources/public/themes/black-tie/*.css" %}
    <link rel="stylesheet" type="text/css" media="screen" href="{{ asset_url }}" />
{% endstylesheets %}
```

### Minimified

For understanding what minimify is, please read this article first : http://symfony.com/doc/current/cookbook/assetic/yuicompressor.html

```
{% stylesheets "@IvoryJQueryBundle/Resources/public/themes/black-tie/*.css" filter="yui_css" %}
    <link rel="stylesheet" type="text/css" media="screen" href="{{ asset_url }}" />
{% endstylesheets %}
```

Previous : [Installation](http://github.com/egeloen/IvoryJQueryBundle/blob/master/Resources/doc/installation.md)
