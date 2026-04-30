---
title: Set access restrictions using an entity based record access update utility
description: Set access restrictions for the existing records in bulk by using the Entity based record access update utility guided-experience. Use the workflow to enable or disable access to record types.
locale: en-US
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring access control, Accessing control through organizational structure, Use, Privacy Management, Governance, Risk, and Compliance]
---

# Set access restrictions using an entity based record access update utility

Set access restrictions for the existing records in bulk by using the Entity based record access update utility guided-experience. Use the workflow to enable or disable access to record types.

## Before you begin

Role required: sn\_privacy.admin

## About this task

By configuring a bulk access update, you can apply the entity-based access restrictions to multiple records in bulk.

The system provides real-time status tracking of update operations, categorized as Completed, Failed, or Update queued. After each update, a comprehensive log is generated, detailing updated records, applied scopes, and execution outcomes.

## Procedure

1.  Navigate to **All** &gt; **Entity Based Access Configurations** &gt; **Entity based record access update utility**.

2.  Select **New**.

3.  In the Scope entities section, do the following:

    1.  From the Make entity scope selection based on drop-down list, select the entity scope .

    2.  In the Select entities option, select the name of the entity \(for which you have created the access configuration\).

    3.  Mark **Select downstream entities also** to include the downstream entities in scoping.

        **Note:** You can see this option only when you select one entity.

    4.  Select **Mark as complete and proceed**.

4.  In the Scope related records section, select the related records that you want to set access to, and do the following:

    1.  From the Add a record type drop-down list, select a record type .

    2.  From the **Add another record type** drop-down list, select another record type .

    3.  Apply conditions on each record type.

    4.  Select **Mark as complete and proceed**.

5.  In the Preview record counts section, preview how many records for each record type are impacted based on the selected scope of entities and record types.

    1.  Select **I want to preview** to preview record counts.

    2.  Select **Back to scope related records** to navigate to the previous step where you can select the related records.

    3.  From **Set Access**, select either **Enable access restrictions** or **Disable access restrictions** for the scoped entities and record types.

    4.  Confirm applying access restrictions to the selected records by selecting **Proceed**.

6.  In the View results section, you can see the status of the update operation.

    You can also view log details for the configuration record, including the update status. The system supports the following states:.

    -   Update queued: The update is actively being processed.
    -   Completed: The update was successfully applied to all selected records.
    -   Failed: The update cannot be executed due to configuration issues or system errors. In the Failed state, a **Retry** button is available to trigger the update again.

## Result

Entity-based restrictions are enabled at the record level for the scoped entity. The system creates a scheduled job that runs at intervals \(default: 1 hour\) to update records in batches for entity-based access restrictions.

**Parent Topic:**[Configuring access control](../configure-access-control-by-legal-entity.md)

