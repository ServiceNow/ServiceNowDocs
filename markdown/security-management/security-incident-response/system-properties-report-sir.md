---
title: System properties for reports
description: The system properties for Security Incident Response reports are explained below.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure report templates in Security Incident Response, Configure, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# System properties for reports

The system properties for Security Incident Response reports are explained below.

|Property|Description|Value|
|--------|-----------|-----|
|sn\_si.sn\_si\_incident.load\_all\_records|Loads all the records for the lists in the report created from a template. true - Load all records and false - loads specific number of records defined by sn\_si.sn\_si\_incident.reporting\_list\_records\_count property.|False|
|sn\_si.sn\_si\_incident.max\_list\_columns\_allowed|Limit the number of columns which can be added when rendering lists in report pdfs. This will use the columns from the beginning from the view till the allowed limit.|5|
|sn\_si.sn\_si\_incident.report\_default\_style\_object|Use this property to control css of free form fields, left panel, report lists.|\(JSON object\)|
|sn\_si.sn\_si\_incident.reporting\_list\_records\_count|Loads specific number of records in the report editor.|200|
|sn\_si\_reporting\_email\_template\_sn\_si\_incident|Sys ID of the email client template for the SIR \(sn\_si\_incident\) table which will be used in shared report.|9ce97ae643461210416896ed3ab8f258|
|sn\_si.sn\_si\_incident.ctx\_menu\_field\_header|Field header|sn\_si\_incident\_report\_field\_header,sn\_si\_incident\_report\_list\_header|
|sn\_si.sn\_si\_incident.defang\_record\_list\_urls|Control whether the URLs from list are defanged or not.|False|
|sn\_si.sn\_si\_incident.reporting\_dot\_walk\_tables|List of tables available for dot-walking in reports.|\(JSON object\)|

**Parent Topic:**[Configure report templates in Security Incident Response](daily-status-sir.md)

