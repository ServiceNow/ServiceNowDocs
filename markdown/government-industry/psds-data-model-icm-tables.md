---
title: Tables installed with Investigative Case Management
description: This section describes the tables installed with the Investigative Case Management application and shows how they store and manage information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-data-model-icm-tables.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Investigative Case Management, Data Model, Reference, Public Sector Digital Services \(PSDS\)]
---

# Tables installed with Investigative Case Management

This section describes the tables installed with the Investigative Case Management application and shows how they store and manage information.

## Investigative Case Management tables installed

|Table|Description|Extends Table|
|-----|-----------|-------------|
|Master Index|Parent table that contains information about all entity records created within the case. All new entities created within the case extend from this index.|N/A|
|Firearm Index|Contains information about the firearm entity records created within the case.|N/A|
|Location Index|Contains information about the location entity records created within the case.|N/A|
|Organization Index|Contains information about the organization entity records created within the case.|N/A|
|Person Index|Contains information about the person entity records created within the case.|N/A|
|Property Index|Contains information about the property entity records created within the case.|N/A|
|Vehicle Index|Contains information about the vehicle entity records created within the case.|N/A|
|Investigative Evidence|Contains information about evidence records within the case. Non-specific to PSDS ICM. Parent table of GSM Evidence \[sn\_gsm\_icm\_evidence\] table.|Evidence|
|Chain of Custody Log|Contains the custody log files created each time a piece of evidence is transferred. Non-specific to PSDS ICM. Parent table of GSM Chain of Custody Log \[sn\_gsm\_icm\_chain\_of\_custody\] table.|Chain of Custody Log|
|Investigative Case|Contains information about the investigative case record.|CSM Investigative Case|
|Investigative Task|Contains information about the investigative tasks records associated with the case.|CSM Investigative Task|
|Evidence|Contains evidence records created within the case. Specific to PSDS ICM.|N/A|
|Chain of Custody Log|Contains the custody log files created each time a piece of evidence is transferred. Specific to PSDS ICM.|N/A|
|CSM Investigative Case|Investigative case parent table. Non-specific to PSDS ICM.|N/A|
|CSM Investigative Task|Investigative case task parent table. Non-specific to PSDS ICM.|N/A|

**Parent Topic:**[Investigative Case Management Data Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/government-industry/psds-data-model-icm.md)

