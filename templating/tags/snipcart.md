---
description: >-
  Output Snipcart-specific HTML elements like a product button or the total
  number of items in the cart.
---

# Snipcart

## Product button

A Snipcart product button. The `data-item-*` attributes are automatically generated based on the product's content. Learn more about [Snipcart's product attributes](https://docs.snipcart.com/v3/setup/products).

```text
{{ snipcart:product }}
```

### Overriding attributes

You can override any attribute directly on the tag.

```text
{{ snipcart:product id="{{ increment }}" name="{{ some_variable }}" }}
```

{% hint style="info" %}
If you use this tag outside of the product collection, you'll have to manually define the product attributes to make it work.
{% endhint %}

## Cart button

A Snipcart cart button.

```text
{{ snipcart:cart }}
```

## Sign-in button

A Snipcart sign-in button.

```text
{{ snipcart:signin }}
```

## Total items

The total number of items in the cart.

```text
{{ snipcart:items }}
```

## Total price

The total price of items in the cart.

```text
{{ snipcart:price }}
```

## Parameters

There are a couple of parameters you may use on the tags.

| Parameter | Description | Support |
| :--- | :--- | :--- |
| `class` | Add classes to the HTML element | `product` `cart` `signin` `items` `price` |
| `text` | Override the default text | `product` `cart` `signin` |

**Example:** Style the button and override the default text.

```text
{{ snipcart:cart class="p-2 bg-gray-100" text="Checkout" }}
```

