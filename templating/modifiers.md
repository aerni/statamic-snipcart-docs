---
description: >-
  There are a couple of useful modifiers to help you format variables in your
  templates.
---

# Modifiers

## Add Operator

Use this modifier to prepend the correct operator to a money variable.

```markup
{{ price_modifier }} // $1.00
{{ price_modifier | add_operator }} // +$1.00
```

## Strip Unit

Use this modifier to strip a variable's currency, length, or weight unit.

```markup
{{ price }} // $19.99
{{ price | strip_unit }} // 19.99

{{ length }} // 10 in
{{ length | strip_unit }} // 10

{{ weight }} // 3.5 oz
{{ weight | strip_unit }} // 3.5
```
