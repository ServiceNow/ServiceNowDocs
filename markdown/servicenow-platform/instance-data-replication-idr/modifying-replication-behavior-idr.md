---
title: Modifying replication behavior in Instance Data Replication
description: Modify how data is replicated by configuring optional settings in Instance Data Replication \(IDR\).Coalesce records using a different column when records on the consumer instance have a different sys\_id than the same record on the producer instance in Instance Data Replication \(IDR\).Preserve producer values in system fields when replicating data in Instance Data Replication \(IDR\).Trigger workflows after replication using platform business rules.
locale: en-US
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Replicate data, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Modifying replication behavior in Instance Data Replication

Modify how data is replicated by configuring optional settings in Instance Data Replication \(IDR\).

## Custom coalescing

Coalesce records using a different column when records on the consumer instance have a different sys\_id than the same record on the producer instance in Instance Data Replication \(IDR\).

By default, the **sys\_id** field is used to coalesce records in IDR. Beginning with the San Diego release, you can choose to use a different field.

Use the coalesce columns feature when records on the consumer instance have a different sys\_id than the same record on the producer instance. For example, when a record is created by Discovery and loaded into multiple instances, the sys\_id might not match. In this scenario, you can use a different unique identifier field by selecting the **Enable Custom Coalesce** option and choosing a coalesce field on the producer Replication entry form.

When you select the **Coalesce** field, you must verify the following:

-   The field that you selected is in the Included Fields on the Replication Entry form on the producer instance.
-   The field exists with the same name, length, and type on the consumer instance.

    **Note:** The **Coalesce** field can be different on the consumer instance if you create a valid transform for the field.

-   The **Unique** column value for the field that you selected is set to **true** in the Dictionary Entry \[sys\_dictionary\] table.

Don’t change the value of the field after it’s set as the **Coalesce** field.

To change the **Coalesce** field after it has been set, you must delete the Replication Entry on the producer instance and create a new Replication Entry.

If the **Coalesce** field doesn’t exist on the consumer instance, the following error is displayed on the Consumer Replication Set form. `The consumer instance does not recognize the <column_name> coalesce field as a valid member of the <table_name> table. Create this field or enable a transformation with this table to receive updates from the producer table to the consumer instance.`

### Errors when using coalesce with transformation

If transform is enabled on the producer instance, the **Coalesce** field on the target table must have the same name, type, and length. If any of those parameters don’t match, an error is displayed.

If transform is enabled on the producer instance, the mapping is invalid for the **Coalesce** field, and the consumer syncs entries, the system displays an error on the Consumer Replication Set form.

If transform is enabled for a replication entry with a valid mapping of the **Coalesce** field and then the table schema for the target table is updated so that the mapping is no longer valid, the system displays an error on the Replication Entry form.

If a replication entry attempts to enable transform and a valid mapping for the **Coalesce** field doesn’t exist from the source table to the target table, the system displays an error on the Replication Entry form.

## Preserving system field values

Preserve producer values in system fields when replicating data in Instance Data Replication \(IDR\).

To preserve the user name in an Activities entry, select the **Preserve Modified By** option on the Inbound Entry form on a consumer replication set.

For example, the **Work Notes** field is an Activity type in change request records. When a user updates a change request, the work note moves into the Activities stream.

-   If you do not select **Preserve Modified By**, Instance Data Replication appears in place of the user name in the consumer records.
-   If you select **Preserve Modified By**, the user who updated the change request is identified in the entry and the system prepends IDR to their name.

![Preserve modified by.](../image/preserved-modified-by-2.png)

When replicating changes, **Preserve modified by** affects values for the **Updated by**, **Updated**, **Created**, and **Created by** system fields:

-   When **Preserve modified by** is enabled and you include system fields in the producer replication entry, producer system field values are replicated to the consumer records. If you do not include system fields in the producer replication entry, default system values from the consumer instance are used instead.
-   When **Preserve modified by** is disabled, default system field values from the consumer instance are used, which means they may not match the system field values in records on the producer.

When seeding data, the **Preserve modified by** setting has no effect:

-   If you include system fields in the producer replication entry, producer system field values appear in the seeded records.
-   If you do not include system fields in the producer replication entry, null values appear in the system fields for seeded records.

## Triggering workflows after replication

Trigger workflows after replication using platform business rules.

Inserts and updates that are replicated to a consumer instance can trigger business rules configured on the target table. A business rule is a server-side script that is associated with a table. Use business rules to trigger workflows that are associated with replications, such as sending a notification or validating the replicated data.

Business rules are part of the ServiceNow AI Platform. For more information, see [Business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/business-rules-classic/c_BusinessRules.md).

To run a business rule after replication, select the **Run Business Rule** option on the Inbound Entry form in a consumer replication set. IDR will invoke the business rules that are associated with the specified table after replicating the data to the table.

