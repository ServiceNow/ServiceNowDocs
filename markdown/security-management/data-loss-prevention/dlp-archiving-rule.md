---
title: DLP Incidents Archival
description: The Data Loss Prevention Incident Response is provisioned with one archival rule in the base system for the DLP incident table. The related records are also added in the base system to the DLP incident archive rule.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# DLP Incidents Archival

The Data Loss Prevention Incident Response is provisioned with one archival rule in the base system for the DLP incident table. The related records are also added in the base system to the DLP incident archive rule.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Rules**.

    The system archiving rules that are in the base system are displayed.

2.  View the DLP archiving rule.

    **Note:** **DLP Incidents inactive over 15 days** is the default base system archiving rule for DLP incidents. You can modify the archiving rule if necessary. This rule signifies that the incidents that are inactive above 15 days are automatically archived.

    ![DLP incidents archival](../image/dlp-archiving-rule.png)

    **Note:** For information on how the archival rules are created, see [Create an archive rule](https://servicenow.com/docs/bundle/vancouver-platform-administration/page/administer/database-rotation/task/t_CreateAnArchiveRule.html).

    For information on how to view the archived incidents, see [View archived DLP incidents](../concept/using-dlp-ops-portal.md#).

3.  **Update** the rule.


-   **[Archive DLP related records](archive-dlp-related-records.md)**  
Use the Archive Related Records related list for DLP incidents to add the related records to the archive rule.

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

[Create age chart configurations](configure-age-chart.md)

[Create user delegate configurations](configure-delegation.md)

[Create repeat offender identification rules](repeat-offender-identification-rules.md)

[Create Additional Incident Data Fields](create-custom-fields-dlp.md)

[DLP SLA Definition form](../reference/dlp-sla-def-properties.md)

[Configure advanced settings](configure-advanced-settings-dlp.md)

[Monitor DLP Integration Run process](../../dlp-microsoft/concept/configure-microsoft-dlp-integration-run-process.md)

[DLP Incident Access Restrictions](../concept/dlp-incident-access-restrictions.md)

