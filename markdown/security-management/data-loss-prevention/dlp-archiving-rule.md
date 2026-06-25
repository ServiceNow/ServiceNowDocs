---
title: DLP Incidents Archival
description: The Data Loss Prevention Incident Response is provisioned with one archival rule in the base system for the DLP incident table. The related records are also added in the base system to the DLP incident archive rule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/data-loss-prevention/dlp-archiving-rule.html
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-06-25"
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

    \[Omitted image "dlp-archiving-rule.png"\] Alt text: DLP incidents archival

    **Note:** For information on how the archival rules are created, see [Create an archive rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateAnArchiveRule.md).

    For information on how to view the archived incidents, see [View archived DLP incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/data-loss-prevention/using-dlp-ops-portal.md).

3.  **Update** the rule.


-   **[Archive DLP related records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/data-loss-prevention/archive-dlp-related-records.md)**  
Use the Archive Related Records related list for DLP incidents to add the related records to the archive rule.

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

[Create assessments]()

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

