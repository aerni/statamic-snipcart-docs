---
description: Output data of the currency defined in the config.
---

# Currency

## Currency code

The code of the currency, e.g. `USD`.

```text
{{ currency:code }}
```

## Currency name

The name of the currency, e.g. `US Dollar`

```text
{{ currency:name }}
```

## Currency symbol

The symbol of the currency, e.g. `$`

```text
{{ currency:symbol }}
```

## Tag pair

Alternatively, you can also access this information with a tag pair.

```text
{{ currency }}
    {{ code }} {{ name }} {{ symbol }}
{{ /currency }}
```

