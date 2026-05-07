---
title: Care Team Operations for Facilities data model tables
description: The Healthcare Facilities Case \[sn\_cto\_facilities\_case\] enables streamlined support for facilities management use cases.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Care Team Operations for Facilities, Healthcare Operations, Healthcare and Life Sciences]
---

# Care Team Operations for Facilities data model tables

The Healthcare Facilities Case **\[sn\_cto\_facilities\_case\]** enables streamlined support for facilities management use cases.

It extends the Healthcare Operations Core **\[sn\_hco\_case\]** case.

|Field|Description|
|-----|-----------|
|Number|The case number for this Healthcare Facilities case. Generated automatically when created.|
|Short description|Brief description of the issue.|
|Description|Description of the issue.|
|Category|The type of service.|
|Healthcare location|Healthcare location where the issue is being reported.|
|Location|Common location mapped to the healthcare location.|
|State|The current state of the Healthcare Facilities case. Synchronizes with the associated work order automatically when the Field Service Management plugin is installed.|
|Priority|Sequence in which the case should be resolved.|
|Urgency|Speed at which the case should be resolved.|
|Impact|Level of disruption caused. Indicates the size of the issue.|
|Opened by|The user who submitted the case.|
|Primary contact|The user for whom the case is created.|
|Assignment group|The assignment group of the user that fulfills and resolved the request/issue.|
|Assigned to|The user that fulfills and resolves the request/issue.|
|Requesting organization|The service organization of the requester.|
|Supporting organization|The service organization that fulfills the case/request.|
|Service|Service definition linked to the case.|

