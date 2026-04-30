---
title: Instance Data Replication system properties
description: These system properties control the behavior of the Instance Data Replication \(IDR\) application.
locale: en-US
release: yokohama
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Reference, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Instance Data Replication system properties

These system properties control the behavior of the Instance Data Replication \(IDR\) application.

To set IDR system properties, navigate to the System Properties \[sys\_properties\] table and add the property.

<table id="table_gfn_112_bxb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

The record batch size for data comparison results

 `idr.instance.comparison.batch.size`

</td><td>

If the data comparison results exceed 1 million records within the given date range, the request is divided into batches of 10,000 records.-   Type: integer
-   Default value: 10,000

</td></tr><tr><td>

The maximum runtime

 `idr.instance.comparison.max.runtime`

</td><td>

The maximum amount of time allowed for running a data comparison.-   Type: integer
-   Default value: 15 minutes

</td></tr><tr><td>

Fields to skip

 `idr.dct.comparison.skip.fields`

</td><td>

The list of fields to skip when comparing records between instances. -   Type: string
-   Default value: caller\_id,sys\_created\_on,sys\_created\_by,sys\_updated\_on,sys\_updated\_by

</td></tr></tbody>
</table><table id="table_cbn_dym_gxb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Stop replication if an out-of-order issue occurs

 `idr.message.gap.order_enforcement.enabled`

</td><td>

By default, IDR stops replication if an out-or-order issue occurs on the consumer. You can change the default behavior when an out of order issue occurs on the consumer by adding this property and setting it to `false`. This automatically re-queues and replicates missing messages using the most recent record details from the producer without stopping replication.

-   Type: string
-   True: Stop replication
-   False: Don't stop replication and re-queue

**Note:** Each producer and consumer instance must be on the same family version to use this property. Both instances must be on Vancouver or higher.

</td></tr><tr><td>

Set attachment size limit

`idr.cdc.replication.table.reader.attachment.size`

</td><td>

By default, IDR doesn't restrict the size of attachments.You can change the default behavior by adding this property and entering a maximum size for attachments.

-   Type: integer \(size in bytes\)
-   Default value: 100,000,000

</td></tr><tr><td>

The maximum number of records allowed in a seeding request

 `idr.max.seeding.limit`

</td><td>

If this property isn't set or present, there's no limit on the number of records for seeding requests in V2 replication sets.-   Type: integer
-   Default value:

</td></tr></tbody>
</table>**Parent Topic:**[Instance Data Replication reference](../concept/reference-instance-data-replication.md)

**Related topics**  


[Data privacy in Instance Data Replication](../concept/data-privacy-consumers-idr.md)

[Adapter descriptions for Instance Data Replication](adapter-descriptions.md)

[Excluded tables in Instance Data Replication](IDR-excluded-tables.md)

[Domain separation and IDR](instance-data-replication-domain-separation.md)

[Instance Data Replication roles](instance-data-replication-roles.md#)

