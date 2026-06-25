---
title: Create assessments
description: Create and manage assessments to enable end users to respond to DLP incidents. You can use the assessments to gather information about the sensitive data exposed or leaked from the DLP incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/data-loss-prevention/create-and-manage-assessments-for-dlp-incidents.html
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Create assessments

Create and manage assessments to enable end users to respond to DLP incidents. You can use the assessments to gather information about the sensitive data exposed or leaked from the DLP incidents.

## Before you begin

Role required:

-   sn\_dlir.admin - Create, edit, and delete.
-   sn\_dlir.analyst and sn\_dlir.analyst\_read - View \(read-only\).

## About this task

DLP incident assessments help you identify potential threats and vulnerabilities to your data based on the end-user response. You can use this information to determine your end users' existing gaps, concerns, and expectations.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **Assessments**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the DLP incident assessment.|
    |Active|Option to indicate whether the DLP incident assessment is active.|
    |Description|Unique description for this DLP incident assessment.|
    |Assessment Introduction|Provide an introduction or context for your assessment. You can also use variables from the Select variables section to dynamically display certain fields.|

4.  Click **Submit**.

5.  After creating an assessment, open the assessment and click **Assessment Designer**.

6.  In the New Assessment section, select a type of assessment question under the Controls section.

7.  Drag-and-drop the required assessment question type under the New Assessment section.

    For example, you can drag-and-drop the **Choice** control under the New Assessment or New Category section.

8.  To add more categories for the assessment, click the \[Omitted image "dlp-plus-icon.png"\] Alt text: Add category icon icon.

9.  To modify an existing category, click the \[Omitted image "dlp-setting-icon.png"\] Alt text: Add category icon icon.

10. After creating the different assessment questions for the first time, click **Save**, and then **Publish**.


**Parent Topic:**[DLP Incident Response Administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/data-loss-prevention/data-loss-prevention-administration.md)

**Related topics**  


[DLP default configuration settings]()

[Create end user lookup rules]()

[Create assignment rules]()

[Create incident consolidation rules]()

[Create response due date rules]()

[Create Approval Rules]()

[Create user instructions templates]()

[Create email templates]()

[Create a Data Loss Prevention Incident Response SLA trigger]()

[Create a Data Loss Prevention Incident Response SLA definition]()

[Configure response option for your DLP incidents]()

[Create incident response option rules]()

[Create age chart configurations]()

[Create user delegate configurations]()

[Create repeat offender identification rules]()

[Create additional incident data fields]()

[DLP SLA Definition form]()

[Configure advanced settings]()

[Monitor DLP Integration Run process]()

[DLP Incident Access Restrictions]()

[DLP Incidents Archival]()

