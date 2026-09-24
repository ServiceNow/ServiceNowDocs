---
title: Configure a CRM Workspace list
description: List categories and lists enable agents and managers to quickly find records. Configure a list to display the right information for your intended audience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/config-csm-config-ws-lists.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Set up CRM Workspace, CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure a CRM Workspace list

List categories and lists enable agents and managers to quickly find records. Configure a list to display the right information for your intended audience.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

You can configure the baseline lists and list categories as needed: create or delete list categories and lists and adjust the display order. For each list, you can also select the columns that are visible and specify the intended audience.

## Procedure

1.  Navigate to the UX List Menu Configurations list by entering **sys\_ux\_list\_menu\_config.LIST** in the application navigator and pressing **Enter**.

2.  Select the **CRM Workspace List Menu Config**.

    You can use the UX List Categories and UX Lists related lists to update your categories and lists as needed. The following steps walk you through the process of creating a list.

3.  In the UX Lists related list, select **New**.

4.  Fill out the fields on the UX List record and select **Save**.

5.  To select an audience for the list, navigate to **All** &gt; **Now Experience Framework** &gt; **Building Blocks** &gt; **Audiences**.

6.  Create an audience for your list if one doesn't already exist.

7.  Associate the audience to the list.

    1.  Navigate to the List Applicabilities list by entering **sys\_ux\_applicability\_m2m\_list.LIST** in the application navigator and pressing **Enter**.

    2.  Select **New** to create a List Applicability record.

    3.  Select a list in the **List** field.

    4.  Select an audience in the **Applicability** field.

    5.  Select **Submit**.

    **Note:**

    -   The system does not display list categories that don't have one or more associated lists.
    -   The **Order** field determines the order in which list categories and lists are displayed.

