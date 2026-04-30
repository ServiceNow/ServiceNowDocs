---
title: Upgrade History module
description: The Upgrade History module tracks every upgrade made to an instance. You can also view the complete report of an old upgrade or a recently completed upgrade version using this module.
locale: en-US
release: xanadu
product: Upgrade Center
classification: upgrade-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Upgrade Center, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade History module

The Upgrade History module tracks every upgrade made to an instance. You can also view the complete report of an old upgrade or a recently completed upgrade version using this module.

To view an upgrade history record, navigate to **All** &gt; **Upgrade Center** &gt; **Upgrade History** and select an upgrade from the list. On selecting an upgrade from the list, the System Upgrades form appears.

|Field|Description|
|-----|-----------|
|From|Name of the previous .war file \(version\).|
|To|Name of the applied .war file \(version\).|
|Upgrade started|Time stamp when the upgrade process began.|
|Upgrade finished|Time stamp when the upgrade process was completed.|

<table id="table_b5b_p14_dlb"><thead><tr><th>

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

Total number of copied records to review whose base records have been upgraded

</td></tr></tbody>
</table>Select Skipped Record VTB related link to view and manage skipped records over VTB. See [Skipped Records visual task board \(VTB\)](uc-vtb-history.md) for more information.

Select View Upgrade Plan History related link to view the details of the upgrade plan configuration. See [Upgrade Plan overview](uc-upgrade-plan.md) for more information.

Select View Upgrade Summary Report related link to view the summary of an older upgrade over Upgrade Monitor module.

See [Review skipped records using related lists](../task/uc-access-rl.md#) for more information about related lists.

