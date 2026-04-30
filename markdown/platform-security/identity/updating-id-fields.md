---
title: Updating ID fields
description: Update the ID fields to regenerate the Federated IDs based on the updated fields.
locale: en-US
release: xanadu
product: Identity
classification: identity
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Global Identity, Identity]
---

# Updating ID fields

Update the ID fields to regenerate the Federated IDs based on the updated fields.

## Before you begin

Role required: iamsync\_admin

**Note:** Any changes to the ID fields result in the change of Federated Ids for all the existing records on the selected table. These changes may have implications on performance, compliance, and licensing.

## Procedure

1.  Navigate to **All** &gt; **Manage Federated ID** &gt; **Federated ID Criteria**.

2.  Select the Type Name \(**User**\).

3.  Select the new ID fields in the Federated ID Criteria User page that you want to add from the Available to Selected using the arrow buttons.

    For example, **Employee number**.

    **Note:**

    -   User name is required for generating Federated IDs.
    -   User name and email are used to generate Federated IDs by default.
    -   If there are users with duplicate user names and email, then the Federated ID is generated only for one user. If the user name is null or empty, then the Federated ID is null.
    ![ID Fields](../images/id-fields.png)

    Now, the **Employee number** selected becomes another attribute for generating the Federated ID.

4.  Select **Update** to generate Federated IDs.

    **Note:** Select **Update** first and then check for the completion percentage \(100\) before initiating another update.

    The status percentage indicates the Federated ID generation for all the identities across instances.

    **Note:**

    -   Until the previous update job is complete, don’t change the field.
    -   Fields that are updated should be a string type.
    -   Fields that cannot be select as ID fields are as follows:
        -   System level fields
        -   Edge encryption fields
        -   Password fields.
5.  Navigate to the sys\_user table to view the new Federated IDs that are generated due to updating the ID fields.

    **Note:** Select **Regenerate Federated IDs** if a user is created or updated via XML imports, low-level database updates, the instance not working correctly. Selecting **Regenerate Federated IDs**, regenerates the IDs for all the users, using the current id field criteria.


