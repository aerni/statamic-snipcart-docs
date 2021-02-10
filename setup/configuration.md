---
description: >-
  You can configure Snipcart for Statamic with the configuration options
  outlined on this page.
---

# Configuration

## Sites

Define the currency, length, and weight unit for each site defined in `config/statamic/sites.php`. If you add or remove a site or change a value, you need to [run the migration command](https://snipcart.docs.michaelaerni.ch/setup/commands#migrate-content) to update the products collection and entries.

```php
'sites' => [

    'default' => [
        'currency' => 'USD',
        'length' => 'in',
        'weight' => 'oz',
    ],
    
],
```

{% hint style="warning" %}
The sites need to be in sync with Statamic's sites config. Make sure to add a new key for each site defined in **config/statamic/sites.php**
{% endhint %}

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
'live_secret' => env('SNIPCART_LIVE_SECRET'),

'test_key' => env('SNIPCART_TEST_KEY'),
'test_secret' => env('SNIPCART_TEST_SECRET'),
```

## Test Mode

Set this to `false` to start processing real transactions. You probably want to do this in production only.

```php
'test_mode' => env('SNIPCART_TEST_MODE', true),
```

## Snipcart Version

The Snipcart version you want to use.

```php
'version' => '3.0.29',
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

## Snipcart API Cache Lifetime

Define the cache lifetime of Snipcart API responses in seconds. The API is used for things like fetching the stock of a product.

```php
'api_cache_lifetime' => 3600,
```

## Snipcart Webhook Route

Define the route where the Snipcart webhook requests will be sent to. Don't forget to [add this URL in your Snipcart Dashboard](https://app.snipcart.com/dashboard/webhooks). Set this to `null` to remove the route.

```php
'webhook' => 'webhooks/snipcart',
```

