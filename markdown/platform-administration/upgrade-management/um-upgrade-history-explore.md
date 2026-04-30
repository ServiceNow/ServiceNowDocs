---
title: Explore Upgrade History in Upgrade Console
description: The Upgrade History module maintains a comprehensive record of all upgrades performed on an instance. This module allows you to access detailed reports for both historical and recent upgrade versions.
locale: en-US
release: yokohama
product: Upgrade Management
classification: upgrade-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Upgrade Console summary, Exploring Upgrade Console, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Explore Upgrade History in Upgrade Console

The Upgrade History module maintains a comprehensive record of all upgrades performed on an instance. This module allows you to access detailed reports for both historical and recent upgrade versions.

To view an upgrade history record, navigate to Upgrade Console in one of the ways.

<table id="table_oqw_5jr_hdc"><thead><tr><th>

Option

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Using left navigation

</td><td>

1.  Navigate to **All** &gt; **Admin Center** &gt; **Upgrade Management** &gt; **Upgrade History**.
2.  Select an upgrade from the list. On selecting an upgrade from the list, the System Upgrades form appears.

</td></tr><tr><td>

Using Admin tab option

</td><td>

1.  Navigate to **Admin** &gt; **Upgrade Management** &gt; **Upgrade History**.
2.  Select an upgrade from the list. On selecting an upgrade from the list, the System Upgrades form appears.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|From|Name of the previous .war file \(version\).|
|To|Name of the applied .war file \(version\).|
|Upgrade started|Time stamp when the upgrade process began.|
|Upgrade finished|Time stamp when the upgrade process was completed.|

<table id="table_mc5_sql_hdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Changes skipped

</td><td>

Total number of records that are different from the previous upgrade and the upgrade component was not applied, mostly due to customization.

</td></tr><tr><td>

Changes applied

</td><td>

Total number of changes that are applied as a part of this upgrade**Changes applied** is sum of updated and different records, added to the number of deleted records \(where the value of changed is true\) added to the number of inserted records \(where the value of changed is true\).

</td></tr><tr><td>

Changes processed

</td><td>

Total number of records that were processed as a part of this upgrade. Changes processed is the sum of **Changes skipped** and **Changes applied**.

</td></tr><tr><td>

Copies to review

</td><td>

Total number of copied records to review whose base records have been upgraded.

</td></tr></tbody>
</table>See [Upgrade History tool in Upgrade Console](um-upgrade-history-tool.md) for more information.

