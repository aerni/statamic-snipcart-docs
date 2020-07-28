---
description: Configure the package to get started.
---

# Configuration

## Publish assets \(optional\)

The vendor assets will be automatically published after installation. The default config will be merged and the translations loaded.

### **Config**

You may publish the config to `config/snipcart.php` using this command:

```text
php please vendor:publish --tag="snipcart-config"
```

### **Translations**

You may publish the translations to `resources/lang/vendor/snipcart` using this command:

```text
php please vendor:publish --tag="snipcart-translations"
```



## Add the Snipcart API keys

Add your **Snipcart API keys** to your `.env` file. You can find them in your [Snipcart dashboard](https://app.snipcart.com/dashboard/account/credentials).

```bash
SNIPCART_LIVE_KEY=************************
SNIPCART_TEST_KEY=************************
```

## Configure package settings

Make sure to review the package config published to `config/snipcart.php` to get an overview of the available settings and options.

