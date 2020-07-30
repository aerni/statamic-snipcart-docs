---
description: You can customize translations or add your own.
---

# Translations

## Publish Translations

To start customizing the translations, you first need to publish them to `resources/lang/vendor/snipcart` using this command:

```text
php please vendor:publish --tag=snipcart-translations
```

## Customize Translations

### Buttons

The translation of **buttons** are located in:   
`resources/lang/vendor/snipcart/{language}/buttons.php`

### Currencies

The translation of **currencies** are located in:   
`resources/lang/vendor/snipcart/{language}/currencies.php`

### Units

The translation of **length** and **weight** units are located in:   
`resources/lang/vendor/snipcart/{language}/units.php`

## Add Translations

You can add your own translations by placing them into: `resources/lang/vendor/snipcart/{language}/{filename}.php`

