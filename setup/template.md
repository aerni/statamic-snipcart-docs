---
description: >-
  Add the following tags to your template to include the necessary Snipcart
  assets.
---

# Template

## Head

Add this tag to the `<head>` of your template to render Snipcart's **preconnect hints** and **stylesheet**.

```markup
{{ snipcart:head }}
```

If you want more control, you may add the **preconnect hints** and **stylesheet** separately instead.

```markup
{{ snipcart:preconnet }}
{{ snipcart:stylesheet }}
```

## Body

Add this tag before the closing `<body>` tag of your template to render Snipcart's **container** and **script**.

```markup
{{ snipcart:body }}
```

If you want more control, you may add the **container** and **script** separately instead.

```markup
{{ snipcart:container }}
{{ snipcart:script }}
```

{% hint style="danger" %}
Make sure to include the **script** after the **container**.
{% endhint %}

