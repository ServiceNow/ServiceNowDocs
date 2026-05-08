---
title: Retire or archive a specification version
description: Move a published specification version to a Retired or Archived state when the version is no longer in use or being sold to your customers. When you retire a specification version, you can't use it in a product offering or create a specification version.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-07"
reading_time_minutes: 1
breadcrumb: [Retiring or archiving versioned specifications and product offerings, Configuring product offerings and catalogs, Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Retire or archive a specification version

Move a published specification version to a Retired or Archived state when the version is no longer in use or being sold to your customers. When you retire a specification version, you can't use it in a product offering or create a specification version.

## Before you begin

Role required: admin

## About this task

You can maintain only one active version of the specification. When you retire or archive a specification version, you can't do the following actions:

-   Update the specification version.
-   Use it to create other catalog entities or rules such as product offerings, specification relationships, attribute mappings, or decomposition rules.

You retire or archive service and resource specification versions in the same manner.

**Note:** To archive a specification version, you must first retire it.

## Procedure

1.  Open CSM Configurable Workspace.

2.  Navigate to **List** &gt; **Specifications** &gt; **Product Specifications**.

3.  Select a record you want to modify.

4.  Navigate to the **Versions \(n\)** tab to view the previous versions that are related to this specification.

    Here, n represents the number of base and previous versions for this specification. For detailed information about the field descriptions, see Specification Versions form.

5.  Retire or archive one or more specification versions.

    1.  To retire a previous specification version, select the checkbox next to the Number column, and then select **Retire**.

        Validations ensure that the specification version is not being used in other active specifications or product offerings. If it's being used in a published specification or product offering, the following message appears:

        ```
        Selected specification(s) will be changed from Published to Retired state. This could affect published specifications/product offerings.Are you sure you want to archive the selected specification(s).
        ```

        To retire this specification, select **Retire**.

    2.  To archive a previous specification version, select the checkbox next to the Number column, and then select **Archive**.

    When you retire a specification, its state changes to Retired. After you retire a specification, you can't make any changes to it, use it in a product offering, or create specification versions for it.


