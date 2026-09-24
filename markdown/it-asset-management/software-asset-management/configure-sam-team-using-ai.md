---
title: Configure groups and users using AI
description: Use the AI conversational experience in the Configuration Console to configure groups and users for Software Asset Management. This approach allows you to complete multiple setup tasks through a single interface without navigating to individual modules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/configure-sam-team-using-ai.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Software Asset Management, Groups, Users, ServiceNow Otto]
breadcrumb: [Configure SAM using AI, Configure SAM using Configuration Console, Configuration Console for Software Asset Management, Software Asset Management installation methods, Configuring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Configure groups and users using AI

Use the AI conversational experience in the Configuration Console to configure groups and users for Software Asset Management. This approach allows you to complete multiple setup tasks through a single interface without navigating to individual modules.

## Before you begin

-   The Software Asset Management application must be installed on your ServiceNow instance. For details, see [Install Software Asset Management from the Product Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/install-sam-product-hub.md).
-   The ServiceNow Otto for Software Asset Management \(SAM\) application must be installed on your ServiceNow instance. For details, see [Install ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/install-now-assist-sam.md).
-   The ServiceNow Otto panel must be enabled on your ServiceNow instance. For details, see [Enable the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-enable-now-assist-panel.md).
-   AI Search must be activated on your ServiceNow instance. For details, see the AI Search activation steps in [Install ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/install-now-assist-sam.md).

Role required: admin

## About this task

Groups organize the users that are responsible for day-to-day Software Asset Management operations and receive the notifications that support those operations. The Users page sets up the users who work with Software Asset Management and assigns the roles that establish their access and capabilities. The Configuration Console includes a **Configure with AI** option that opens a conversational interface. You can use this interface to complete the following setup tasks without navigating to individual modules:

-   Configure groups and roles
-   Import users into your ServiceNow instance

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  In the **Manage your products** section of the Admin Home page, select the **Software Asset Management** card to open the Product Hub.

3.  In the Configure your product section, select **Configure**.

    The Configure Software Asset Management page opens in the Configuration Console.

4.  Select **Configure with AI**.

    The ServiceNow Otto panel opens and displays the estimated time to complete the full configuration process.

5.  Select the task that you want to complete.

    -   To configure groups, assign users, assign roles, or search by org chart, select **Start with Assignment groups \(Team management\)**.
    -   To view all available options, including groups, users, and roles, select **Choose something else**.
6.  Follow the prompts in the panel based on your selection in the previous step.

<table id="choicetable_follow_prompts"><thead><tr><th align="left" id="d268511e250">

If you selected

</th><th align="left" id="d268511e253">

Do this

</th></tr></thead><tbody><tr><td id="d268511e259">

**__Start with Assignment groups \(Team management\)__**

</td><td>

Select one of the following options or enter a natural-language prompt: -   **Assign user\(s\) to a group**
-   **Assign user\(s\) to a role**
-   **Assign role\(s\) to a group**
-   **Create Group**
-   **Search by Org Chart**


</td></tr><tr><td id="d268511e292">

**__Choose something else__**

</td><td>

Select **Groups \(Team management\)** or **Users \(Team management\)**, and then follow the prompts. For **Users \(Team management\)**, select a data source \(File or LDAP\) to import users into your ServiceNow instance.

</td></tr></tbody>
</table>7.  Respond to the follow-up questions and provide any additional information requested in the panel.

8.  Review the action summary and select the required action.

    -   **Yes**: Confirm the action.
    -   **Change details**: Modify the information you provided.
    -   **Cancel**: Cancel the action.
9.  When prompted for confirmation, select **Yes** to proceed or **No** to cancel.

10. Select one of the following options after the AI assistant displays a success message:

    The success message appears only when you select **Yes** in the previous step.

    -   **Do something else**: Return to the task selection to complete another configuration.
    -   **No further assistance**: End the conversation. The AI assistant then asks whether to mark the step as configured.
11. When the AI assistant asks whether to mark the step as configured, select one of the following options:

    -   **Mark as configured**: Mark the step as complete immediately.
    -   **Mark later**: Mark the step as complete later and return to the Configuration Console to complete this action manually.

## Result

The AI assistant completes the requested configuration and creates or updates the relevant records in your instance. Group and user configuration changes appear in the Team management module of the Configuration Console.

**Parent Topic:**[Configure Software Asset Management using AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown)

