---
title: Generate a Case Report using a template
description: Use a predefined report template to generate case reports. These reports include post investigation report or an executive summary report.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/view-case-reports.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Generate a Case Report using a template

Use a predefined report template to generate case reports. These reports include post investigation report or an executive summary report.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## About this task

Generate case reports using predefined templates.

For information about generating a report using AI, see [Generate a Case Report using generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/na-tisc-generate-ai-reports.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select **Threat Analyst Workbench**.

3.  In **Case Management**, open the case to generate the report.

4.  Select the **Case Reports** tab.

    **Note:** You can delete the reports from the list, create a duplicate copy of the existing reports and customize your own report.

5.  Select **New with Template** as the report generation method.

    For information about generating a report using AI, see [Generate a Case Report using generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/na-tisc-generate-ai-reports.md).

6.  Select a report template from the list.

    The selected report template for the report type is generated. In the draft stage, the report viewing is restricted. As an analyst you can view the published reports but not the draft.

7.  Use the report editor to build the report content.

    -   Select the \[Omitted image "icon-tisc-report-edit.png"\] Alt text: Edit report details icon**Edit report details** icon to edit the report name and description.
    -   Select the \[Omitted image "icon-tisc-report-expand.png"\] Alt text: Expand icon**Expand** icon to insert additional content — for example, Observables or Indicators — into the report.
    -   Type `/` to use a slash command and insert dynamic content, such as a record count, a specific record or field, or a system user. For the available slash commands and supported tables, see [Working with Reports in TISC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-reports-lib-view.md).
    -   Select **Save Content** to save your changes and enable **Publish**.
    -   Select **Preview** to generate a PDF preview of the current content.
8.  When your edits are complete, select **Publish**.

    After publishing, download the report as a PDF or share it with stakeholders by email.


**Parent Topic:**[Threat Analyst Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/threat-analyst-workbench.md)

**Related topics**  


[Workbench Overview]()

[Creating cases using Threat Analyst Workbench]()

[Summarize a Case with Now Assist for Threat Intelligence Security Center]()

[Creating case task using Threat Analyst Workbench]()

[Working with Investigation Canvas]()

[Add artifacts to case\(s\) or case task\(s\)]()

[Run Enrichment Actions within a case]()

[Generate a Case Report using generative AI]()

[Create a security incident from a TISC case]()

[Upload Secure File Attachments]()

[Using playbooks]()

