---
title: Resolve conflicts for an individual record
description: Reconcile differences between your customized record and the changes associated with the upgrade.
locale: en-US
release: yokohama
product: Upgrade Center
classification: upgrade-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Scheduling and monitoring an upgrade, Using Upgrade Center, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Resolve conflicts for an individual record

Reconcile differences between your customized record and the changes associated with the upgrade.

## Before you begin

Role required: admin

## Procedure

1.  From the [Upgrade Details form](../reference/uc-upgrade-details-form.md) for the record you are reconciling, click **Resolve Conflicts**.

    The system displays the [Resolve Conflicts form](../reference/uc-resolve-conflicts-form.md), which highlights differences between the two versions of the record. The form displays information about the base system record on the left and the customized record on the right.

    **Note:** The system creates a new customer update record when you click **Resolve Conflicts**.

2.  Compare the base system with the customized record for each field on this form.

    For non-script fields, edit the customized record on the right-hand side to include what you want from the base system and the customization.

3.  If this record contains a script, check it for conflicts and resolve.

    1.  Click inside the Script field.

        The system displays the Resolve Conflicts - Script form highlighting areas where the two versions of the script differ.

    2.  Edit the right-hand side so that the script contains whichever content you want. To move a block of code from the left to right side, click the small arrows corresponding to that block in the middle column.
    3.  Click **OK**.

        The system returns to the Resolve Conflicts form.

4.  To save your changes to the record, click **Save Merge**.

    The system sets the **Resolution** for this record to **Reviewed and Merged**.


