---
description: >-
  Output Snipcart-specific HTML elements like a product button or the total
  number of items in the cart.
---

# Snipcart

## Buy Button

This tag creates a Snipcart product buy button with all the `data-item-*` attributes according to the product's content. This is arguably the most important tag as it does all the heavy lifting for you. Learn more about [product attributes](https://docs.snipcart.com/v3/setup/products).

```html
{{ snipcart:buy }}
```

{% hint style="info" %}
The automatic generation of attributes only works on a product page or inside a product collection loop. If you use the tag in any other place, you must manually define each attribute.
{% endhint %}

### Manually Defining Attributes

You can manually define any accepted attribute directly on the tag. You can also use this to override the values of automatically generated attributes.

```html
{{ snipcart:buy id="{{ increment }}" name="{{ some_variable }}" }}
```

### Customize Button

You can also fully customize your buy buttons with your own markup. Use this tag to get the product's data attributes:

```html
<button {{ snipcart:attributes }} class="snipcart-add-item button">
    Add to cart
</button>
```

{% hint style="info" %}
Don't forget to add the **snipcart-add-item** class to your custom button.
{% endhint %}

## Cart Button

A Snipcart cart button.

```
{{ snipcart:cart }}
```

## Sign-in Button

A Snipcart sign-in button.

```
{{ snipcart:signin }}
```

## Total Items

The total number of items in the cart.

```
{{ snipcart:items }}
```

## Total Price

The total price of items in the cart.

```
{{ snipcart:price }}
```

## Parameters

There are a couple of parameters you may use on the tags.

| Parameter | Description                     | Supported By                          |
| --------- | ------------------------------- | ------------------------------------- |
| `class`   | Add classes to the HTML element | `buy` `cart` `signin` `items` `price` |
| `text`    | Override the default text       | `buy` `cart` `signin`                 |

**Example:** Add some classes to the cart button and override the default text.

```
{{ snipcart:cart class="p-2 bg-gray-100" text="Checkout" }}
```
