---
title: Create a Case Report using generative AI
description: Use generative AI to draft a structured case report from the data in the selected case, then review and publish it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-create-case-report-ai.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 2
keywords: [Create Case Reports, Generate Case Reports using AI]
breadcrumb: [Create Case Reports, Working with Reports in TISC, TISC Library Repository, Threat Intel Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Create a Case Report using generative AI

Use generative AI to draft a structured case report from the data in the selected case, then review and publish it.

## Before you begin

Generative AI driven report generation is available only when the following prerequisites are met:

-   Threat Intelligence security center-Advanced \[sn\_ai\_tisc\_adv\] is installed.
-   The TISC Report Authoring skill is active.
-   AI report styling must be configured by the Threat Intelligence administrator \(sn\_sec\_tisc.admin\). For more information, see [Configure report styling for TISC Case reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/configure-report-styling-tisc.md).

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library**.

2.  Select **Reports** &gt; **Case Reports**.

    Alternatively, select **Reports** &gt; **All Reports** or **Reports** &gt; **My Reports**.

3.  Select **New Case Report**.

4.  In the **Create New Case Report** window, enter the following details:

    1.  In **Case Number**, select the case number to generate the report.

    2.  In **Generation Method**, select **Using AI**.

5.  Select **Next**.

6.  In **Report type**, enter the type of report you want to generate or save for future usage.

    The report types are saved for the current user and listed under **Saved Report Types**.

7.  In **Report description**, enter a brief description in a maximum of 500 characters of how AI should generate the report.

    **Tip:** The fields contain default values to help you understand the Report Authoring feature.

8.  To reuse the report later, select **Save Report Type**.

    You can save up to 10 report types per user. When you reach the limit, delete a saved report type before saving a new one.

    To modify a saved report type, select **Save Changes** or save it as a new report type, select **Save as New**.

    Use the search bar under **Saved Report Types** to find a saved report type.

9.  Select **Generate report**.

    A loading indicator appears for up to five seconds.

    -   If the report generates within five seconds, the window closes and the report editor opens automatically.
    -   If it takes longer, the window closes and a notification appears in the list view. The report editor opens when the report is ready.
10. Use the report editor to build the report content.

    -   Select the \[Omitted image "icon-tisc-report-edit.png"\] Alt text: Edit report details icon**Edit report details** icon to edit the report name and description.
    -   Select the \[Omitted image "icon-tisc-report-expand.png"\] Alt text: Expand icon**Expand** icon to insert additional content — for example, Observables or Indicators — into the report.
    -   Type `/` to use a slash command and insert dynamic content, such as a record count, a specific record or field, or a system user. For the available slash commands and supported tables, see [Working with Reports in TISC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-reports-lib-view.md).
    -   Select **Save Content** to save your changes and enable **Publish**.
    -   Select **Preview** to generate a PDF preview of the current content.
11. When your edits are complete, select **Publish**.

    After publishing, download the report as a PDF or share it with stakeholders by email.


**Parent Topic:**[Create Case Reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-create-case-report.md)

