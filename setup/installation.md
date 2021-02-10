---
description: Follow the following instructions to setup Snipcart for Statamic.
---

# Installation

## Install Addon

**Option 1:** Install the addon with Composer.

```bash
composer require aerni/snipcart
```

**Option 2:** Install the addon through the Addons section in the Statamic Control Panel.

## Publish Config

Publish the config with the following command. The config will be published to `config/snipcart.php` .

```text
php please vendor:publish --tag=snipcart-config
```

## Add Snipcart API Keys

Add your Snipcart API keys to your `.env` file. You can find the keys in your [Snipcart dashboard](https://app.snipcart.com/dashboard/account/credentials).

```bash
SNIPCART_LIVE_KEY=************************
SNIPCART_LIVE_SECRET=************************

SNIPCART_TEST_KEY=************************
SNIPCART_TEST_SECRET=************************
```

## Add Webhook URL

Add the absolute URL of your Snipcart Webhook in your [Snipcart Dashboard](https://app.snipcart.com/dashboard/webhooks). You can [customize the webhook route](https://snipcart.docs.michaelaerni.ch/setup/configuration#snipcart-webhook-route) in the config. The default route is `webhooks/snipcart`.

## Setup Views

### Head Tag

Add this tag to the `<head>` of your view to render Snipcart's **preconnect hints** and **stylesheet**.

```markup
{{ snipcart:head }}
```

If you want more control, you may add the **preconnect hints** and **stylesheet** separately instead.

```markup
{{ snipcart:preconnect }}
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

