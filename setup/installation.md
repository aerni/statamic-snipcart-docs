---
description: Install the addon and setup your views to get started.
---

# Installation

## Install Addon

**Option 1:** Install the addon with Composer.

```bash
composer require aerni/snipcart
```

**Option 2:** Install the addon through the Addons section in the Statamic Control Panel.

## Setup Views

### Head Tag

Add this tag to the `<head>` of your view to render Snipcart's **preconnect hints** and **stylesheet**.

```markup
{{ snipcart:head }}
```

If you want more control, you may add the **preconnect hints** and **stylesheet** separately instead.

```markup
{{ snipcart:preconnet }}
{{ snipcart:stylesheet }}
```

### Body Tag

Add this tag before the closing `<body>` tag of your view to render Snipcart's **container** and **script**.

```markup
{{ snipcart:body }}
```

If you want more control, you may add the **container** and **script** separately instead. Just make sure to include the script **after** the container.

```markup
{{ snipcart:container }}
{{ snipcart:script }}
```

