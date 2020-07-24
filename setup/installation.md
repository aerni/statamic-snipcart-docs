# Installation

## Install the package

**Option 1:** Install the package with Composer.

```bash
composer require aerni/statamic-snipcart
```

**Option 2:** Install the addon through the Addons section in the Statamic Control Panel.

## Publish assets

Publish the vendor assets including the addon's config and language files.

```text
php artisan vendor:publish --provider="Aerni\Snipcart\ServiceProvider"
```

The **config** will be published to `config/snipcart.php`   
The **language files** will be published to `resources/lang/vendor/snipcart`

