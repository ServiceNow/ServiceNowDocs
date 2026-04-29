---
title: Configuring read-only security options
description: Control the ability to edit read-only fields by configuring read-only options.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing tables and indexes, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Configuring read-only security options

Control the ability to edit read-only fields by configuring read-only options.

Read-only fields are intended to restrict modifications in specific situations. In addition, the system provides configurable read-only options that enable you to customize the behavior of read-only fields according to your requirements, while balancing usability and security. You can adjust the read-only behavior by updating the **Read only option** field in a dictionary record.

## Available read-only options

-   **Instance Configured**

    Default **Read only option** value for read-only fields created prior to the Australia release. Used for maintaining backwards compatibility and testing read-only behavior in non-production instances.

    When the **Read only option** is set to Instance Configured in a dictionary record, read-only behavior is derived from the **glide.read\_only.legacy\_read\_only\_behavior** system property. By default, the property is set to client\_script\_modifiable, which honors the pre Australia read-only behavior, allowing changes to read-only fields through client scripts.

-   **Display Read Only**

    Displays the field as read-only in the UI, but allows changes to the read-only field through client scripts and server-side operations such as **TableAPI**, **GraphQL**, and **GlideRecordSecure\(\)**.

-   **Client Script Modifiable**

    Displays the field as read-only in the UI, and allows changes to read-only fields through client scripts but not through background scripts or server-side APIs like **TableAPI**, **GraphQL**, and **GlideRecordSecure\(\)**.

-   **Strict read only**

    Displays the field as read-only in the UI, but prevents any changes from both client scripts and server-side APIs.


## Testing read-only behavior

The Instance Configured read-only option maintains backwards compatibility for read-only fields created prior to the Australia release, and also enables you to test other read-only options on a non-production instance before implementing them on your production instance.

When the **Read only option** is set to Instance Configured, read-only behavior is determined by the **glide.read\_only.legacy\_read\_only\_behavior** system property. The default value for the **glide.read\_only.legacy\_read\_only\_behavior** system property is **client\_script\_modifiable**, which means the field appears as read-only in the UI, but can still be changed by a client script.

You can test read-only behavior on a non-production instance by updating the system property with the following values and then validating that your fields and client scripts work as expected.

-   **display\_read\_only**
-   **client\_script\_modifiable**
-   **strict\_read\_only**

**Important:** The **glide.read\_only.legacy\_read\_only\_behavior** system property is only intended for testing read-only behavior on non-production instances. Updating this property affects all fields where the **Read only option** field is set to Instance Configured.

For example, to verify that tighter security controls still work with your client scripts and other customizations, you can set the **glide.read\_only.legacy\_read\_only\_behavior** property to **strict\_read\_only** in a non-production instance, and then test the behavior. After you verify the behavior in a non-production instance, you can update individual fields on your production instance to use the Strict Read Only option on a field-by-field basis.

-   **[Test read-only options](../task/test-read-only-options.md)**  
Test read-only behavior on a non-production instance before updating **Read only option** field values on your production instance.
-   **[Make a field read only](../task/make-field-read-only.md)**  
Control whether a field is read only and whether it can be changed by a client script and server-side APIs.

**Parent Topic:**[Managing tables and indexes](using-table-administration.md)

