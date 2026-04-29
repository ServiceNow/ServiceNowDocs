---
title: Updating ID fields
description: To generate new Federated IDs, you can either use the existing user resolution search criteria or update the criteria before regeneration.
locale: en-US
release: australia
product: Identity
classification: identity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Global Identity, Identity]
---

# Updating ID fields

To generate new Federated IDs, you can either use the existing user resolution search criteria or update the criteria before regeneration.

## Before you begin

Role required: iamsync\_admin

**Important:** Any change to the ID fields results in the change of Federated IDs **for all existing records** on the selected table. These changes may have implications on performance, compliance, and licensing.

## About this task

In ServiceNow, Federated IDs ensure consistent user identification across multiple instances. By default, the **User ID** and **Email** ID fields are used as the system's search criteria for identifying and matching users across instances. When you change the ID fields, the system regenerates Federated IDs \(a hash based on the selected ID fields\) for all records in the selected table based on the updated criteria. You can regenerate Federated IDs in two ways:

-   **Update.** Updates the system with your new search criteria when you add or remove ID fields. Use when you want to remove or add fields \(such as Employee Number\) or modify which attributes define a unique user. This approach is helpful for improving accuracy or aligning with new compliance requirements.
-   **Regenerate Federated IDs.** Uses existing search criteria when you only need to refresh Federated IDs without changing the identification logic. This is useful after XML data imports, the instance not working correctly, or low-level database updates.

## Procedure

1.  Navigate to **All** &gt; **Manage Federated ID** &gt; **Federated ID Criteria**.

2.  Select the Type Name \(**User**\).

3.  To change the criteria, proceed to the next step. To use the existing Federated ID criteria, click **Regenerate Federated IDs** and read the notes in steps \#5 and \#6 to complete the procedure.

4.  On the **Federated ID Criteria User** page, use the right and left arrow buttons to add or remove ID fields from the **Selected** list. All ID fields listed under **Selected** are used to generate new Federeated IDs.

    For example, **Employee number**.

    **Note:**

    -   **User ID** is required for generating Federated IDs. If the user name is null or empty, then the Federated ID is null.
    -   **User ID** and **Email** are used to generate Federated IDs by default.
    -   If more than one user share the same **User ID** and **Email**, then the system generates a Federated ID for only one of the users.
    ![ID Fields](../images/id-fields.png)

    Now, the **Employee number** selected becomes another attribute for identifying and resolving users and generating the hashed Federated ID.

5.  Click **Update** to generate Federated IDs.

    **Note:** Wait for the **Completion Percentage** to reach `100` before initiating another **Update** or **Regenerate Federated IDs**.

    The status percentage indicates the Federated ID generation for all identities across instances.

    **Note:**

    -   Don’t change a field until the previous **Update** job or **Regenerate Federated IDs**is complete.
    -   Fields that are updated should be a string type.
    -   Fields that cannot be select as ID fields are as follows:
        -   System level fields
        -   Edge encryption fields
        -   Password fields
6.  Navigate to the **sys\_user** table to view the new Federated IDs that are generated due to updating the ID fields.


