# Installation

## Install the package

**Option 1:** Install the package with Composer.

```bash
composer require aerni/statamic-snipcart
```

**Option 2:** Install the addon through the Addons section in the Statamic Control Panel.

## Publish assets

Publish the vendor assets including the addon's config, JavaScript, and language files.

```text
php artisan vendor:publish --provider="Aerni\Snipcart\ServiceProvider"
```

The **config** will be published to `config/snipcart.php`   
The **JavaScript** will be published to `public/vendor/statamic-snipcart/cp.js`   
The **language files** will be published to `resources/lang/vendor/snipcart`

## Add head tag

Add this tag to the `<head>` of your template to render Snipcart's **preconnect hints** and **stylesheet**.

```markup
{{ snipcart:head }}
```

If you want more control, you may add the **preconnect hints** and **stylesheet** separately instead.

```markup
{{ snipcart:preconnet }}
{{ snipcart:stylesheet }}
```

## Add body tag

Add this tag before the closing `<body>` tag of your template to render Snipcart's **container** and **script**.

```markup
{{ snipcart:body }}
```

If you want more control, you may add the **container** and **script** separately instead.

```markup
{{ snipcart:container }}
{{ snipcart:script }}
```

{% hint style="danger" %}
Make sure to include the **script** after the **container**.
{% endhint %}

