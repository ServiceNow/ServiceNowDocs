---
title: Configure concurrent import and parallel loading for Nokia Altiplano
description: Improve the efficiency of large data imports from Nokia Altiplano by configuring concurrent imports and enabling parallel loading. This configuration allows the platform to run multiple data import and transformation jobs simultaneously.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure Nokia Altiplano SGC, Set up Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Configure concurrent import and parallel loading for Nokia Altiplano

Improve the efficiency of large data imports from Nokia Altiplano by configuring concurrent imports and enabling parallel loading. This configuration allows the platform to run multiple data import and transformation jobs simultaneously.

## Before you begin

Role required: TSOM Visibility admin

## About this task

Concurrent import and parallel loading improve performance by dividing large datasets into smaller partitions, allowing multiple transformation and collection jobs to run in parallel. This setup is useful when importing large volumes of equipment, logical connections, and network topology data during bulk or filtered discoveries.

Use the following guidance to optimize performance:

-   If transformation is slow: Enable Concurrent import in the import schedule.
-   If data collection is slow: In addition to enabling concurrent import, configure Parallel loading in the data source and update the system property.

**Note:** Parallel loading works in addition to concurrent import. It does not replace it.

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Nokia Altiplano** &gt; **Import Schedule**.

2.  Configure concurrent import or concurrent import

<table id="choicetable_mpn_2vz_yfc"><thead><tr><th align="left" id="d26791e103">

To

</th><th align="left" id="d26791e106">

Do the following

</th></tr></thead><tbody><tr><td id="d26791e112">

**To enable concurrent import**

</td><td>

1.  Navigate to the **Import Schedule** for the discovery job.
2.  Select the **Concurrent import** checkbox.
3.  Set the **Partition method** to **Custom size**.
4.  In the **Partition size**e field, enter the number of records per partition \(for example, 1000\).
 **Note:** The system splits the dataset into import sets based on the partition size. Each import set is processed in parallel, improving the speed of data transformation.

</td></tr><tr><td id="d26791e154">

**Configure parallel loading in the data source**

</td><td>

1.  Navigate to the corresponding Data Source record.
2.  Select the **Parallel loading** checkbox.
3.  Navigate to Nokia Altiplano &gt; Properties.
4.  Open the system property **sn\_sgc\_altiplano.parallel\_number\_of\_data\_source\_jobs**
5.  Set the value to the desired number of parallel jobs \(for example, `3`\).

**Note:** By default, the number of data source jobs is set to `1`. Increasing this value allows the platform to execute multiple data collection jobs concurrently.

</td></tr></tbody>
</table>
**Related topics**  


[Set up Nokia Altiplano](initial-setup-procedure.md)

[Mapping Nokia Altiplano CIs and Relationships in CMDB](../concept/data-mapping.md)

[System components installed with Nokia Altiplano](../reference/properties-installed-with-nokia-altiplano.md)

