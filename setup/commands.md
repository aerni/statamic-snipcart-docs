# Commands

## Setup Command

The setup command is run **automatically** during the installation process. You only need to manually run it, if you [change a collection or taxonomy handle](https://snipcart.docs.michaelaerni.ch/setup/configuration#collections-and-taxonomies) in the addon's config.

```bash
php please snipcart:setup
```

The command creates the collection for the products, the taxonomies for the categories and taxes, and their blueprints. It respects existing collections and taxonomies with the same handle and won't override them.

You can override existing collections, taxonomies, and blueprints by adding the `--force` flag to the command.

```text
php please snipcart:setup --force
```

