---
description: Follow the instructions below to setup Snipcart for Statamic.
---

# Installation

## Install Addon

Install the addon with Composer:

```bash
composer require aerni/snipcart
```

## Perform Basic Configuration

The installation process will automatically publish the addon's config to `config/snipcart.php`. Open the config and perform the following configuration:

1. **Sites:** Add the desired currency, length, and weight units for each of your sites. [Learn more](configuration.md#sites)
2. **Collections & Taxonomies:** Add the collections and taxonomies you want to use for your products. [Learn more](configuration.md#collections-and-taxonomies)

## Run Setup Command

After configuring your **Sites** and **Collections & Taxonomies,** you may run the `setup` command. This will create all the necessary collections, taxonomies, and blueprints to get you started.

```bash
php please snipcart:setup
```

After running the command, make sure to customize the configuration of the created collections and taxonomies to define the sites, templates, routes, etc.

## Add Snipcart API Keys

Add your Snipcart API keys to your `.env` file. You can find them in your [Snipcart dashboard](https://app.snipcart.com/dashboard/account/credentials).

```bash
SNIPCART_LIVE_KEY=************************
SNIPCART_LIVE_SECRET=************************

SNIPCART_TEST_KEY=************************
SNIPCART_TEST_SECRET=************************
```

## Add Script Tag

Add the following tag to your layout view. Snipcart recommends adding it directly after the `<body>` element.

```markup
{{ snipcart:script }}
```

## Add Webhook URL

Add the absolute URL of the configured Snipcart webhook to your [Snipcart Dashboard](https://app.snipcart.com/dashboard/webhooks), eg. `https://my-shop.com/webhooks/snipcart`

You can [customize the webhook route](https://snipcart.docs.michaelaerni.ch/setup/configuration#snipcart-webhook-route) in the config. The default route is `webhooks/snipcart`.

