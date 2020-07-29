---
description: There's a bunch of configuration options to tailor the addon to your needs.
---

# Configuration

## Collections & Taxonomies

Define the handles of the products collection and taxonomies. If you change a value, you need to run `php please snipcart:setup` to re-generate the collection/taxonomies and product blueprint.

```php
'collections' => [
    'products' => 'products',
],

'taxonomies' => [
    'categories' => 'categories',
    'taxes' => 'taxes',
]
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
'version' => '3.0.17',
```

## Currency

Define the currency you want to use.

```php
'currency' => 'USD',
```

## Length Unit

Define the length unit you want to use.   
You can choose between the following options: `cm` `m` `in` `ft`

```php
'length' => 'cm',
```

## Weight Unit

Define the weight unit you want to use.   
You can choose between the following options: `g` `kg` `oz` `lb`

```php
'weight' => 'g',
```

## Cart Behaviour

Set this to `none` to prevent the cart from opening every time a product is added.   
Default is `null`

```php
'behaviour' => null,
```

## Cart Image

Define a Glide preset to be applied to the product image that shows in the cart. You may also turn the manipulation off by setting `'manipulation' => false`

```php
'image' => [
    'manipulation' => true,
    'preset' => ['w' => 240, 'q' => 75],
]
```

