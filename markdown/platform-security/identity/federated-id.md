---
title: Exploring Federated ID
description: The ServiceNow Identity system deduplicates users across multiple instances using their User ID and email, and assigns each resolved user a unique Federated ID for consistent identification.
locale: en-US
release: australia
product: Identity
classification: identity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Global Identity, Identity]
---

# Exploring Federated ID

The ServiceNow® Identity system deduplicates users across multiple instances using their User ID and email, and assigns each resolved user a unique Federated ID for consistent identification.

With Federated ID, you can accurately calculate the number of unique users across instances, which is useful for licensing and user management. For more information, see [Federated ID](federated-id.md).

**Note:** User name is required for generating Federated IDs.

With the user’s **User ID** and **Email** \(default setting\) to identify and match users across instances, ServiceNow® generates a Federated ID unique identifier with a hashing function and stores it in the **sys\_user** table.

**Note:**

-   **User ID** is required for generating Federated IDs. If the user name is null or empty, then the Federated ID is null.
-   **User ID** and **Email** are used to generate Federated IDs by default. To configure the fields used for generating Federated IDs based on your requirements, see [Updating ID fields](../task/updating-id-fields.md). The**Iamsync\_admin** role is required to update the configuration.
-   If multiple users share the same username and email, the system generates a Federated ID for only one of the users.

![Federated ID in sys_user table](../images/federated-id-sys.png)

After upgrading to the Australia release, the Federated ID Generation \(**com.glide.identity.globalid**\) plugin is auto-installed on all instances. Once the plugin is installed, the schema changes are as follows:

-   A column **federated\_id** in the **sys\_user** table is created.
-   A table - **iamsync\_type** is auto populated with the default configuration for the **sys\_user** table.

Federated ID is only supported for the **sys\_user** table and all the tables that extend the **sys\_user** table.

