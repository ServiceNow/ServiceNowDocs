---
title: Customize a Vendor Management Workspace page using UI Builder
description: Clone an existing Vendor Management Workspace page variant and customize it based on your needs using the UI Builder.
locale: en-US
release: yokohama
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Vendor Management Workspace, Vendor Management Workspace, IT Service Management]
---

# Customize a Vendor Management Workspace page using UI Builder

Clone an existing Vendor Management Workspace page variant and customize it based on your needs using the UI Builder.

## Before you begin

Role required: admin, workspace\_admin, or ui\_builder\_admin

## About this task

All UI Builder pages and page variants are read-only. You can copy a page variant and then customize it. You can create a page variant from scratch or use a page template. For more information, see [Create a variant of a page](https://www.servicenow.com/docs/access?context=create-variant&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

**Note:** After you copy and customize a page variant, any automatic updates applied to the original read-only page variant will not be applied to the page variant that you have customized.

To open your configurable workspace experience in UI Builder, see [Open a Configurable Workspace experience in UI Builder](https://www.servicenow.com/docs/access?context=open-your-configurable-workspace-experience-in-ui-builder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)

For a list of all workspaces ServiceNow offers to target specific users, see [List of workspaces](https://www.servicenow.com/docs/access?context=list-of-workspaces&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **UI Builder**.

2.  In the UI Builder screen, select **Vendor Management Workspace**.

3.  In the **Page** menu, select the page you want to edit.

4.  In the **Variants** section, select the menu icon \(![Menu options icon](../../configurable-workforce-optimization-itsm/image/menu-icon.png)\) of the variant you would like to copy select **Duplicate**.

5.  In the variant that you've duplicated, select the menu icon \(![Menu options icon](../../configurable-workforce-optimization-itsm/image/menu-icon.png)\) and select **Edit page variant settings**.

6.  In the Edit settings pop-up window, do the following:

    -   In the **Variant name** field, enter a unique name for the variant.
    -   If you would like to use a different page template, in the **Page template** field, select the page template.
    -   Select **Save** to keep the changes.

        If you do not want to make any updates, select **Cancel** or select **Delete** to delete the variant.

7.  Select the menu icon \(![menu-icon](../../configurable-workforce-optimization-itsm/image/menu-icon.png)\) and select **Edit conditions**.

    -   To add or edit conditions for the variant, in the **Variant Conditions** field, add your preferred conditions for the variant.
    -   To display the variant in Vendor Management Workspace, in the **Order** field, set the preferred order number.
8.  Select **Done**.


**Related topics**  


[Configuring the Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-ui-admin&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)

