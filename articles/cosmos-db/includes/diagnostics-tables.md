---
ms.service: azure-cosmos-db
ms.topic: include
ms.date: 08/23/2024
---

For Azure Diagnostics tables, all data is written into one single table. Users specify which category they want to query. If you want to view the full-text query of your request, see [Monitor Azure Cosmos DB data by using diagnostic settings in Azure](../monitor-resource-logs.md#enable-full-text-query-for-logging-query-text) to learn how to enable this feature.

For [resource-specific tables](../monitor-resource-logs.md#create-diagnostic-settings), data is written into individual tables for each category of the resource. We recommend this mode because it:

- Makes it much easier to work with the data.
- Provides better discoverability of the schemas.
- Improves performance across both ingestion latency and query times.
