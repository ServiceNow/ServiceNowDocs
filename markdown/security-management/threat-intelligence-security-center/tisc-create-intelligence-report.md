---
title: Create an intelligence report
description: Create an intelligence report from the Reports module in the Threat Intelligence Library by using a published intelligence template and populating it with intelligence from library lists and slash commands, independent of a case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/threat-intelligence-security-center/tisc-create-intelligence-report.html
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-06-23"
reading_time_minutes: 2
keywords: [Create Intelligence Reports, Generate Intelligence Reports]
breadcrumb: [Working with Reports in TISC, TISC Library Repository, Threat Intel Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Create an intelligence report

Create an intelligence report from the **Reports** module in the Threat Intelligence Library by using a published intelligence template and populating it with intelligence from library lists and slash commands, independent of a case.

## Before you begin

The intelligence report template must be published. For more information, see [Configure report templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/tisc-report-templates.md).

Role required: sn\_sec\_tisc.analyst

## About this task

Intelligence reports use templates that have an **Intelligence** report context. Unlike case reports, intelligence reports are independent of a case, and the editor does not display case-specific fields. The navigator displays all the lists from the Threat Intelligence Library, and you use record-selection tools and slash commands to add content. Only published templates are available for selection.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library**.

2.  Select **Reports** &gt; **Intelligence Reports**.

    The list of intelligence reports is displayed.

3.  Select **New Intelligence Report**.

4.  Enter a name for the report and select **Next**.

    **Note:** Intelligence reports do not require a case selection.

5.  Select the required intelligence report template.

    The report is generated and opens in an editable view in the **Report Content** tab.

6.  Select the **Report Content** tab to build the report content.

    -   Select the **Expand** icon to insert additional content — for example, Observables or Indicators — into the report.
    -   Type `/` to use a slash command and insert dynamic content, such as a record count, a specific record or field, or a system user. For the available slash commands and supported tables, see [Working with Reports in TISC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/tisc-reports-lib-view.md).
    -   Select **Save Content** to save your changes and enable **Publish**.
    -   Select **Preview** to generate a PDF preview of the current content.
    -   Select **Popout** to view or edit the report in a separate window.
7.  Select **Save Details** to save the report details.

8.  Select **Publish** to publish the report.

    **Important:** After publishing, the report is read-only. To download or share the report after editing, republish it.

    A confirmation message is displayed before the report is published.

9.  Select **Duplicate** from the overflow menu to create a copy of the report.

    **Note:** You can also duplicate reports from the list view. Duplicate reports are created in the Draft state.

10. After the report is published, download or share it.

    -   Select **Download** to download the published PDF.
    -   Select **Share** to share the report by email.

**Parent Topic:**[Working with Reports in TISC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/tisc-reports-lib-view.md)

