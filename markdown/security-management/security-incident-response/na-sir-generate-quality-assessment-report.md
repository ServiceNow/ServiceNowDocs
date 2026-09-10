---
title: Generate a quality assessment report
description: Generate a quality assessment report for a security incident using a predefined rule set.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/na-sir-generate-quality-assessment-report.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Generate quality assessment report, quality report, security incident quality analysis]
breadcrumb: [Explore Security incident quality assessment, Use generative AI skills, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Generate a quality assessment report

Generate a quality assessment report for a security incident using a predefined rule set.

## Before you begin

Role required: sn\_sec\_gen\_ai.qa\_reviewer

## About this task

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Security Incident Response Workspace**.

2.  Open a security incident that is assigned to you.

3.  Select the **Quality Assessment Reports** tab.

4.  Select **Generate New Report**.

5.  From the **Select Assessment Rules** list, choose an assessment rule.

6.  Select **Generate Report**.

    The report contains an overall assessment summary followed by the detailed assessment for all the rules. The report remains in the draft state until you publish it.

7.  In a draft report, use the ServiceNow Otto context menu to elaborate or shorten the content, refresh only the selected text, or enter your own instruction.

    1.  Use the ServiceNow Otto context menu to enter your instruction in natural language.

    2.  Select the text and use the ServiceNow Otto context menu to shorten, elaborate, or refresh it.

    3.  Select **Insert** to replace the current text with the updated.

    4.  Select **Save**.

8.  To regenerate the entire draft report with the latest security incident information, select the refresh icon.

    **Important:** Refreshing a draft report discards any manual edits that you made to it.

9.  To publish the draft report, select **Publish**.

    You can export a published report to a PDF file. After you publish a report, you can't edit it.

10. To revise a published report, select **Duplicate as draft**.

    A new draft report is created from the published report. When you publish the draft, the version number increases by one. You can have only one draft report at a time for an assessment rule set.

11. To email a published PDF report, select **Send email**.


**Parent Topic:**[Exploring Security incident quality assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/na-sir-quality-assessment.md)

