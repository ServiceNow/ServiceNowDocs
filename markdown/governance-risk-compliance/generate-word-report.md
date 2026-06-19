---
title: Generate a Microsoft Word report
description: Generate customized Microsoft Word reports for different records using Microsoft Word templates. This functionality enables you to streamline reporting in a standardized format.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/generate-word-report.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Generating Microsoft Word reports using Document designer, Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Generate a Microsoft Word report

Generate customized Microsoft Word reports for different records using Microsoft Word templates. This functionality enables you to streamline reporting in a standardized format.

## Before you begin

Role required: sn\_dri\_inc\_rptg.digital\_resilience\_incident\_manager \(The Reporting Configurations module in DRIR requires this role for generating reports\)

## Procedure

1.  Navigate to **All** &gt; **Operational Resilience** &gt; **Operational Resilience Workspace**.

2.  Open a record, such as an action task, from the list view.

3.  To generate the report in Microsoft Word format, select **...** and select **Generate MS Word** in the record view.

    \[Omitted image "d3-gen-word-ui-action.png"\] Alt text: Generate MS Word UI action.

    The Generate report window is displayed.

4.  From the Generate report window, select the action task report template from the Template list \(only Published templates appear\) and enter a Name for the report.

5.  Select **Generate**.

    The action task report is generated in the Microsoft Word format. It includes information from the **Details** and **Assessments** tabs and attachments. It includes information such as form sections, questions, template sections, question answers, and attachment links as shown in the examples.

    \[Omitted image "word-rep-1.png"\] Alt text: Contents of the Microsoft Word report.\[Omitted image "word-rep-2.png"\] Alt text: Fields in the Microsoft Word report.

    For information on Microsoft Word templates and Template configurations, see [Generating Microsoft Word reports using Document designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/gen-word-reports.md).

    The generation of Microsoft Word reports, required by the authorities for analysis in Digital resilience incident reporting, is completed with this step.

6.  Navigate to the attachment section of the record and view the report listed in the Activity section.

    The report is generated in Microsoft Word format and it is displayed in the Activity section of the record.

7.  Download the report in your ServiceNow instance or in the cloud \(Microsoft Office 365\).

    You can save the generated reports of the action tasks in your ServiceNow instances or in the cloud \(Microsoft Office 365\) for future references.


