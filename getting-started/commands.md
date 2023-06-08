---
description: There are a couple of commands to help you with the setup of this addon.
---

# Commands

## Setup

The `setup` command creates all the necessary collections, taxonomies, and blueprints to get you started. The command won't override existing collections, taxonomies, and blueprints.

```bash
php please snipcart:setup
```

You can restore the collections, taxonomies, and blueprints to their factory preset by adding the `--force` flag to the command. This will purge all the changes you may have made.

```
php please snipcart:setup --force
```

## **Sync Sites**

The `sync-sites` command syncs your Snipcart sites with your Statamic sites.

```
php please snipcart:sync-sites
```

{% hint style="info" %}
Run this command whenever you add or delete a Statamic site or change a site's handle.&#x20;
{% endhint %}
