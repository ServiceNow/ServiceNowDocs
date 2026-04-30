---
title: Activate a playbook page or page variant
description: Activate a playbook page or page variant and set the page order. The system uses the active page with the lowest order number to display records in CSM Configurable Workspace.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Playbook pages, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Activate a playbook page or page variant

Activate a playbook page or page variant and set the page order. The system uses the active page with the lowest order number to display records in CSM Configurable Workspace.

## Before you begin

Role required: ui\_builder\_admin, admin

Some playbook pages and page variants are not active by default. You need to activate the pages and set the page order before using the pages in CSM Configurable Workspace.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  In the Experiences list, select **CSM/FSM Configurable Workspace**.

3.  Find one of the following pages by scrolling through the Pages and variants list to the Record section:

    -   Case playbook: horizontal stages
    -   Case playbook: vertical stages
    -   Complaint case process page
    -   Onboarding case process page
    -   Product Support process page
    **Note:** These pages may be marked as **Inactive**.

4.  Display the page settings by selecting **Settings** for the desired page or page variant.

5.  Activate the page by selecting the **Active** check box.

6.  In the **Order** field, set the order number for the page.

    Each page has an order number. The page with the lowest order number is the default page. When the system displays a record in CSM Configurable Workspace, it uses this default page to display the record information. For more information, see [Set record page order](config-csm-ws-set-record-page-order.md).

7.  In the **Variant conditions** field, specify the table value.

    Add the table values for the case types where you want to see this page variant.

8.  Select **Save**.


**Related topics**  


[Create a page from a template](https://www.servicenow.com/docs/access?context=reuse-page-definitions&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)

[Edit a page](https://www.servicenow.com/docs/access?context=edit-page&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)

[Create a page variant](https://www.servicenow.com/docs/access?context=create-variant&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)

[Edit page variant settings](https://www.servicenow.com/docs/access?context=edit-variant-settings&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)

