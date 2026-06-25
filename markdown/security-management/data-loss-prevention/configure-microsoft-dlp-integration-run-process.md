---
title: Monitor DLP Integration Run process
description: Track and monitor the ongoing ingestion or the integration run process. The integration run processes contains the statistics on how much the data was processed and the integration status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/data-loss-prevention/configure-microsoft-dlp-integration-run-process.html
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Monitor DLP Integration Run process

Track and monitor the ongoing ingestion or the integration run process. The integration run processes contains the statistics on how much the data was processed and the integration status.

Role required: sn\_dlir.admin.

The integration run process lists the details on how many records are ingested. For example:

1.  In Symantec integration, the process contains both child and parent integration runs. The parent record indicates the ingestion data and child record indicates the enrichment calls and custom attribute records.
2.  In Microsoft integration, there is only parent record ingestion process to be run.

**DLP Integration Run Processes**: This displays the queue entries, status of queue entries, and fetched records.

The integration run contains the Source for which the integration profile and the integration run record is created, profile polling intervals, ingestion states and substates, incident count which indicates the number of records that are ingested.

1.  Navigate to **DLP Administration** &gt; **Integration Runs**.
2.  Select the integration run from the list.
3.  Navigate to the **DLP Integration Run Process**.
4.  View the queue entry status of the record.

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

[DLP Incident Access Restrictions]()

[DLP Incidents Archival]()

