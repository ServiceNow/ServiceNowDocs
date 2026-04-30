---
title: Define ERP source configuration for Source-to-Pay
description: ERP source configuration determines the ERP source to which your ERP system connects. Map the integration payload with the Source-to-Pay \(S2P\) tables.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integration settings on Source-to-Pay side, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Define ERP source configuration for Source-to-Pay

ERP source configuration determines the ERP source to which your ERP system connects. Map the integration payload with the Source-to-Pay \(S2P\) tables.

## Before you begin

Role required: sn\_shop.procurement\_administrator

## Procedure

1.  Navigate to **All** &gt; **Finance – ERP Integration** &gt; **ERP Source Configuration**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |ERP|Name of the ERP system.|
    |ERP Source|ERP source for which the integration is required.|
    |Name|Name of the ERP.|

4.  Click **Submit**.


## What to do next

For the defined source configuration:

-   Define service mappings for each integration service by accessing the Service Mappings related list. You can define element level mapping between S2P table fields and payload elements.
-   Map S2P users and corresponding ERP user ids by accessing the ERP User Mappings related list.

