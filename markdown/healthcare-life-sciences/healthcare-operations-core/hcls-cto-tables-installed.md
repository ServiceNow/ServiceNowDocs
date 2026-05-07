---
title: Tables installed with Healthcare Operations Core
description: The Healthcare Operations Core Case enables streamlined support for operational healthcare use cases.
locale: en-US
release: australia
product: Healthcare Operations Core
classification: healthcare-operations-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data model, Reference, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Tables installed with Healthcare Operations Core

The Healthcare Operations Core Case enables streamlined support for operational healthcare use cases.

It extends the Case \[sn\_customerservice\_case\] table to store all healthcare cases associated with a patient. For more information, see [Tables installed with Customer Service Management](https://www.servicenow.com/docs/access?context=r_TIWCustomerService&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

It includes the Healthcare Location field, which references the Healthcare Location table in the Healthcare and Life Sciences data model.

|Field|Description|
|-----|-----------|
|Number|The case number. Generated automatically when the case is created.|
|Short description|Brief description of the issue or request.|
|Description|Detailed description of the issue or request.|
|Category|The type of service.|
|Healthcare location|The healthcare location where the issue is being reported.|
|Location|Common location mapped to the healthcare location.|
|State|The current state of the case.|
|Priority|Sequence in which the case should be resolved.|
|Urgency|Speed at which the case should be resolved.|
|Impact|Level of disruption caused. Indicates the size of the issue.|
|Opened by|The user who submitted the case.|
|Primary contact|The user for whom the case is created.|
|Assignment group|The group responsible for fulfilling and resolving the case.|
|Assigned to|The user responsible for fulfilling and resolving the case.|
|Requesting organization|The service organization of the requester.|
|Supporting organization|The service organization that fulfills the case.|
|Service|Service definition linked to the case.|

