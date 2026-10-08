---
title: Data assets enrichment system properties
description: System properties that control how the AI enrichment process batches assets, runs parallel enrichment lanes, and manages lane timeouts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/ai-enrichment-system-properties-dc.html
release: brazil
topic_type: reference
last_updated: "2026-10-05"
reading_time_minutes: 1
keywords: [AI metadata enrichment, enrichment system properties, Data Catalog, data steward]
breadcrumb: [Reference, Data Catalog, Workflow Data Fabric]
---

# Data assets enrichment system properties

System properties that control how the AI enrichment process batches assets, runs parallel enrichment lanes, and manages lane timeouts.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the filter navigator.

These properties are optional. The default values work for most implementations. Adjust them only if enrichment jobs are running slower than expected or you are tuning performance.

<table><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_dcg\_app.dcg.enrichment.batch\_size**

</td><td>

Number of assets sent to the AI at a time. -   Type: integer
-   Default value: 50
-   Who can change: Admin, Data Steward
-   When to change: Rarely. Leave as is unless enrichment jobs are running slower or failing more than expected.

</td></tr><tr><td>

**sn\_dcg\_app.dcg.enrichment.max\_lanes**

</td><td>

Number of asset groups enriched in parallel. More lanes means more work happening at the same time. -   Type: integer
-   Default value: 10
-   Who can change: Admin, Data Steward
-   When to change: Only between jobs, never while a job is running.

</td></tr><tr><td>

**sn\_dcg\_app.dcg.enrichment.deadline\_ms**

</td><td>

Duration in milliseconds that one lane keeps working before it hands off and restarts itself. For example, 270000 equals 4.5 minutes. -   Type: integer
-   Default value: 270000
-   Who can change: Admin, Data Steward
-   When to change: Rarely. Only when tuning performance with platform support.

</td></tr></tbody>
</table>**Parent Topic:**[Data catalog reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/data-catalog-reference.md)

