---
title: Create assessments
description: Create and manage assessments to enable end users to respond to DLP incidents. You can use the assessments to gather information about the sensitive data exposed or leaked from the DLP incidents.
locale: en-US
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

Create and manage assessments for DLP incidents![Create and manage assessments for DLP incidents]()

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

8.  To add more categories for the assessment, click the ![Add category icon](../image/dlp-plus-icon.png) icon.

9.  To modify an existing category, click the ![Add category icon](../image/dlp-setting-icon.png) icon.

10. After creating the different assessment questions for the first time, click **Save**, and then **Publish**.


**Parent Topic:**[DLP Incident Response Administration](../concept/data-loss-prevention-administration.md)

**Related topics**  


[DLP default configuration settings](configure-data-loss-prevention.md)

[Create end user lookup rules](configure-enduser-lookup-rules.md)

[Create assignment rules](create-assignment-rules.md)

[Create incident consolidation rules](configure-incident-consolidation-rules-to-consolidate-your-dlp-incidents.md)

[Create response due date rules](setup-response-due-date-rules.md)

[Create Approval Rules](configure-approval-rules.md)

[Create user instructions templates](create-and-manage-user-instructions-template-for-dlp-incidents.md)

[Create email templates](create-and-manage-email-templates.md)

[Create a Data Loss Prevention Incident Response SLA trigger](sla-records.md)

[Create a Data Loss Prevention Incident Response SLA definition](dlp-sla-definitions.md)

[Configure response option for your DLP incidents](configure-response-option-mapping.md)

[Create incident response option rules](configure-end-user-action.md)

[Create age chart configurations](configure-age-chart.md)

[Create user delegate configurations](configure-delegation.md)

[Create repeat offender identification rules](repeat-offender-identification-rules.md)

[Create additional incident data fields](create-custom-fields-dlp.md)

[DLP SLA Definition form](../reference/dlp-sla-def-properties.md)

[Configure advanced settings](configure-advanced-settings-dlp.md)

[Monitor DLP Integration Run process](../../dlp-microsoft/concept/configure-microsoft-dlp-integration-run-process.md)

[DLP Incident Access Restrictions](../concept/dlp-incident-access-restrictions.md)

[DLP Incidents Archival](dlp-archiving-rule.md)

