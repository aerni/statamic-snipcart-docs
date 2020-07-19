---
description: Output data of the length unit defined in the config.
---

# Length

## Length abbreviation

The abbreviation of the length unit, e.g. `cm`.

```text
{{ length:abbr }}
```

## Length singular name

The singular name of the length unit, e.g. `Centimeter`.

```text
{{ length:singular }}
```

## Length plural name

The plural name of the length unit, e.g. `Centimeters`.

```text
{{ length:plural }}
```

## Tag pair

Alternatively, you can also access this information with a tag pair.

```text
{{ length }}
    {{ abbr }} {{ singular }} {{ plural }}
{{ /length }}
```

