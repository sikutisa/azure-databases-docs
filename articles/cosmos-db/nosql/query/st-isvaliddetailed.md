---
title: ST_ISVALIDDETAILED
titleSuffix: Azure Cosmos DB for NoSQL
description: An Azure Cosmos DB for NoSQL system function that returns if a GeoJSON object is valid along with the reason.
author: seesharprun
ms.author: sidandrews
ms.service: azure-cosmos-db
ms.subservice: nosql
ms.topic: reference
ms.devlang: nosql
ms.date: 08/22/2024
ms.custom: query-reference
---

# ST_ISVALIDDETAILED (NoSQL query)

[!INCLUDE[NoSQL](../../includes/appliesto-nosql.md)]

Returns a JSON value containing a Boolean value if the specified GeoJSON **Point**, **Polygon**, or **LineString** expression is valid, and if invalid, the reason.

## Syntax

```nosql
ST_ISVALIDDETAILED(<spatial_expr>)  
```

## Arguments

| | Description |
| --- | --- |
| **`spatial_expr`** | Any valid GeoJSON **Point**, **Polygon**, or **LineString** expression. |

## Return types

Returns a JSON object containing a boolean value indicating if the specified GeoJSON point or polygon expression is valid. If invalid, the object additionally contains the reason as a string value.

## Examples

The following example how to check validity of multiple objects.

:::code language="nosql" source="~/cosmos-db-nosql-query-samples/scripts/st-isvaliddetailed/query.sql" highlight="2-9":::

:::code language="json" source="~/cosmos-db-nosql-query-samples/scripts/st-isvaliddetailed/result.json":::

## Remarks

- The GeoJSON specification requires that points within a Polygon be specified in counter-clockwise order. A Polygon specified in clockwise order represents the inverse of the region within it.

## Related content

- [System functions](system-functions.yml)
- [`ST_ISVALID`](st-isvalid.md)
