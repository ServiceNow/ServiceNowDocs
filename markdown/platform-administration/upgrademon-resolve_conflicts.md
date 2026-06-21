---
title: Resolve conflicts for an individual record
description: Reconcile differences between your customized record and the changes associated with the upgrade.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-administration/upgrademon-resolve\_conflicts.html
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Upgrade Monitor module: Upgrade an individual instance, Upgrades and conversions, Upgrade, Administer the ServiceNow AI Platform]
---

# Resolve conflicts for an individual record

Reconcile differences between your customized record and the changes associated with the upgrade.

## Before you begin

Role required: admin

## Procedure

1.  From the [Upgrade Details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/upgrademon-upgrade-details-form.md) for the record you are reconciling, click **Resolve Conflicts**.

    The system displays the [Resolve Conflicts form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/upgrademon-resolve-conflicts-form.md), which highlights differences between the two versions of the record. The form displays information about the base system record on the left and the customized record on the right.

2.  Compare the base system with the customized record for each field on this form, and for non-script fields, edit the customized record to include what you want from the base system and the customization.

3.  If this record contains a script, check it for conflicts and resolve.

    1.  Click inside the Script field.

        The system displays the Resolve Conflicts - Script form highlighting areas where the two versions of the script differ.

    2.  Edit the script by clicking the small arrows that correspond to the blocks of code until script contains whichever content you want.

    3.  Click **OK**.

        The system returns to the Resolve Conflicts form.

4.  To save your changes to the record, click **Save Merge**.

    The system sets the **Resolution** for this record to **Reviewed and Merged**.


-   **[Upgrade Details form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/upgrademon-upgrade-details-form.md)**  
From the Upgrade Details form, you can review an individual record affected by the upgrade and reconcile conflicts between the upgrade and customizations.
-   **[Resolve Conflicts form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/upgrademon-resolve-conflicts-form.md)**  
The Resolve Conflicts form you compare to the base system version with the customized version of a record and reconcile the differences.

**Parent Topic:**[Upgrade Monitor module: Upgrade an individual instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-administration/upgrademon-landing-page.md)

**Related topics**  


[bundle-cadev.t_CompareToCurrentVersion]

[bundle-cadev.t_ComparePushedVerLocalVer]

[bundle-platcap.compare-two-article-versions]

[bundle-cadev.t_ResolveACollision]

[bundle-cadev.t_RevertAChange]

[bundle-cadev.view-customer-update-records]

