---
title: IS_FINITE_NUMBER
titleSuffix: Azure Cosmos DB for NoSQL
description: An Azure Cosmos DB for NoSQL system function that returns a boolean indicating if a number is a countable (finite) number.
author: seesharprun
ms.author: sidandrews
ms.service: azure-cosmos-db
ms.subservice: nosql
ms.topic: reference
ms.devlang: nosql
ms.date: 08/22/2024
ms.custom: query-reference
---

# IS_FINITE_NUMBER (NoSQL query)

[!INCLUDE[NoSQL](../../includes/appliesto-nosql.md)]

Returns a boolean indicating if a number is a finite number (not infinite).

## Syntax

```nosql
IS_FINITE_NUMBER(<numeric_expr>)
```

## Arguments

| | Description |
| --- | --- |
| **`numeric_expr`** | A numeric expression. |

## Return types

Returns a boolean.

## Examples

This example demonstrates the function with various static values.

:::code language="nosql" source="~/cosmos-db-nosql-query-samples/scripts/is-finite-number/query.sql" highlight="2-4":::

:::code language="json" source="~/cosmos-db-nosql-query-samples/scripts/is-finite-number/result.json":::

## Remarks

- This function benefits from a [range index](../../index-policy.md#includeexclude-strategy).

## See also

- [System functions](system-functions.yml)
- [`IS_NUMBER`](is-number.md)
