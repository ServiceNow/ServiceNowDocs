---
title: Customize a Workforce Optimization for ITSM page using the Next Experience UI Builder
description: Clone an existing Workforce Optimization for ITSM page and customize it based on your needs using the Next Experience UI Builder.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Advanced configurations, Workforce Optimization for ITSM, IT Service Management]
---

# Customize a Workforce Optimization for ITSM page using the Next Experience UI Builder

Clone an existing Workforce Optimization for ITSM page and customize it based on your needs using the Next Experience UI Builder.

## Before you begin

Role required: workspace\_admin or ui\_builder\_admin

## About this task

All Workforce Optimization for ITSM Next Experience UI Builder pages and page variants are read-only. You can copy a page variant and then customize it. You can create a page variant from scratch or use a page template. For more information, see [Create a variant of a page](https://www.servicenow.com/docs/access?context=create-variant&version=australia&pubname=australia-application-development&ft:locale=en-US).

**Note:** After you copy and customize a page variant, any automatic updates applied to the original read-only page variant will not be applied to the page variant that you have customized.

To open your configurable workspace experience in UI Builder, see [Open a Configurable Workspace experience in UI Builder](https://www.servicenow.com/docs/access?context=open-your-configurable-workspace-experience-in-ui-builder&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)

For a list of all workspaces ServiceNow offers to target specific users, see [List of workspaces](https://www.servicenow.com/docs/access?context=list-of-workspaces&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **UI Builder**.

2.  In the UI Builder screen, select **Manager Workspace**.

3.  In the **Page** menu, select the page you want to edit.

    For example, Landing Page or Work Scheduler.

4.  In the **Variants** section, select the menu icon \(![menu-icon](../image/menu-icon.png)\) of the variant you would like to copy select **Duplicate**.

5.  In the variant that you've duplicated, select the menu icon \(![menu-icon](../image/menu-icon.png)\) and select **Edit page variant settings**.

6.  In the Edit settings pop-up window, do the following:

    -   In the **Variant name** field, enter a unique name for the variant.
    -   If you would like to use a different page template, in the **Page template** field, select the page template.
    -   Select **Save** to keep the changes.

        If you do not want to make any updates, select **Cancel** or select **Delete** to delete the variant.

7.  Select the menu icon \(![menu-icon](../image/menu-icon.png)\) and select **Edit conditions**.

    -   To add or edit conditions for the variant, in the **Variant Conditions** field, and add your preferred conditions for the variant.
    -   To display the variant in Workforce Optimization for ITSM, in the **Order** field, set the preferred order number.
8.  Select **Done**.


**Parent Topic:**[Advanced configurations for Workforce Optimization for ITSM](../concept/advanced-configuration-workforce-optimization-itsm.md)

**Related topics**  


[Configuring the Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-ui-admin&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)

