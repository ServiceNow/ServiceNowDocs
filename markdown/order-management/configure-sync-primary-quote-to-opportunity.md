---
title: Sync primary Quote to Opportunity
description: Designate a quote as primary and sync the quote's lines to the opportunity. When sync is enabled, any changes to the quote's lines are synced to the source opportunity lines. An opportunity can have only one quote marked as primary and enabled for sync.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/configure-sync-primary-quote-to-opportunity.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Sync primary Quote to Opportunity

Designate a quote as primary and sync the quote's lines to the opportunity. When sync is enabled, any changes to the quote's lines are synced to the source opportunity lines. An opportunity can have only one quote marked as primary and enabled for sync.

## Before you begin

Role required: admin

Before configuring the sync feature, complete the following instance setup:

1.  Activate the ServiceNow Quote Experience plugin \(App ID: sn\_quote\_mgmt\_adv\).
2.  Submit a support ticket requesting to enable the **Sync Quote to Opportunity** tenant setting.
3.  When the tenant setting is enabled, export and import the transaction blueprint.

## About this task

The sync feature uses the following system objects to control the sync between a primary quote and its source opportunity.

|Type|Display name|Variable name|
|----|------------|-------------|
|Field|Is Synced to Opportunity|`txn.opportunity.isSynced`|
|Field|Opportunity Line Item|`txn.line.opportunity.lineItem`|
|Event|Enable Sync to Opportunity|`txn.syncToOpportunity.enable`|
|Event|Disable Sync to Opportunity|`txn.syncToOpportunity.disable`|
|Integration|Sync to Opportunity|`txn.syncToOpportunity.updateStatus`|

To configure the feature, add a button for each sync event to the layout, configure the event properties, and optionally restrict event access by stage.

## Procedure

1.  Navigate to **All** &gt; **CPQ Administration** &gt; **Transaction** and open the blueprint.

2.  Select **Layouts**.

3.  Add a button to the layout for each sync event: **Enable Sync to Opportunity** and **Disable Sync to Opportunity**.

4.  Open the properties for the **Enable Sync to Opportunity** event.

5.  Add the **Sync to Opportunity** integration \(`txn.syncToOpportunity.updateStatus`\) to the event.

6.  Set the **Event Access** for the event.

7.  Configure the **Disable Sync to Opportunity** event
8.  Open the properties for the **Disable Sync to Opportunity** event.

9.  Add the **Sync to Opportunity** integration \(`txn.syncToOpportunity.updateStatus`\) to the event.

10. Set the **Event Access** for the event.

11. \(Optional\) Restrict event access by stage
12. In **Views**, adjust the access to the sync events for each stage.

    This configuration lets you set the sync events to **No Access** on specific stages.


## Result

When a user selects **Enable Sync to Opportunity**, the quote's lines sync to the source opportunity lines, and subsequent changes to the quote's lines continue to sync. When a user selects **Disable Sync to Opportunity**, the sync stops.

