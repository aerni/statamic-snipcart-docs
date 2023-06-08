---
description: >-
  You can configure Snipcart for Statamic with the configuration options
  outlined below.
---

# Configuration

## Sites

Set the currency, length, and weight units for each Statamic site. The units will be converted from a product's root entry in a multi-site setup.

**Supported currencies:** ISO 4217 letter codes supported by Snipcart, eg. `USD` or `EUR`\
**Supported length units:** `cm`, `m`, `in`, `ft`\
**Supported weight units:** `g`, `kg`, `oz`, `lb`

```php
'sites' => [

    'english' => [
        'currency' => 'USD',
        'length' => 'in',
        'weight' => 'oz',
    ],
    
    'german' => [
        'currency' => 'EUR',
        'length' => 'cm',
        'weight' => 'g',
    ],
    
],
```

{% hint style="info" %}
Make sure to keep the sites in sync with your Statamic sites. You can do so by [running the sync-sites command](https://snipcart.docs.michaelaerni.ch/setup/commands#sync-sites)[.](commands.md#sync-sites)
{% endhint %}

## Collections & Taxonomies

Configure your product collections and taxonomies.

```php
'products' => [
    [
        'collection' => 'games',
        'taxonomies' => ['genres'],
    ],
    [
        'collection' => 'movies',
        'taxonomies' => ['genres', 'directors'],
    ],
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

## Snipcart Settings

Configure any settings you want to apply to the Snipcart script. Make sure to set the keys exactly as documented, e.g., `LoadCSS`. [All available settings.](https://docs.snipcart.com/v3/setup/installation#settings)

```php
'snipcart_settings' => [
    'version' => '3.5.0',
    'loadStrategy' => 'on-user-interaction',
],
```

## Cart Image

Define a [Glide](https://statamic.dev/tags/glide) preset to be applied to the product image in the cart. You may also turn the manipulation off (not recommended).

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
