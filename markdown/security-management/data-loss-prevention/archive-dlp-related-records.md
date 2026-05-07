---
title: Archive DLP related records
description: Use the Archive Related Records related list for DLP incidents to add the related records to the archive rule.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [DLP Incidents Archival, Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Archive DLP related records

Use the Archive Related Records related list for DLP incidents to add the related records to the archive rule.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Archiving** &gt; **Archive Rules**.

2.  Select **DLP Incidents inactive over 15 days** archiving rule.

3.  Go to **Archive Related Records** related list.

4.  View the DLP related records.

    |Application|Reference Table|
    |-----------|---------------|
    |DLP Incident Response integration with Symantec|Symantec DLP Incident Profile M2M \[sn\_sym\_dlp\_incident\_profile\_m2m\]|
    |Data Loss Prevention Incident Response|Custom Field Value \[sn\_dlir\_custom\_field\_value\]|
    |DLP Incident Response integration with Microsoft|Microsoft DLP Incident Profile M2M \[sn\_msft\_dlp\_incident\_profile\_m2m\]|
    |DLP Incident Response integration with Microsoft|Detected Sensitive Information Type \[sn\_msft\_dlp\_detected\_sensitive\_information\_type\]|
    |Data Loss Prevention Incident Response|Custom Attribute \[sn\_dlir\_custom\_attribute\]|
    |DLP Incident Response integration with Proofpoint|Proofpoint DLP Incident M2M \[sn\_pp\_dlp\_incident\_m2m\]|
    |DLP Incident Response integration with Netskope|Netskope DLP Incident M2M \[sn\_ns\_dlp\_incident\_m2m\]|
    |DLP Incident Response integration with Symantec|Detected Sensitive Information Type \[sn\_sym\_dlp\_detected\_sensitive\_information\_type\]|

    **Note:** All the system tables such as Emails, Assessments, Attachments will automatically direct to the archived DLP record.

5.  Select the archive related record rule you want to archive.

    **Note:** For more information on how to add more related records, see [Archive DLP related records](https://servicenow.com/docs/bundle/vancouver-platform-administration/page/administer/database-rotation/task/t_CreateAnArchiveRule.html) on ServiceNow AI Platform.


**Parent Topic:**[DLP Incidents Archival](dlp-archiving-rule.md)

