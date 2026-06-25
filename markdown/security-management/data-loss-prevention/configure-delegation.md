---
title: Create user delegate configurations
description: Prevent certain executives in the organization from receiving notifications about the incidents assigned or escalated to them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/data-loss-prevention/configure-delegation.html
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Create user delegate configurations

Prevent certain executives in the organization from receiving notifications about the incidents assigned or escalated to them.

## Before you begin

Role required:

-   sn\_dlir.admin - Create, edit, and delete.
-   sn\_dlir.analyst and sn\_dlir.analyst\_read - View \(read-only\).

## About this task

Consider a scenario where the executive is a user who belongs to a leadership or executive group. The executive should not be sent emails about incident assignment or escalation. A delegated user can then take the necessary action on behalf of the executive.

Once a user has assigned a particular person, Henry, as a delegate, another user cannot assign Henry as a delegate again. Similarly, a delegate cannot assign another user as a delegate.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **Delegate Configuration**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |User|Name of the user who needs a delegate for DLP incidents.|
    |Delegate|Name of the user who can respond to the DLP incident on behalf of the original end user.|

4.  Click **Submit**.


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

[Create repeat offender identification rules]()

[Create additional incident data fields]()

[DLP SLA Definition form]()

[Configure advanced settings]()

[Monitor DLP Integration Run process]()

[DLP Incident Access Restrictions]()

[DLP Incidents Archival]()

