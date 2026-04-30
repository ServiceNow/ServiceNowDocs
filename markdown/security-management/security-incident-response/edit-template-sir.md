---
title: Edit a report template in Security Incident Response
description: Edit a report template to reuse an existing template to create a new template.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure report templates in Security Incident Response, Configure, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Edit a report template in Security Incident Response

Edit a report template to reuse an existing template to create a new template.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspaces** &gt; **Administration**.

2.  Select **Reports**, and then **Report Templates**.

    The Report Templates page appears with all the templates available in the base system.

3.  Select the template.

    Displays the **Details** tab of the template in edit mode.

4.  Update the name and description of the template.

5.  Select **Save**.

6.  Select **Content** tab.

    Displays the content page of the template with a blank report.

7.  Select **Expand** and insert/remove the desired fields.

    -   **Common SIR Fields**: The list of most used fields for an incident.
    -   **All SIR Fields**: All the fields related to an incident. For example, when you are generating a incident report and want to add a field called Short description then you can select that field from the All SIR Fields. The Short description field is added as a variable in the report template. When you generate a report for the analyst, the short description if the incident is displayed in the report.
    -   **Related Records**: The related records of a particular incident. For example, if you want to add any associated observables in the report, you can add it to your report template. These related records are displayed in the table format
    -   **Scripts**: To add the date and time of the report, you can add the Current Date Time script to your report template. This will add the Report Created Date and Time in report.
8.  Select **Save Content** to save the contents of your report template.

9.  Select **Preview** to preview your report format.

    After you add all the required fields to you report template, you need publish your report template.

10. Select **Publish** to publish the template.

    A confirmation message is displayed whether you want to publish the report template.


**Parent Topic:**[Configure report templates in Security Incident Response](../concept/daily-status-sir.md)

