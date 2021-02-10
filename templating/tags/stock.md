---
description: >-
  Get the stock of a product as defined in the product's inventory section in
  the Snipcart Dashboard.
---

# Stock

## Single Product Stock

Get the stock of a single product. The `Management Method` of your inventory has to be set to `As a single product`.

```text
{{ stock }}
```

## Variant Product Stock

Get the stock of a product variant. The `Management Method` of your inventory has to be set to `By product variation`.

```text
{{ variants }}
    {{ stock }}
{{ /variants }}
```

