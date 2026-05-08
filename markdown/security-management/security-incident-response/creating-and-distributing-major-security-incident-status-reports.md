---
title: Create and distribute MSIM Status Reports
description: As a Major Security Incident \(MSI\) manager, you can create and distribute the different status reports to different stakeholders at various intervals based on the configured report template or a previous status report throughout the course of the major security incident resolution.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Use, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create and distribute MSIM Status Reports

As a Major Security Incident \(MSI\) manager, you can create and distribute the different status reports to different stakeholders at various intervals based on the configured report template or a previous status report throughout the course of the major security incident resolution.

## Before you begin

Role required: sn\_msi.workspace\_manager

You can preview the previously configured summary report data elements, add additional text or summary, remove individual report components as needed, and verify the accuracy and completeness of the report before distributing it to different stakeholders.

Create the status reports by selecting the desired report template that was initially configured on the MSI Report Templates Setup page.

## Procedure

1.  Navigate to **Workspaces** &gt; **Major Security Incident Management** &gt; **Major Security Incidents**.

2.  Select the **Lists** view.

3.  Select the respective promoted MSI record.

4.  Select the **Status Reports** tab.

    The Status Reports tab contains three different types of subsections such as below.

<table id="table_v3s_4cq_d1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Report Name

</td><td>

Name of the status report template.**Note:** The Status Reports view lists the existing predefined report templates that are available as a part of the base system for the concerned persona. For example, Executive Status Reports through email \(Mobile-friendly\), Technical Status Reports and Executive Status Reports as PDFs.

</td></tr><tr><td>

Updated

</td><td>

The date when the report template was last updated.

</td></tr><tr><td>

Report Type

</td><td>

Type of status report. The status report can be in one of the following types:-   PDF
-   Email


</td></tr><tr><td>

State

</td><td>

State of the status reports. The status reports can be in one of the following states:-   Draft
-   Queued
-   Published


</td></tr></tbody>
</table>5.  Select the type of the status report that you would want to view or select **New** to create a status report.

    ![Create and distribute MSIM Status Reports](../image/msim-status-reports-tab.png "MSIM Status Reports tab")

6.  Choose one of the following status report types from the list.

    -   **Executive** Email Status Reports that are mobile-friendly.
    -   **Technical Status Report** PDF
    -   **Executive Status Report** PDF
    **Note:** When you select any desired report template, the preview of the selected report is immediately generated in the right-pane. You can view the selected status report of the MSI.

7.  On the Executive Email Status Report template, fill the sections with the details of the status report.

<table id="choicetable_lfv_mkq_d1c"><thead><tr><th align="left" id="d309639e249">

Report section

</th><th align="left" id="d309639e252">

Description

</th></tr></thead><tbody><tr><td id="d309639e258">

**Updates**

</td><td>

Provide a summary of the status update. This section contains the following:-   **MSI Summary**: Provide a brief summary of the major security incident.
-   **Append text from last report shared**: Select this option to append the text from the last report shared.


</td></tr><tr><td id="d309639e280">

**Explanation**

</td><td>

Add an explanation on what has changed since the last status update was done. This section contains the following:-   **Key updates**: Provide key updates like what the security team should know about the major security incident, name the key events that took place, and list any pending actions.
-   **Next Update**: Provide the date and time of the next update for resolving the major security incident. For example, 5:00 pm EST on March 25th, 2024.
-   **Append text from last report shared**: Select this option to append the text from the last report shared.
-   **Filter elements**: Select the report elements to be included in the report. For example, Key Updates or Next Updates.


</td></tr><tr><td id="d309639e312">

**Additional Information**

</td><td>

Provide specific details relevant to the status update.

</td></tr><tr><td id="d309639e321">

**Visualizations**

</td><td>

Select the visualizations that best help communicate the status update. -   **Incident Impact**: Select the Incident Impact metrics like Affected Assets, Affected Location, Affected Users that are related to the status update.
-   **Filter elements**: Select the report elements to be included in the report. For example, Incident Impact.


</td></tr><tr><td id="d309639e344">

**Lists**

</td><td>

Select lists of records that provide context to the status update.-   **Linked records**: Select the records that are linked to the major security incident status update. For example, Linked Security Incident.
-   **Filter elements**: Select the report elements to be included in the report. For example, Linked records.


</td></tr></tbody>
</table>    **Note:** The options that you’ve selected from the Status Reports section are the same options that are rendered in the Preview report.

    ![Status Report Template](../image/msim-status-report-template.png "Status Report Template")

8.  Select **Save** to save the updates you made to the status report.

9.  Select **Share** to share the status report with internal and external stakeholders.

    The Share dialog box appears. Fill in the fields in the dialog box:

<table id="table_ppn_bnj_k3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Subject

</td><td>

Subject for the email report.

</td></tr><tr><td>

To, Cc, Bcc

</td><td>

Fields to add the email recipients. Emails can be added using one or more of the following:-   Select individual users or groups from drop-down lists.
-   Manually enter email addresses into any of the recipient field.
-   Copy and paste multiple comma-separated or semicolon-separated email addresses.
-   Copy and paste existing distribution lists.
**Note:** Recipient fields \(To, Cc, and Bcc\) are automatically populated with recipients from the most recently sent status report using the same template, eliminating the need to add recipients for recurring status report communications.

</td></tr><tr><td>

Remove Invalid Recipients

</td><td>

Option to remove all the invalid email addresses. This field appears only when there are invalid email addresses in a recipient field.**Note:** Invalid email addresses are highlighted with an error icon.

</td></tr><tr><td>

Clear ALL Recipients

</td><td>

Option to clear the all the recipients fields simultaneously. This field is enabled only when there is at least one email address in any of the recipient fields.

</td></tr><tr><td>

Body

</td><td>

Body of the email message.

</td></tr></tbody>
</table>10. Select **Email Report**.

    An email with the attached PDF Status Report is successfully sent to the concerned recipient for them to verify.

    ![Report email](../image/email-report.png "Status Report - email")

11. You can also perform the following actions on the Status Reports tab:

    1.  Use the **Refresh** action on the Status Reports view to refresh the status reports list.

    2.  Use the **List Actions** action on the Status Reports view to edit columns or reset the widths of the status reports list.

    3.  Use the **Filter** action on the Status Reports view to filter the status reports based on certain conditions.


**Parent Topic:**[Using Major Security Incident Management](../../security-incident-response/concept/major-security-incident-setup.md)

**Related topics**  


[Propose, promote, and link incident records](../../security-incident-response/concept/promoting-sir-to-msim.md)

[Using MSI List view in the MSIM workspace](../../security-incident-response/task/list-view-in-msim.md)

[View Major Security Incident impact metrics](../concept/viewing-trend-charts-and-progress-of-msi.md)

[View Major Security Incident trend charts](../concept/viewing-msi-impact-metrics.md)

[Update Major Security Incident details](../concept/msim-details-tab.md)

[Link additional records to Major Security Incident](linking-additional-records-to-major-security-incidents.md)

[Unlink records from Major Security Incident](unlinking-msi-records.md)

[Manage tasks in a Major Security Incident](../concept/tasks-tab.md)

[Track collaboration activity via MSIM workspace](../concept/collab-tab.md#)

[Configure Major Security Incident status reports](../concept/manage-status-reports-for-major-security-incident-management.md)

