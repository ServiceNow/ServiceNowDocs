---
title: Determine the statement item type
description: Determine the type of statement item as a first step to create a statement item. Or, you must determine the source from where the consumption or usage details and the cost of consumption data is retrieved.
locale: en-US
release: zurich
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Financial charging application setup - Legacy, Financial Charging - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Determine the statement item type

Determine the type of statement item as a first step to create a statement item. Or, you must determine the source from where the consumption or usage details and the cost of consumption data is retrieved.

## Before you begin

Role required: service\_charging\_analyst

**Important:**

This feature is available only when you own an ITBM Analyst license.

## About this task

-   **Consumption Statement Item**

    The cost of the consumption statement item is generated every fiscal period from any platform table that contains the consumption data. Cost information could also come from the same table or can be applied from a rate card.

-   **Cost Model Statement Item**

    The cost model statement item retrieves the allocated unit cost data from the Financial Modeling application.

-   **Service Catalog Statement Item**

    You can derive the cost, consumption volumes, and consumption details of an item from the Requested Item \(sc\_req\_item\) table in service catalog.


## Procedure

1.  Navigate to **All** &gt; **Financial Charging** &gt; **Administration** &gt; **Statement Items**.

2.  To create a statement item, click **New**, or click the name of an existing statement item that you want to edit in the Statement Items list.

3.  Select the type of statement item you want to create.


## What to do next

Define a statement item depending on the source where your consumption data is available.

|Field|Description|
|-----|-----------|
|Consumption Statement Item|Link to create a consumption statement item.|
|Cost Model Statement Item|Link to create a cost model statement item.|
|Service Catalog Statement Item|Link to create a service catalog statement item.|

-   **[Define a consumption statement item](define-consumption-statmt-item.md)**  
If your cost and business service usage details are sourced from an external consumption table, then you can source the consumption details of the consumption table for the statement item.
-   **[Define a cost model statement item](define-cost-model-statement-item.md)**  
The cost of the item or service is derived from the allocation lines of financial modeling application. The statement item captures the cost from the segment accounts, specific accounts in a segment, or buckets in an account, which gives you the cost of the statement item for a fiscal period.
-   **[Define a service catalog statement item](define-service-catalog-statmt-item.md)**  
A business service can be represented by a service catalog category or a catalog item. When a service request from the service catalog is fulfilled, the price listed for the service in the service catalog item is captured as the cost of the statement item for a fiscal period.

**Parent Topic:**[Financial charging application setup - Legacy](../concept/financial-reporting-appln-setup.md)

