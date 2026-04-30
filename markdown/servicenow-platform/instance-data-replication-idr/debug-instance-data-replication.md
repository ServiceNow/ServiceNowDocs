---
title: Identify Instance Data Replication errors
description: Identify Instance Data Replication \(IDR\) errors by viewing the metadata for messages between producer and consumer instances, payload error logs, and message logs.
locale: en-US
release: zurich
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Resolving errors, Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Identify Instance Data Replication errors

Identify Instance Data Replication \(IDR\) errors by viewing the metadata for messages between producer and consumer instances, payload error logs, and message logs.

## Before you begin

Role required: idr\_admin or admin

## Procedure

1.  View the producer or consumer metadata logs.

<table id="choicetable_h3s_qkz_pkb"><tbody><tr><td id="d340369e62">

**Producer**

</td><td>

Navigate to **Instance Data Replication** &gt; **Producer Replication Sets**, select a producer replication set and click the **Replication Metadata Logs** related link.

</td></tr><tr><td id="d340369e83">

**Consumer**

</td><td>

Navigate to **Instance Data Replication** &gt; **Consumer Replication Sets**, select a consumer replication set and click the **Replication Metadata Logs** related link.

</td></tr></tbody>
</table>2.  On either the producer instance or the consumer instance, to view transformation errors and replications that failed to load:

    1.  Navigate to **Instance Data Replication** &gt; **Replication Payload Error**.

        If the **Source** value is **Seeding**, the error occurred during seeding. If the source value is different, the error occurred during a replication set update. If any column breaks during transformation, transformation for the entire table breaks and data is not replicated in the table.

    2.  Select an error in the Created column.

        The **Error Message** field on the Payload Error pane describes the payload error.

3.  View the replication log on either the producer instance or the consumer instance:

    1.  Navigate to **Instance Data Replication** &gt; **Replication Log**.

    2.  Select an entry.

        The Instance Data Replication Log form shows the message and message level.


**Parent Topic:**[Resolving data replication errors in Instance Data Replication](../reference/common-issues-idr.md)

