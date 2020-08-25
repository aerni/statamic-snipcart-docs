# Modifiers

## Strip Unit

Use this modifier to strip the currency, length, or weight unit from a variable.

```markup
{{ price }} // $19.99
{{ price | strip_unit }} // 19.99

{{ length }} // 10 in
{{ length | strip_unit }} // 10

{{ weight }} // 3.5 oz
{{ weight | strip_unit }} // 3.5
```

