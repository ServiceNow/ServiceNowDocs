---
title: Configure assignment groups, roles, and users using AI
description: Use the AI conversational experience in the Configuration Console to configure assignment groups, roles, and users for Hardware Asset Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/configure-team-using-ai.html
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-08-19"
reading_time_minutes: 3
breadcrumb: [Configuration Console for Hardware Asset Management, Configure, Hardware Asset Management, IT Asset Management]
---

# Configure assignment groups, roles, and users using AI

Use the AI conversational experience in the Configuration Console to configure assignment groups, roles, and users for Hardware Asset Management.

## Before you begin

-   The Hardware Asset Management \(HAM\) application must be installed on your ServiceNow instance. For details, see [Install Hardware Asset Management from Product Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/install-ham-from-product-hub.md).
-   The ServiceNow Otto for Hardware Asset Management \(HAM\) application must be installed on your ServiceNow instance. For details, see [Install additional HAM applications using Product Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/install-additional-ham-apps.md).
-   The ServiceNow Otto panel must be enabled on your ServiceNow instance. For details, see [Enable the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-center-enable-now-assist-panel.md).
-   AI Search must be activated on your ServiceNow instance. For details, see the AI Search activation steps in [Install ServiceNow Otto for Hardware Asset Management \(HAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/now-assist-for-hardware-asset-management/install-now-assist-ham.md).

Role required: To access the Configuration Console, you must have the ham\_admin and ia\_user roles. The setup items available within the console depend on the additional roles assigned. For more information on roles required for modules, see [Configuration Console for Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/config-console-ham.md).

## About this task

The Configuration Console includes a **Configure with AI** option that opens a conversation in the ServiceNow Otto panel. You can use this conversational interface to complete the following setup tasks without navigating to individual modules:

-   Configure assignment groups and roles
-   Import users into your ServiceNow instance

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  In the **Manage your products** section of the Admin Home page, select the **Hardware Asset Management** card to open the Product Hub.

3.  In the Configure your product section, select **Configure**.

    The Configure Hardware Asset Management page opens in the Configuration Console.

4.  Select **Configure with AI**.

    The ServiceNow Otto panel opens and displays the estimated time to complete the full configuration process.

5.  Select the task that you want to complete.

    -   Select **Start with Assignment groups \(Team management\)** to configure groups, assign users, assign roles, or search by org chart.
    -   Select **Choose something else** to view all available options, including groups, users, and roles.
6.  Based on your selection, follow the prompts in the panel.

<table id="choicetable_otq_dy3_hkc"><tbody><tr><td id="d326422e258">

**__Assignment groups \(Team management\)__ or __Roles \(Team management\)__**

</td><td>

Select one of the following options or enter a natural-language prompt: -   **Assign user\(s\) to a group**
-   **Assign user\(s\) to a role**
-   **Assign role\(s\) to a group**
-   **Create Group**
-   **Search by Org Chart**


</td></tr><tr><td id="d326422e294">

**__Users \(Team management\)__**

</td><td>

Select a data source \(File or LDAP\) and follow the prompts to import users into your ServiceNow instance.

</td></tr></tbody>
</table>7.  Respond to the follow-up questions and provide any additional information requested in the panel.

8.  Review the action summary and select the required action.

    -   **Yes**—Confirm the action.
    -   **Change details**—Modify the information you provided.
    -   **Cancel** — Cancel the action.
9.  When prompted for confirmation, select **Yes** to proceed or **No** to cancel.

10. When the assistant displays a success message, select the required option.

    -   **Do something else**: Return to the task selection to complete another configuration.
    -   **No further assistance**: End the conversation. The assistant then asks if you want to mark the step as configured.
11. When prompted, select how to proceed with the configuration step.

    -   To mark the step as complete immediately, select **Mark as configured**.
    -   To mark the step as complete later, select **Mark later** and return to the Configuration Console to complete this action manually.

## Result

-   The AI agents complete the requested configuration and create or update the relevant records in your ServiceNow instance.
-   Assignment group, users, and role configuration changes appear in the Team management module of the Configuration Console.

