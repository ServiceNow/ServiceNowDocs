---
title: Create and publish a foundation data sync offering definition
description: Create an foundation data sync \(FDS\) offering definition to inform your consumers about the data you’re ready to share.
locale: en-US
release: australia
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring outbound FDS as providers, Configure for providers, Service Exchange for Providers, Service Exchange]
---

# Create and publish a foundation data sync offering definition

Create an foundation data sync \(FDS\) offering definition to inform your consumers about the data you’re ready to share.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Administration** &gt; **FDS Offering Definitions**.

2.  Select **New**.

3.  Determine whether to publish FDS subscriptions automatically or manually.

<table id="table_wl4_ddb_1gc"><thead><tr><th>

Method

</th><th>

Description

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Auto publish FDS subscriptions \(default option\)

</td><td>

After the offering is published, when consumers accept the subscription, it’s automatically published and data is synchronized according to the defined cadence.

</td><td>

If it is not already selected, select the **Auto publish FDS subscriptions** check box.

</td></tr><tr><td>

Manually publish FDS subscriptions

</td><td>

After the offering is published, and consumers accept the subscription, you must acknowledge it and send sample files to let them know about the type of data they will receive.For the detailed procedure, see [Validate foundation data sync subscription items](service-bridge-v2-validate-fds-subscription.md).

</td><td>

Clear the**Auto publish FDS subscriptions** check box.

</td></tr></tbody>
</table>4.  Determine whether consumer FDS requests should be automatically acknowledged with a sample payload automatically sent to the consumer in response to each FDS request or manually acknowledged.

    |Method|Description|Action|
    |------|-----------|------|
    |Auto acknowledge FDS requests|After the offering is published, all FDS requests from consumers are automatically acknowledged and a sample payload is sent to the consumer in response to each FDS request.|If it is not already selected, select the **Auto Acknowledge FDS Requests** check box.|
    |Manually acknowledge FDS requests|After the offering is published, consumer FDS requests must be acknowledged manually. For the detailed procedure, see [Validate foundation data sync subscription items](service-bridge-v2-validate-fds-subscription.md)|Clear the**Auto Acknowledge FDS Requests** check box.|

5.  Provide a name and description.

6.  Select **Save**.

7.  In the Offering items related list, create an offering item.

    For each table you offer to share, you must create an offering item. You can create more than one offering.

    1.  Select **New**.

    2.  In the **Table name** field, select the table you want to share with your consumer.

    3.  In the **Outbound field**, select the table fields you want to share by selecting the lock icon and moving them from the **Available** to the **Selected** column.

    4.  If you selected a non-CMDB table, unlock the **Coalesce field** field, select the table fields you want to share, and move them from the **Available** to the**Selected** column.

    5.  Select **Save**.

8.  Create a dependent relationship for the offering item.

    If the table you are offering depends on another table, you must create a dependent table offering to share the related table. You can create multiple dependent offerings.

    1.  Select **Create Dependent Offering Item**.

    2.  From the drop-down menu, choose a dependent item and select **Create Offering Item**.

    3.  In the **Outbound field**, select the table fields you want to share by selecting the lock icon to unlock the field.

    4.  Select **Save**.

9.  Return to the main offering page by selecting **Back**.

10. In the Consumer criteria related list, add a consumer criteria to determine which consumer instances are eligible to receive the offering.

    For information on consumer criteria, see [Create a consumer criteria](../concept/service-bridge-v2-create-consumer-criteria.md) topic.

11. Select **Publish**.


## Result

The FDS offering is now published. Consumers can request foundation data based on the published FDS offering.

## What to do next

[Acknowledge foundation data sync offering request](service-bridge-v2-acknowledge-FDS-request.md).

