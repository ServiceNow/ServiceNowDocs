---
title: Upload the Microsoft 365 Copilot, Visio Online, and Project Online usage reports to your ServiceNow instance
description: Monitor the usage activity data for Microsoft 365 Copilot, Visio Online, and Project Online to identify reclamation candidates based on low usage.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrating with Microsoft 365, Microsoft 365 integration, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Upload the Microsoft 365 Copilot, Visio Online, and Project Online usage reports to your ServiceNow instance

Monitor the usage activity data for Microsoft 365 Copilot, Visio Online, and Project Online to identify reclamation candidates based on low usage.

## Before you begin

Role required:

-   Access the Microsoft 365 admin center: admin
-   Add reports to the ServiceNow instance: sam\_admin

## About this task

You can export the usage reports for Microsoft Copilot, Visio Online, and Project Online from the [Microsoft 365 admin center](https://admin.microsoft.com/#/homepage) and add the reports to your ServiceNow instance. These usage activity reports help in license optimization by identifying potential reclamation candidates based on low usage.

## Procedure

1.  Log in to [Microsoft 365 admin center](https://admin.microsoft.com/#/homepage) using your global administrator credentials.

2.  Navigate to **Reports** &gt; **Usage**.

3.  Download the usage reports.

    -   Select **Copilot for Microsoft 365** and download the CSV file by selecting **Export**.
    -   Select **Project** and download the CSV file by selecting **Export**.
    -   Select **Visio** and download the CSV file by selecting **Export**.
    **Important:** You must not change the names of the downloaded files. You must upload the files as is to your ServiceNow instance.

    You must upload the CSV files to your ServiceNow instance within 7 days for correctly identifying potential reclamation candidates.

4.  From the navigation menu, select **Identity**.

    The Azure portal for the current tenant opens.

5.  On the Overview page, copy the value in the **Tenant ID** field and save it for later use.

6.  From a web browser, open your ServiceNow instance.

<table id="choicetable_yzk_rml_bcc"><thead><tr><th align="left" id="d285372e211">

Interface

</th><th align="left" id="d285372e214">

Action

</th></tr></thead><tbody><tr><td id="d285372e220">

**Core UI**

</td><td>

Open the Integration Profiles \[samp\_sw\_subscription\_profile\] table.Integration profiles open in the list view.

</td></tr><tr><td id="d285372e232">

**Software Asset Workspace**

</td><td>

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace** &gt; **License operations**.
2.  Under **User subscription**, select **Direct integration profiles**.


</td></tr></tbody>
</table>7.  Apply filters to open integration profiles for a specific Tenant id for which you want to upload the usage reports.

<table id="choicetable_np5_wnl_bcc"><thead><tr><th align="left" id="d285372e278">

Interface

</th><th align="left" id="d285372e281">

Action

</th></tr></thead><tbody><tr><td id="d285372e287">

**Core UI**

</td><td>

1.  Select the Show/hide filter icon on the table header.
2.  Set the condition **\[Tenant name or id\] \[is\] \[Tenant ID copied in step 5\] AND \[Profile type\] \[is\] \[Microsoft 365\]**.
3.  Select **Run**.


</td></tr><tr><td id="d285372e315">

**Software Asset Workspace**

</td><td>

1.  Select the filter icon and then select **Advanced view**.
2.  Set the condition **\[Tenant name or id\] \[is\] \[Tenant ID copied in step 5\]**.
3.  Add a filter condition by selecting **+ New condition set**.
4.  Set the condition **\[Profile type\] \[is\] \[Microsoft 365\]**.
5.  Select **Update**.


</td></tr></tbody>
</table>8.  Add the usage reports to an integration profile.

<table id="choicetable_my4_mcm_bcc"><thead><tr><th align="left" id="d285372e367">

Interface

</th><th align="left" id="d285372e370">

Action

</th></tr></thead><tbody><tr><td id="d285372e376">

**Core UI**

</td><td>

1.  Select an integration profile.
2.  Select the Manage Attachments ![Manage attachments icon.](../image/manage-attachments-icon.png) icon on the form header.
3.  In the Attachments dialog box, select **Choose file**.
4.  Select all the CSV files that you downloaded in step 3 to add them to the integration profile.
5.  Close the dialog box to return to the Integration Profile form.
6.  The uploaded CSV files appear next to the Manage Attachments icon.


</td></tr><tr><td id="d285372e415">

**Software Asset Workspace**

</td><td>

1.  Select an integration profile.
2.  Select the Attachment ![Manage attachments icon.](../image/manage-attachments-icon.png) icon from the sidebar of the integration profile.
3.  In the Attachments window, select **Select file**.
4.  Select all the CSV files that you downloaded in step 3 to add them to the integration profile.
5.  The uploaded CSV files appear in the Attachment window.


</td></tr></tbody>
</table>
## What to do next

The usage activity reports that you uploaded can be monitored for license optimization and generation of reclamation candidates. For details, see [Evaluating software usage activity for Microsoft 365 subscriptions](../concept/o365-usage-activity.md).

