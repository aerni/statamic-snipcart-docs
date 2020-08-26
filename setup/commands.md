---
description: There are a couple of helpful commands at your service.
---

# Commands

## Setup Content

The setup command creates all the necessary collections, taxonomies, and blueprints to get you started. This won't override existing collections, taxonomies, and blueprints.

```bash
php please snipcart:setup
```

You can restore the collections, taxonomies, and blueprints to their factory preset by adding the `--force` flag to the command. This will purge all the changes you may have made.

```text
php please snipcart:setup --force
```

{% hint style="info" %}
The setup command is run automatically during the installation process. You only need to manually run it, if you [change a collection or taxonomy handle](https://snipcart.docs.michaelaerni.ch/setup/configuration#collections-and-taxonomies) in the addon's config.
{% endhint %}

## Migrate Content

The migrate command updates your products collection and entries according to the settings defined in the `sites` array in `config/snipcart.php`.

```text
php please snipcart:migrate
```

{% hint style="info" %}
You need to run this command if you [add or remove a site or change a value](https://snipcart.docs.michaelaerni.ch/setup/configuration#sites).
{% endhint %}

## **Publish Assets**

The config and translations are automatically merged and loaded. You can publish them using the following commands.

### **Config**

Publish the config to `config/snipcart.php` 

```text
php please vendor:publish --tag=snipcart-config
```

### **Translations**

Publish the translations to `resources/lang/vendor/snipcart` 

```text
php please vendor:publish --tag=snipcart-translations
```

