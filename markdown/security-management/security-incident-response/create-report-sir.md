---
title: Create a report
description: Analysts can create a report in Security Incident Response to include the status of an incident and share it via email.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-16"
reading_time_minutes: 1
breadcrumb: [Reports in Security Incident Response, Working with Security Incident Records, Using SIR Workspace, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a report

Analysts can create a report in Security Incident Response to include the status of an incident and share it via email.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Open a security incident.

3.  Select **Reports**.

    The **Report** page displays a list of all the reports created for the selected incident.

4.  Select **New**.

    The **Select Template** page appears with a list of all the published templates. The list of templates is available only when the admin has published reports templates. For more information, see [Create a Report Template in Security Incident Response](create-report-template-sir.md).

5.  Select a report template.

    The report opens in edit mode with the incident data as configured in the template.

6.  Select **Expand** and insert/remove the desired fields.

    -   **Common SIR Fields**: The list of most used fields for an incident.
    -   **All SIR Fields**: All the fields related to an incident. For example, when you are generating a incident report and want to add a field called Short description then you can select that field from the **All SIR Fields**. When you add a field, the short description if the incident is displayed in the report.
    -   **Related Records**: The related records of a particular incident. For example, if you want to add any associated observables in the report, you can add it to your report. These related records are displayed in the table format
    -   **Scripts**: To add the date and time of the report, you can add the Current Date Time script to your report. This will add the Report Created Date and Time in report.
7.  Select **Preview** to view a preview of the report.

8.  Select **Save Content** to save the changes.

9.  Select the edit report details icon to update the report name and description.

10. Select **Publish** to publish the report.

11. Select the share report in email icon.

    1.  Enter the recipient’s emails in the **To** and **Cc/Bcc** fields.

    2.  Update the email **Subject and Email Body**.

    3.  Select **Send** to share the report over email.


**Parent Topic:**[Reports in Security Incident Response](../concept/report-templates-sir.md)

