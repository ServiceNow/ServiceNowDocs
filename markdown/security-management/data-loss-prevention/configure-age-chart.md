---
title: Create age chart configurations
description: Configure the age chart that appears in the Data Loss Prevention Incident Response \(DLP IR\) Ops portal. This chart shows the count of open incidents by the number of days.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Create age chart configurations

Configure the age chart that appears in the Data Loss Prevention Incident Response \(DLP IR\) Ops portal. This chart shows the count of open incidents by the number of days.

## Before you begin

Role required:

-   sn\_dlir.admin - Create, edit, and delete.
-   sn\_dlir.analyst and sn\_dlir.analyst\_read - View \(read-only\).

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **Age Chart Configuration**.

2.  Review the age chart entries in the following table and customize the entries for your environment.

    |Name|Condition|
    |----|---------|
    |0-30 days|Age of the open incident that is between 0 through 30 days.|
    |31-60 days|Age of the open incident that is between 31 through 60 days.|
    |61-90 days|Age of the open incident that is between 61 through 90 days.|
    |90+ days|Age of the open incident that is over 90 days.|

3.  Add a new age chart configuration by clicking **New**.

4.  In the Name field, enter a **Name** for the DLP age chart configuration.

5.  Set the conditions for the DLP age chart configuration.

    1.  To add conditions, click **AND** or **OR**.

        -   If **AND** is selected, all conditions must be matched.
        -   If **OR** is selected, either condition can be matched.
        **Note:** The conditions in the condition builder are case sensitive.

    2.  To set a second filter condition, click **New Criteria**.

6.  Click **Submit**.


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

[Create assessments](create-and-manage-assessments-for-dlp-incidents.md)

[Configure response option for your DLP incidents](configure-response-option-mapping.md)

[Create incident response option rules](configure-end-user-action.md)

[Create user delegate configurations](configure-delegation.md)

[Create repeat offender identification rules](repeat-offender-identification-rules.md)

[Create additional incident data fields](create-custom-fields-dlp.md)

[DLP SLA Definition form](../reference/dlp-sla-def-properties.md)

[Configure advanced settings](configure-advanced-settings-dlp.md)

[Monitor DLP Integration Run process](../../dlp-microsoft/concept/configure-microsoft-dlp-integration-run-process.md)

[DLP Incident Access Restrictions](../concept/dlp-incident-access-restrictions.md)

[DLP Incidents Archival](dlp-archiving-rule.md)

