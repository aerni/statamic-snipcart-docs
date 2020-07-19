---
description: Output data of the weight unit defined in the config.
---

# Weight

## Weight abbreviation

The abbreviation of the weight unit, e.g. `kg`.

```text
{{ weight:abbr }}
```

## Weight singular name

The singular name of the weight unit, e.g. `Kilogram`.

```text
{{ weight:singular }}
```

## Weight plural name

The plural name of the weight unit, e.g. `Kilograms`.

```text
{{ weight:plural }}
```

## Tag pair

Alternatively, you can also access this information with a tag pair.

```text
{{ weight }}
    {{ abbr }} {{ singular }} {{ plural }}
{{ /weight }}
```

