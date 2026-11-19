---
title: Create a Case Report using a template
description: Generate a case report from a published report template, such as a post-investigation report or an executive summary, and then preview, publish, and share it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/threat-intelligence-security-center/tisc-create-case-report-template.html
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-06-24"
reading_time_minutes: 1
keywords: [Create Case Reports, Generate Case Reports using template]
breadcrumb: [Create Case Reports, Working with Reports in TISC, TISC Library Repository, Threat Intel Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Create a Case Report using a template

Generate a case report from a published report template, such as a post-investigation report or an executive summary, and then preview, publish, and share it.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library**.

2.  Select **Reports** &gt; **Case Reports**.

    Alternatively, select **Reports** &gt; **All Reports** or **Reports** &gt; **My Reports**.

3.  Select **New Case Report**.

4.  In the **Create New Case Report** window, enter the following details:

    1.  In **Case Number**, select the case number to generate the report.

    2.  In **Generation Method**, select **Using Template**.

5.  Select **Next**.

6.  Select the required report template to generate the report.

    The report opens in the editor, populated from the selected template.

7.  Use the report editor to build the report content.

    -   Select the \[Omitted image "icon-tisc-report-edit.png"\] Alt text: Edit report details icon**Edit report details** icon to edit the report name and description.
    -   Select the \[Omitted image "icon-tisc-report-expand.png"\] Alt text: Expand icon**Expand** icon to insert additional content — for example, Observables or Indicators — into the report.
    -   Type `/` to use a slash command and insert dynamic content, such as a record count, a specific record or field, or a system user. For the available slash commands and supported tables, see [Working with Reports in TISC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/tisc-reports-lib-view.md).
    -   Select **Save Content** to save your changes and enable **Publish**.
    -   Select **Preview** to generate a PDF preview of the current content.
8.  When your edits are complete, select **Publish**.

    After publishing, download the report as a PDF or share it with stakeholders by email.


**Parent Topic:**[Create Case Reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/tisc-create-case-report.md)

