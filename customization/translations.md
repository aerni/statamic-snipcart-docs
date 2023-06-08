---
description: You can customize the default translations or add your own.
---

# Translations

## Publish Translations

To start customizing the translations, you first need to publish them to `lang/vendor/snipcart` using this command:

```
php please vendor:publish --tag=snipcart-translations
```

## Customize Translations

### Buttons

The translation of **buttons** are located in: \
`lang/vendor/snipcart/{language}/buttons.php`

### Currencies

The translation of **currencies** are located in: \
`lang/vendor/snipcart/{language}/currencies.php`

### Units

The translation of **length** and **weight** units are located in: \
`lang/vendor/snipcart/{language}/units.php`

## Add Translations

You can add your own translations by placing them into: `lang/vendor/snipcart/{language}/{filename}.php`
