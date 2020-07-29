---
description: >-
  Install the addon, setup your views and add your Snipcart API Keys to get
  started.
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

## Add Snipcart API Keys

Add your Snipcart API keys to your `.env` file. You can find the keys in your [Snipcart dashboard](https://app.snipcart.com/dashboard/account/credentials).

```bash
SNIPCART_LIVE_KEY=************************
SNIPCART_TEST_KEY=************************ 
```

