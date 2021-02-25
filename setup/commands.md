---
description: >-
  There are a couple of commands to help you with the setup of Snipcart for
  Statamic.
---

# Commands

## Setup

The `setup` command creates all the necessary collections, taxonomies, and blueprints to get you started. The command won't override existing collections, taxonomies, and blueprints.

```bash
php please snipcart:setup
```

You can restore the collections, taxonomies, and blueprints to their factory preset by adding the `--force` flag to the command. This will purge all the changes you may have made.

```text
php please snipcart:setup --force
```

{% hint style="info" %}
You need to run this command whenever you update your [Sites](https://snipcart.docs.michaelaerni.ch/setup/configuration#sites) or [Collections & Taxonomies](https://snipcart.docs.michaelaerni.ch/setup/configuration#collections-and-taxonomies) in your config.
{% endhint %}

## **Sync Sites**

The `sync-sites` command syncs your Snipcart sites in with your Statamic sites.

```text
php please snipcart:sync-sites
```

{% hint style="info" %}
Run this command whenever you **add** or **delete** a Statamic site or **change** a site's handle. 
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

