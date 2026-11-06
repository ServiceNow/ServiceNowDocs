---
title: CSM centered chat interaction record page settings
description: The CSM centered chat interaction record page includes several default settings, including the audience and conditions that determine when the record page is displayed in CRM Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/centered-chat-page-settings.html
release: australia
topic_type: reference
last_updated: "2026-10-19"
reading_time_minutes: 1
breadcrumb: [CSM centered chat interaction record page, Record pages, Record pages and page templates, CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM centered chat interaction record page settings

The CSM centered chat interaction record page includes several default settings, including the audience and conditions that determine when the record page is displayed in CRM Workspace.

<table id="table_zqv_lvv_q1c"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Selecting the **Active** check box makes the page variant available to the selected audience. The CSM centered chat interaction record page variant is active by default.The active setting combined with the page order determines the page that CRM Workspace uses to display record information. For more information, see [Set record page order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/config-csm-ws-set-record-page-order.md).

</td></tr><tr><td>

Order

</td><td>

Each record page has an order which indicates the page priority. The lower the number, the higher the priority.The default order for the CSM centered chat interaction record page variant is -2000.

</td></tr><tr><td>

Conditions

</td><td>

Conditions determine when a page variant is displayed. The CSM centered chat interaction record page variant has the following conditions:-   **table = interaction**: Limits the use of the CSM centered chat interaction page variant to records from the Interaction \[interaction\] table.
-   **csm.isChatCenteredInteractionVisible = true**: Stores the result of the system's evaluation of the UX Page property that determines user roles.

If these conditions are met, the system displays the CSM centered chat interaction record page variant.

</td></tr><tr><td>

Audience

</td><td>

The audience determines who can see the page variant. The CSM centered chat interaction record page has the following audience: **CSM - Front-line Agent**.This audience includes the sn\_cwf\_wrkspc.frontline\_agent role.

By default, agents who belong to the **CSM - Front-line Agent** audience will see the CSM centered chat interaction record page in CRM Workspace. This is the default for both new \(zboot\) and upgrade customers.

For more information, see [Learn about audiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/add-audiences.md).

</td></tr></tbody>
</table>## Accessing the record page settings

To access the settings for the CSM centered chat interaction record page:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Select the **CRM Workspace** experience.
3.  In the Record section of the Pages and variants list, select **CSM centered chat interaction page**.
4.  Select **Settings** at the top of the page.

