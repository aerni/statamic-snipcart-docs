# Basics

## Product collection

The products are stored in a regular **Statamic collection**. You can access the data using Statamic's collection tag with all its bells and whistles. Nothing fancy here.

**Example:** Get the title of all the items in the `products` collection

```text
{{ collection:products }}
    {{ title }}
{{ /collection:products }}
```

