---
title: Updating ID fields
description: To generate new Federated IDs, you can either use the existing user resolution search criteria or update the criteria before regeneration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/identity/updating-id-fields.html
release: brazil
product: Identity
classification: identity
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Global Identity, Identity]
---

# Updating ID fields

To generate new Federated IDs, you can either use the existing user resolution search criteria or update the criteria before regeneration.

## Before you begin

Role required: iamsync\_admin

**Important:** Any change to the ID fields results in the change of Federated IDs **for all existing records** on the selected table. These changes may have implications on performance, compliance, and licensing.

## About this task

In ServiceNow, Federated IDs verify consistent user identification across multiple instances. By default, the **User ID** and **Email** ID fields are used as the system's search criteria for identifying and matching users across instances. You can change these fields to meet your requirements, as long as the criteria includes at least one unique field. When you change the ID fields, the system regenerates Federated IDs \(a hash based on the selected ID fields\) for all records in the selected table based on the updated criteria. You can regenerate Federated IDs in two ways:

-   **Update**: Updates the system with your new search criteria when you add or remove ID fields. Use when you want to remove or add fields \(such as Employee Number\) or modify which attributes define a unique user. This approach is helpful for improving accuracy or aligning with new compliance requirements.
-   **Regenerate Federated IDs**: Uses existing search criteria when you only needed to refresh Federated IDs without changing the identification logic. This is useful after XML data imports, the instance not working correctly, or low-level database updates.

## Procedure

1.  Navigate to **All** &gt; **Manage Federated ID** &gt; **Federated ID Criteria**.

    The **Federated ID Criteria** page displays Role and User record.

2.  Select the record.

3.  Select **Regenerate Federated IDs** and read the notes in steps \#5 and \#6 to complete the procedure.

    To change the criteria, proceed to the next step.

4.  Use the right and left arrow buttons to add or remove ID fields from the **Selected** list.

    All ID fields listed under **Selected** are used to generate new Federated IDs. For example, **Employee number**.

    **Note:**

    -   The **Selected** list must include at least one unique field. The **User ID** field is no longer required — it qualifies as a unique field, but you can select any other unique field instead. You can select more than one unique field, but at least one must remain.
    -   Only fields whose uniqueness is enforced on a single column can be selected as a unique field: a field marked unique in the dictionary, or a field with a single-column unique database index. Fields with a non-unique index, and fields that are unique only as part of a composite \(multi-column\) index, can't be used as the unique field.
    -   **User ID** and **Email** are used to generate Federated IDs by default.
    -   A record must have a value in a selected unique field for a Federated ID to be generated. If no selected unique field has a value, the Federated ID is null for that record.
    -   If more than one user share the same values in the selected ID fields, then the system generates a Federated ID for only one of the users.
    \[Omitted image "id-fields.png"\] Alt text: ID Fields

    Now, the **Employee number** selected is set to another attribute for identifying and resolving users and generating the hashed Federated ID.

5.  Select **Update** to generate Federated IDs.

    **Note:** Wait for the **Completion Percentage** to reach `100` before initiating another **Update** or **Regenerate Federated IDs**.

    The status percentage indicates the Federated ID generation for all identities across instances.

    **Note:**

    -   Don’t change a field until the previous **Update** job or **Regenerate Federated IDs** is complete.
    -   Fields that are updated should be a string type.
    -   Fields that can't be select as ID fields are as follows:
        -   System level fields
        -   Edge encryption fields
        -   Password fields
6.  Navigate to the **sys\_user** table to view the new Federated IDs that are generated due to updating the ID fields.


