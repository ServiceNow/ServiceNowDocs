---
title: System Upgrade form
description: When an upgrade is complete, the System Upgrades form displays key statistics about the upgrade and a related list of skipped records \(the skipped list\).
locale: en-US
release: zurich
product: Upgrade Center
classification: upgrade-center
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Process the skipped records list, Scheduling and monitoring an upgrade, Use, Upgrade Center, Upgrade, Administer]
---

# System Upgrade form

When an upgrade is complete, the System Upgrades form displays key statistics about the upgrade and a related list of skipped records \(the skipped list\).

![Image showing the System Upgrades form](../image/uc-system-upgrade-form.png)

<table id="table_b5b_p14_dlb"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

From

</td><td>

Version of the instance before upgrading.

</td></tr><tr><td>

To

</td><td>

Version of the instance after upgrading.

</td></tr><tr><td>

Upgrade started

</td><td>

Time of the start of the upgrade.

</td></tr><tr><td>

Upgrade finished

</td><td>

Time at which the upgrade completed.

</td></tr><tr><td>

Changes skipped

</td><td>

Total number of records that are different from the previous upgrade and the upgrade component was not applied, mostly due to customization.

</td></tr><tr><td>

Changes applied

</td><td>

Total number of changes that are applied as a part of this upgrade**Changes applied** is sum of updated, different records, deleted records \(where the value of changed is true\) and inserted records \(where the value of changed is true\).

</td></tr><tr><td>

Changes processed

</td><td>

Total number of records that were processed as a part of this upgrade. Changes processed is the sum of **Changes skipped** and **Changes applied**.

</td></tr><tr><td>

Copies to review

</td><td>

Total number of copied records to review whose base records have been upgraded

</td></tr></tbody>
</table>