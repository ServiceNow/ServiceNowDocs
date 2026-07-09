---
title: Generate a Case Report using generative AI
description: Generate an AI-based, structured, threat intelligence case report from the data in a case and export it for stakeholder distribution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/na-tisc-generate-ai-reports.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 4
breadcrumb: [Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Generate a Case Report using generative AI

Generate an AI-based, structured, threat intelligence case report from the data in a case and export it for stakeholder distribution.

## Before you begin

**Important:** Some generative AI skills, AI agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Generative AI driven report generation is available only when the following prerequisites are met:

-   Threat Intelligence Security Center-Advanced must be installed.
-   TISC Report Authoring skill must be active.
-   AI report styling must be configured by the Threat Intelligence administrator \(sn\_sec\_tisc.admin\). For more information, see [Configure report styling for TISC Case reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/configure-report-styling-tisc.md).

Role required: sn\_sec\_tisc.analyst

## About this task

Generate an AI-based, structured, threat intelligence case report from the data in a case.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the **Threat Analyst Workbench** icon.

3.  In **Case Management**, open the case to generate the report.

4.  Select the **Case Reports** tab.

5.  Select **New with AI**.

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


**Parent Topic:**[Threat Analyst Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/threat-analyst-workbench.md)

**Related topics**  


[Workbench Overview]()

[Creating cases using Threat Analyst Workbench]()

[Summarize a Case with Now Assist for Threat Intelligence Security Center]()

[Creating case task using Threat Analyst Workbench]()

[Working with Investigation Canvas]()

[Add artifacts to case\(s\) or case task\(s\)]()

[Run Enrichment Actions within a case]()

[Generate a Case Report using a template]()

[Create a security incident from a TISC case]()

[Upload Secure File Attachments]()

[Using playbooks]()

