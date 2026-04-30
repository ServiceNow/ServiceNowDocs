---
title: Set access restrictions using an entity based record access update utility
description: Set access restrictions for the existing records in bulk by using the Entity based record access update utility guided-experience. Use the workflow to enable or disable access to record types.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage Entity Based Access, Entity Based Access, Common GRC features, Governance, Risk, and Compliance]
---

# Set access restrictions using an entity based record access update utility

Set access restrictions for the existing records in bulk by using the Entity based record access update utility guided-experience. Use the workflow to enable or disable access to record types.

## Before you begin

Role required: sn\_grc\_ent\_access.bulk\_access\_config\_admin

## About this task

By configuring a bulk access update, you can apply the entity-based access restrictions to multiple records in bulk.

The system provides real-time status tracking of update operations, categorized as Completed, Failed, or Update queued. After each update, a comprehensive log is generated, detailing updated records, applied scopes, and execution outcomes.

## Procedure

1.  Navigate to **All** &gt; **Entity Based Access Configurations** &gt; **Entity based record access update utility**.

2.  Select **New**.

3.  In the **Scope entities** section, do the following:

    1.  Select the entity scope from the **Make entity scope selection based on** drop-down list.

    2.  Select entities, entity types, or entity classes.

    3.  Mark **Select downstream entities also** if you want to include the downstream entities in scoping.

        **Note:** You can see this option only when you select one entity.

    4.  Select **Mark as complete and proceed**.

4.  In the **Scope related records** section, select the related records you want to set access to, and do the following:

    1.  Select a record type from the **Add a record type** drop-down list.

    2.  Select another record type from the **Add another record type** drop-down list.

    3.  Apply conditions on each record type.

    4.  Select **Mark as complete and proceed**.

5.  In the **Preview record counts** section, preview how many records for each record type are impacted based on the selected scope of entities and record types.

    1.  Select **I want to preview** to preview record counts.

    2.  Select **Back to scope related records** to navigate to the previous step where you can select the related records.

    3.  From **Set Access**, either **Enable access restrictions** or **Disable access restrictions** for the scoped entities and record types.

    4.  Confirm applying access restrictions to the selected records by selecting **Proceed**.

6.  In the **View results** section, you can see the status of the update operation.


## Result

Entity-based restrictions are enabled or disabled at the record level for the scoped entity types.

-   **[Bulk access update configuration form](../reference/bulk-access-update-configuration-form.md)**  
Use the Bulk access update configuration form to create a bulk configuration within the Entity Based Access application.

**Parent Topic:**[Managing Entity Based Access](../concept/using-entity-based-access.md)

