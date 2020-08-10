---
description: >-
  Output Snipcart-specific HTML elements like a product button or the total
  number of items in the cart.
---

# Snipcart

## Buy Button

This tag creates a Snipcart product buy button with all the `data-item-*` attributes according to the product's content. This is arguably the most important tag as it does all the heavy lifting for you. Learn more about [product attributes](https://docs.snipcart.com/v3/setup/products).

```text
{{ snipcart:buy }}
```

{% hint style="warning" %}
The automatic generation of attributes only works when looping through the collection of products. If you use the tag outside of it, you'll have to manually define each attribute yourself.
{% endhint %}

### Defining Attributes

You can manually define any accepted attribute directly on the tag. You can also use this to override the values of automatically generated attributes.

```text
{{ snipcart:buy id="{{ increment }}" name="{{ some_variable }}" }}
```

### Customize Button

You can also fully customize your buy buttons with your own markup. Use this tag to get the product's data-attributes:

```text
{{ snipcart:attributes }}
```

{% hint style="warning" %}
Don't forget to add the class **snipcart-add-item** to turn the element into a Snipcart product.
{% endhint %}

## Cart Button

A Snipcart cart button.

```text
{{ snipcart:cart }}
```

## Sign-in Button

A Snipcart sign-in button.

```text
{{ snipcart:signin }}
```

## Total Items

The total number of items in the cart.

```text
{{ snipcart:items }}
```

## Total Price

The total price of items in the cart.

```text
{{ snipcart:price }}
```

## Parameters

There are a couple of parameters you may use on the tags.

| Parameter | Description | Supported By |
| :--- | :--- | :--- |
| `class` | Add classes to the HTML element | `buy` `cart` `signin` `items` `price` |
| `text` | Override the default text | `buy` `cart` `signin` |

**Example:** Add some classes to the cart button and override the default text.

```text
{{ snipcart:cart class="p-2 bg-gray-100" text="Checkout" }}
```

