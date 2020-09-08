# Modifiers

## Add Operator

Use this modifier to prepend the operator to a money variable.

```markup
{{ price_modifier }} // $1.00
{{ price_modifier | add_operator }} // +$1.00
```

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

## Total

Use this modifier to calculate the total price of a product variation option.

```markup
{{ variations }}
    {{ options }}
        {{ price | total }}
    {{ /options }}
{{ /variations }}
```

