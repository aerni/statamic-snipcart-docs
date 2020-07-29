---
description: There are a couple of helpful commands at your service.
---

# Commands

## Setup Content

The setup command creates all the necessary collections, taxonomies, and blueprints to get you started. It is careful enough to not override existing collections, taxonomies, and blueprints with the same handle.

```bash
php please snipcart:setup
```

You can override existing collections, taxonomies, and blueprints by adding the `--force` flag to the command.

```text
php please snipcart:setup --force
```

{% hint style="info" %}
The setup command is run **automatically** during the installation process. You only need to manually run it, if you [change a collection or taxonomy handle](https://snipcart.docs.michaelaerni.ch/setup/configuration#collections-and-taxonomies) in the addon's config.
{% endhint %}

## **Publish Assets**

The config and translations are automatically merged and loaded. You can publish them using the following commands.

### **Config**

Publish the config to `config/snipcart.php` 

```text
php please vendor:publish --tag="snipcart-config"
```

### **Translations**

Publish the translations to `resources/lang/vendor/snipcart` 

```text
php please vendor:publish --tag="snipcart-translations"
```

