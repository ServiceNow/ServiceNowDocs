---
title: Upgrade History module: Track every upgrade
description: The Upgrade History module tracks every upgrade made to an instance. Administrators can use the module to resolve upgrade conflicts and optionally to revert customizations to base system versions to take advantage of new features.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Upgrades and conversions, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade History module: Track every upgrade

The Upgrade History module tracks every upgrade made to an instance. Administrators can use the module to resolve upgrade conflicts and optionally to revert customizations to base system versions to take advantage of new features.

An upgrade history record is created for each upgrade that is run. To view an upgrade history record, navigate to **System Diagnostics** &gt; **Upgrade History** and click the upgrade.

**Note:** Debug Upgrade provides detailed debugging output for transactions containing artifacts affected by the most recent upgrade, and is designed to assist in upgrade error resolution. See [Debug upgrade](../../administer/platform-upgrades/reference/debug-upgrade.md).

**Note:** The **Payload** and **Payload Hash** fields have been removed from the Upgrade History record in a previous release.

<table id="table_zqk_sxn_1p"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

From

</td><td>

Name of the previous .war file \(version\).

</td></tr><tr><td>

To

</td><td>

Name of the applied .war file \(version\).

</td></tr><tr><td>

Upgrade started

</td><td>

Time stamp when the upgrade process began.

</td></tr><tr><td>

Upgrade finished

</td><td>

Time stamp when the upgrade process was completed.

</td></tr><tr><td>

Changes skipped

</td><td>

Total number of records that were different from the previous upgrade but were skipped, mostly likely due to customization. Changes skipped is the sum of the records that have disposition of skipped manual merge \(where the value of changed is true\), added to the number of records that have disposition of skipped error, added to the number of records that were skipped and different.

 **Note:** To prevent your customizations from being overwritten during system upgrades, the upgrade process skips \(does not apply the update to\) objects that have been customized. One of your responsibilities as the administrator is to resolve each update that was skipped due to a customization. To resolve a skipped update, you review the reason for each skipped record and then either merge the customization or revert the customization to the base system.

</td></tr><tr><td>

Changes applied

</td><td>

Total number of the changes that were applied in this upgrade. Changes applied is sum of updated and different records, added to the number of deleted records \(where the value of changed is true\) added to the number of inserted records \(where the value of changed is true\).

</td></tr><tr><td>

Changes processed

</td><td>

Total number of items processed during this upgrade. Changes processed is the sum of Changes skipped, plus Changes applied.

</td></tr></tbody>
</table><table id="table_gfb_5jd_tbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Updated and different

</td><td>

Number of Upgrade Detail records for which the value of the disposition is updated, and the value of changed is equal to true.

 This does not appear on the form by default.

</td></tr><tr><td>

Updated and not different

</td><td>

Number of Upgrade Detail records for which the value of the disposition is updated, and the value of changed is equal to false.

 This does not appear on the form by default.

</td></tr><tr><td>

Skipped and different

</td><td>

Number of Upgrade Detail records for which the value of the disposition is skipped, and the value of changed is equal to true.This does not appear on the form by default.

</td></tr><tr><td>

Skipped and not different

</td><td>

Number of Upgrade Detail records for which the value of the disposition is skipped, and the value of changed is equal to false.This does not appear on the form by default.

</td></tr></tbody>
</table>## Review Skipped Records form section

The [Skipped Changes to Review related list](skipped-changes-to-review-related-list.md) displays each record that was skipped during the upgrade process. Use the list to review the reason for each skipped record in the list and then either merge your customization or revert your customization to the base system.

-   **[Skipped Changes to Review related list](skipped-changes-to-review-related-list.md)**  
To prevent your customizations from being overwritten during system upgrades, the upgrade process skips \(does not apply the update to\) objects that have been customized. To assist you in tracking and resolving skipped update records that need review, Skipped Changes to Review lists all updates skipped during the upgrade process.
-   **[Skipped Changes Reviewed related list](skipped-changes-reviewed-related-list.md)**  
Skipped Changes Reviewed lists update records that previously appeared on the **Skipped Changes to Review** related list and have been reviewed. When you select a skipped record to review and set a **Resolution Status** to a value other than Not Reviewed, the update record moves to the Skipped Changes Reviewed related list.
-   **[Customizations Unchanged related list](customizations-unchanged-related-list.md)**  
Customizations Unchanged lists all records that were skipped \(due to a customization\), but the changes that were going to be applied in this upgrade have not changed from the last upgrade.
-   **[Changes Applied related list](changes-applied-related-list.md)**  
Changes Applied lists all changes that were applied in this upgrade.
-   **[Claim Outcomes to Review related list](claim-outcomes-to-review-related-list.md)**  
During system upgrades, the Claim Status tab displays outcomes to review and resolve. See the Claim Status field in the table below.
-   **[Upgrade Details related list](c_UpgradeDetails.md)**  
Upgrade Details lists all Upgrade Details records for this upgrade.

**Parent Topic:**[Upgrades and conversions](upgrades-conversions.md)

