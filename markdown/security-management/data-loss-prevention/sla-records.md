---
title: Create a Data Loss Prevention Incident Response SLA trigger
description: Create a Data Loss Prevention Incident Response SLA trigger condition that enables a prompt and efficient response to an incident when triggered.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/data-loss-prevention/sla-records.html
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Create a Data Loss Prevention Incident Response SLA trigger

Create a Data Loss Prevention Incident Response SLA trigger condition that enables a prompt and efficient response to an incident when triggered.

## Before you begin

Role required:

-   sn\_dlir.admin - Create, update, and delete DLP SLA triggers
-   sn\_dlir.analyst.read - Read Trigger table.

## Procedure

1.  Navigate to **All** &gt; **DLP Administration** &gt; **SLA Triggers**.

2.  Select **New** to create the SLA trigger.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the trigger|
    |Order|Order in which the trigger is considered.|
    |Active|Option to evaluate the SLA trigger.|
    |Trigger when a DLP incident is updated|Option to evaluate the trigger condition on each update of the DLP incident.|

3.  Configure a condition by selecting the rule record and defining conditions in the **Trigger Condition** field.

    For example, the trigger condition to set SLAs on DLP incidents from an email scan source would be **\[Scan Source\]\[is\]\[Email SMTP\]**.

4.  Select **Submit**.


## Result

Once a task SLA record for a Data Loss Prevention Incident Response incident is created, the SLA records tab becomes visible for that particular incident in the workspace. This tab enables you to use an SLA system for your organization's task.

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

[DLP Incidents Archival]()

