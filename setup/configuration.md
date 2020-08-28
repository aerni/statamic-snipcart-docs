---
description: There's a bunch of configuration options to tailor the addon to your needs.
---

# Configuration

## Publish Config

To start customizing the config, you first need to publish it to `config/snipcart.php` using this command:

```text
php please vendor:publish --tag=snipcart-config
```

## Sites

This addon supports [Statamic Multi-Sites](https://statamic.dev/multi-site). This lets you define the currency, length and weight unit for each site defined in `config/statamic/sites.php`. If you add or remove a site or change a value, you need to [run the migration command](https://snipcart.docs.michaelaerni.ch/setup/commands#migrate-content) to update the products collection and entries.

```php
'sites' => [

    'default' => [
        'currency' => 'USD',
        'length' => 'in',
        'weight' => 'oz',
    ],
    
],
```

## Collections & Taxonomies

Define the handles of the products collection and taxonomies. If you change a value, you need to [run the setup command](https://snipcart.docs.michaelaerni.ch/setup/commands#setup-content) to re-generate the collection, taxonomies, and blueprints.

```php
'collections' => [
    'products' => 'products',
],

'taxonomies' => [
    'categories' => 'categories',
    'taxes' => 'taxes',
],
```

## Snipcart API Keys

Your Snipcart API Keys for the Live and Test Environment.

```php
'live_key' => env('SNIPCART_LIVE_KEY'),
'test_key' => env('SNIPCART_TEST_KEY'),
```

## Test Mode

Set this to `false` to start processing real transactions. You probably want to do this in production only.

```php
'test_mode' => env('SNIPCART_TEST_MODE', true),
```

## Snipcart Version

The Snipcart version you want to use.

```php
'version' => '3.0.19',
```

## Cart Behaviour

Set this to `'none'` to prevent the cart from opening every time a product is added.

```php
'behaviour' => null,
```

## Cart Image

Define a [Glide](https://statamic.dev/tags/glide) preset to be applied to the product image that shows in the cart. You may also turn the manipulation off by setting `manipulation` to `false`.

```php
'image' => [
    'manipulation' => true,
    'preset' => ['w' => 240, 'q' => 75],
]
```

