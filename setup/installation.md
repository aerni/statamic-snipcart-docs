---
description: Follow the instructions below to setup Snipcart for Statamic.
---

# Installation

## Install Addon

**Option 1:** Install the addon with Composer.

```bash
composer require aerni/snipcart
```

**Option 2:** Install the addon through the Addons section in the Statamic Control Panel.

## Perform Basic Configuration

The installation process will automatically publish the addon's config to `config/snipcart.php`. Open the config and perform the following configuration:

1. **Sites:** Add the desired currency, length, and weight units for each of your sites
2. **Collections & Taxonomies:** Define the handles for your products collection and categories taxonomy

## Run Setup Command

After configuring your **Sites** and **Collection & Taxonomies** you need to run the `setup` command. This command will create all the necessary collections, taxonomies, and blueprints to get you started.

```bash
php please snipcart:setup
```

## Add Snipcart API Keys

Add your Snipcart API keys to your `.env` file. You can find them in your [Snipcart dashboard](https://app.snipcart.com/dashboard/account/credentials).

```bash
SNIPCART_LIVE_KEY=************************
SNIPCART_LIVE_SECRET=************************

SNIPCART_TEST_KEY=************************
SNIPCART_TEST_SECRET=************************
```

## Add Webhook URL

Add the absolute URL of your Snipcart Webhook to your [Snipcart Dashboard](https://app.snipcart.com/dashboard/webhooks), eg. `https://my-shop.com/webhooks/snipcart`

You can [customize the webhook route](https://snipcart.docs.michaelaerni.ch/setup/configuration#snipcart-webhook-route) in the config. The default route is `webhooks/snipcart`.

## Setup Views

### Head Tag

Add this tag to the `<head>` in your view to render Snipcart's `preconnect hints` and `stylesheet`.

```markup
{{ snipcart:head }}
```

If you want more control, you may add the `preconnect hints` and `stylesheet` separately instead.

```markup
{{ snipcart:preconnect }}
{{ snipcart:stylesheet }}
```

### Body Tag

Add this tag before the closing `</body>` in your view to render Snipcart's `container` and `script`.

```markup
{{ snipcart:body }}
```

If you want more control, you may add the `container` and `script` separately instead. Just make sure to include the script after the container.

```markup
{{ snipcart:container }}
{{ snipcart:script }}
```

