---
description: >-
  You can configure Snipcart for Statamic with the configuration options
  outlined below.
---

# Configuration

## Sites

Set the currency, length and weight units for each Statamic site. The units set for Statamic's default site act as default Snipcart units. The units of your other sites will be converted from it. 

**Supported currencies:** ISO 4217 letter codes supported by Snipcart, eg. `USD` or `EUR`  
**Supported length units:** `cm`, `m`, `in`, `ft`  
**Supported weight units:** `g`, `kg`, `oz`, `lb`

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
Make sure to keep the sites in sync with your Statamic sites. You can do so by [running the sync-sites command](https://snipcart.docs.michaelaerni.ch/setup/commands#sync-sites).
{% endhint %}

{% hint style="warning" %}
Whenever you update a site, you need to [run the setup command](https://snipcart.docs.michaelaerni.ch/setup/commands#setup) to update your products collection and entries.
{% endhint %}

## Collections & Taxonomies

Define the handles of the products collection and categories taxonomy.

```php
'collections' => [
    'products' => 'products',
],

'taxonomies' => [
    'categories' => 'categories',
],
```

{% hint style="warning" %}
Whenever you change a handle, you need to [run the setup command](https://snipcart.docs.michaelaerni.ch/setup/commands#setup) to setup the new products collection and categories taxonomy.
{% endhint %}

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

Set this to `none` to prevent the cart from opening every time a product is added. Default is `null`.

```php
'behaviour' => null,
```

## Cart Image

Define a [Glide](https://statamic.dev/tags/glide) preset to be applied to the product image that shows in the cart. You may also turn the manipulation off \(not recommended\).

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

