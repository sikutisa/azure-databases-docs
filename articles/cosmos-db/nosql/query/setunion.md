---
title: SetUnion
titleSuffix: Azure Cosmos DB for NoSQL
description: An Azure Cosmos DB for NoSQL system function that gets all expressions in two sets.
author: seesharprun
ms.author: sidandrews
ms.service: azure-cosmos-db
ms.subservice: nosql
ms.topic: reference
ms.devlang: nosql
ms.date: 08/22/2024
ms.custom: query-reference
---

# SetUnion (NoSQL query)

[!INCLUDE[NoSQL](../../includes/appliesto-nosql.md)]

Gathers expressions in two sets and returns a set of expressions containing all expressions in both sets with no duplicates.

## Syntax

```nosql
SetUnion(<array_expr_1>, <array_expr_2>)
```

## Arguments

| | Description |
| --- | --- |
| **`array_expr_1`** | An array of expressions. |
| **`array_expr_2`** | An array of expressions. |

## Return types

Returns an array of expressions.

## Examples

This first example uses the function with static arrays to demonstrate the union functionality.

:::code language="nosql" source="~/cosmos-db-nosql-query-samples/scripts/setunion/query.novalidate.sql" highlight="2-5":::

:::code language="json" source="~/cosmos-db-nosql-query-samples/scripts/setunion/result.novalidate.json":::

This last example uses an item that share values within multiple array properties.

:::code language="json" source="~/cosmos-db-nosql-query-samples/scripts/setunion-field/seed.novalidate.json" range="1-2,4-26" highlight="5-23":::

The query returns the union of the two arrays as a new property.

:::code language="nosql" source="~/cosmos-db-nosql-query-samples/scripts/setunion-field/query.novalidate.sql" highlight="3":::

:::code language="json" source="~/cosmos-db-nosql-query-samples/scripts/setunion-field/result.novalidate.json":::

## Remarks

- This function doesn't return duplicates.
- This function doesn't use the index.

## See also

- [System functions](system-functions.yml)
- [`ARRAY_CONTAINS`](array-contains.md)
