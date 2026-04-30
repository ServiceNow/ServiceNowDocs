---
title: Exploring Federated ID
description: Determine the users across multiple instances based on user name and email and provide a unique ID \(Federated ID\) to the user across instances.
locale: en-US
release: yokohama
product: Identity
classification: identity
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Global Identity, Identity]
---

# Exploring Federated ID

Determine the users across multiple instances based on user name and email and provide a unique ID \(Federated ID\) to the user across instances.

Federated ID is used to identity users across the multiple ServiceNow® instance. Based on the federated id the user can be identified and the accurate number of users across multiple instances can be determined. For more information, see [Federated ID](federated-id.md).

**Note:** User name is required for generating Federated IDs.

Federated ID is a unique identifier for an identity using a hashing function across the ServiceNow® instances.

## Federated ID for Users

By using the **User ID** and **Email** of the user across the instances, the Federated ID is created and displayed in the **sys\_user** table.

After upgrading to the Yokohama release, the Federated ID Generation \(`com.glide.identity.globalid`\) plugin is auto-installed on all instances.

**Note:**

-   User name is required for generating Federated IDs.
-   User name and email are used to generate Federated IDs by default. To update the fields for generating Federated IDs based on your requirement, see [Updating ID fields](../task/updating-id-fields.md).
-   **iamsync\_admin** role is required to update the configuration.
-   If there are users with duplicate user names and email, then the Federated ID is generated only for one user. If the user name is null or empty, then the Federated ID is null.

![Federated ID in sys_user table](../images/federated-id-sys.png)

Schema changes after the plugin installed are as follows:

-   New column federated\_id in the `sys_user` table is created.
-   New table - `iamsync_type` is auto populated with the default configuration for the `sys_user` table.

Federated ID is only supported for the `sys_user` table and all the tables that extend the sys\_user table.

After upgrading to the Yokohama release, the Federated ID Generation \(`com.glide.identity.globalid`\) plugin is auto-installed on all instances.

\[/concept/conbody/section/ph/title \{"- topic/title "\}\)Federated ID for Roles\(title\]By using the `roles` of the user across the instances, the Federated ID is created and displayed in the **sys\_user\_role** table.

**Note:**

-   Role is required for generating Federated IDs in the **sys\_user\_role** table.
-   The Federated IDs in the **sys\_user\_role** table can be used to the over usages of the roles.
-   Updating ID fields and Regenerate Federated IDs options are not available for Role type. There's a scheduled job that runs periodically to generate ID for roles in case its empty.



