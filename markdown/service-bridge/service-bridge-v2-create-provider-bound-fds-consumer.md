---
title: Create and publish a provider-bound foundation data sync offering definition
description: Create a foundation data sync \(FDS\) offering definition to inform your providers about the data you're ready to share.
locale: en-US
release: australia
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configuring outbound FDS as consumers, Configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Create and publish a provider-bound foundation data sync offering definition

Create a foundation data sync \(FDS\) offering definition to inform your providers about the data you're ready to share.

## Before you begin

Version required: 2.3.x.

Role required: admin \(sb\_admin\)

## About this task

As a consumer, you can create FDS offering definitions to share data with providers. This process enables you to configure which tables and fields you want to make available, set up automatic or manual publishing workflows, and define eligibility criteria for providers.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Consumer** &gt; **Administration** &gt; **FDS Offering Definitions**.

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

After the offering is published, when your provider accepts the subscription, it's automatically published and data is synchronized according to the defined cadence.

</td><td>

If it isn’t already selected, select the **Auto publish FDS subscriptions** check box.

</td></tr><tr><td>

Manually publish FDS subscriptions

</td><td>

After the offering is published and the provider accepts the subscription, you must acknowledge it manually. Then send sample files to let them know about the type of data they’ll receive.For the detailed procedure, see TBD.

</td><td>

Clear the **Auto publish FDS subscriptions** check box.

</td></tr></tbody>
</table>4.  Determine whether provider FDS requests should be automatically acknowledged with a sample payload automatically sent to the provider in response to each FDS request or manually acknowledged.

    |Method|Description|Action|
    |------|-----------|------|
    |Auto acknowledge FDS requests|After the offering is published, all FDS requests from providers are automatically acknowledged and a sample payload is sent to the provider in response to each FDS request.|If it isn’t already selected, select the **Auto Acknowledge FDS Requests** check box.|
    |Manually acknowledge FDS requests|After the offering is published, provider FDS requests must be acknowledged manually. For the detailed procedure, see TBD.|Clear the **Auto Acknowledge FDS Requests** check box.|

5.  Provide a name and description for the offering definition.

6.  Select **Save**.

    The FDS offering definition is saved and you can now add offering items.

7.  In the Offering items related list, create an offering item.

    For each table you offer to share with providers, you must create an offering item. You can create more than one offering item to share data from multiple tables.

    1.  Select **New**.

    2.  In the **Table name** field, select the table you want to share with your providers.

    3.  In the **Outbound field**, select the table fields you want to share by selecting the lock icon and moving them from the **Available** to the **Selected** column.

    4.  If it isn’t already selected, select the **AccountSecure** check box to ensure data security.

        When enabled, only records where the company field matches the connection company are synchronized. Clear this option to synchronize all records regardless of company.

        **AccountSecure** option is selected by default.

    5.  If it isn’t already selected, select **Send attachment** check box to send attachment.

        When enabled, file attachments linked to records are included in the synchronization.

        **Send attachment** option is selected by default.

    6.  If you selected a non-CMDB table, unlock the **Coalesce fields**, select the table fields you want share, and move them from the **Available** to the **Selected** column.

        Coalesce fields help identify unique records when synchronizing data between instances.

    7.  If it isn’t already selected, for a non-CMDB table, select the **Maintain SysID** check box to preserve referential integrity.

        When enabled, new records created in the destination instance maintain their original sys\_id. However, if an existing record is updated, the sys\_id may not be preserved.

        **Maintain SysID** option is selected by default for non-CMDB tables and not available for CMDB tables.

    8.  If needed, add conditions to filter which records are shared with providers.

        Use the condition builder to specify criteria that determine which records from the selected table are included in the data sync.

    9.  Select **Save**.

        By default,

8.  Create a dependent relationship for the offering item.

    If the table you’re offering depends on another table, you must create a dependent table offering to share the related table. You can create multiple dependent offerings to maintain referential integrity.

    1.  Select **Create Dependent Offering Item**.

    2.  From the drop-down menu, choose a dependent item and select **Create Offering Item**.

    3.  In the **Outbound field**, select the table fields you want to share by selecting the lock icon to unlock the field.

    4.  Select **Save**.

9.  Preview data for the offering item connection.

    Preview the data that will be synchronized with your provider before publishing the offering. In the preview, you can visualizing available data, test filter conditions, and apply validated conditions directly to the offering item configuration.

    1.  Select **Preview for Connection**.

        You can also access this preview later by opening an existing offering item from the Offering Items related list.

    2.  On the Foundation Data Sync: Preview for connection page, from the Connection drop-down list, select the provider account.

    3.  Add conditions to filter which records are shared with providers.

        Use **Add Filter Condition** to add individual conditions or Add **OR Clause** to add alternative conditions.

    4.  Select **Run** to visualize the data.

        The preview displays all records matching your configuration and filter conditions.

    5.  Apply the filter conditions to the offering item by selecting **Apply to offering item**, then select **OK** when prompted for confirmation.

        The offering item form opens with a banner indicating conditions have changed.

    6.  In the offering item page, save the changes.

        You must save the offering item to apply any changes made during the preview.

10. Return to the main offering page by selecting **Back** or by selecting **offering record** link in the top banner.

11. In the Providers related list, select **Edit** and select a provider from the condition builder to determine which provider instances are eligible to receive the offering.

    Adding a provider help you control which providers can subscribe to your data offerings based on specific attributes or conditions. If you don't select any provider, your offering will be available to all the connected providers.

12. Select **Publish**.


## Result

The FDS offering is now published. Providers can request foundation data based on the published FDS offering.

## What to do next

[Acknowledge foundation data sync offering request.](service-bridge-v2-con-acknowledge-fds-request.md)

**Related topics**  


[Foundation data sync](../concept/service-bridge-v2-explore-foundation-data-sync.md)

[Configuring outbound foundation data sync as consumers](../concept/using-provider-bound-fds-consumer.md)

[Configuring inbound foundation data sync as providers](../concept/service-bridge-v2-configure-inboun-fds-providers.md)

