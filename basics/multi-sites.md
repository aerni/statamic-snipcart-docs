# Multi-Sites

## Important

There are some important behaviors to keep in mind when setting up your shop as a Multi-Site with different locales. The UI of your Snipcart cart will always be displayed in the locale of your current site. However, Snipcart doesn't fully support multiple locales. Meaning, names, and values of your custom product fields like text fields, checkboxes, and product variants can not be translated. 

You can still translate all the localizable fields in your Statamic Control Panel. However, the translation will be exclusive to the Front End of your shop. The Snipcart buttons, and cart, therefore, will always fall back to the values of your default site.

{% hint style="warning" %}
Snipcart doesn't fully support multiple locales. Your Snipcart buttons and cart will always fall back to the default locale.
{% endhint %}

## Variants

Please make sure to always keep the order of your variations in sync between your sites. This is very important, as the product button of your variant will automatically pick the correct variations in the Snipcart cart.

