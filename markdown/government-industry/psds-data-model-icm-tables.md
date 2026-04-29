---
title: Tables installed with Investigative Case Management
description: This section describes the tables installed with the Investigative Case Management application and shows how they store and manage information.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Investigative Case Management, Data Model, Reference, Public Sector Digital Services \(PSDS\)]
---

# Tables installed with Investigative Case Management

This section describes the tables installed with the Investigative Case Management application and shows how they store and manage information.

## Investigative Case Management tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th><th>

Extends Table

</th></tr></thead><tbody><tr><td>

Master Index\[sn\_icm\_master\_index\]

</td><td>

Parent table that contains information about all entity records created within the case. All new entities created within the case extend from this index.

</td><td>

N/A

</td></tr><tr><td>

Firearm Index\[sn\_icm\_firearm\]

</td><td>

Contains information about the firearm entity records created within the case.

</td><td>

N/A

</td></tr><tr><td>

Location Index\[sn\_icm\_location\]

</td><td>

Contains information about the location entity records created within the case.

</td><td>

N/A

</td></tr><tr><td>

Organization Index\[sn\_icm\_organization\]

</td><td>

Contains information about the organization entity records created within the case.

</td><td>

N/A

</td></tr><tr><td>

Person Index\[sn\_icm\_person\]

</td><td>

Contains information about the person entity records created within the case.

</td><td>

N/A

</td></tr><tr><td>

Property Index\[sn\_icm\_property\]

</td><td>

Contains information about the property entity records created within the case.

</td><td>

N/A

</td></tr><tr><td>

Vehicle Index\[sn\_icm\_vehicle\]

</td><td>

Contains information about the vehicle entity records created within the case.

</td><td>

N/A

</td></tr><tr><td>

Investigative Evidence\[sn\_icm\_evidence\]

</td><td>

Contains information about evidence records within the case. Non-specific to PSDS ICM. Parent table of GSM Evidence \[sn\_gsm\_icm\_evidence\] table.

</td><td>

Evidence

 \[sn\_gsm\_icm\_evidence\]

</td></tr><tr><td>

Chain of Custody Log\[sn\_icm\_chain\_of\_custody\]

</td><td>

Contains the custody log files created each time a piece of evidence is transferred. Non-specific to PSDS ICM. Parent table of GSM Chain of Custody Log \[sn\_gsm\_icm\_chain\_of\_custody\] table.

</td><td>

Chain of Custody Log

 \[sn\_gsm\_icm\_chain\_of\_custody\]

</td></tr><tr><td>

Investigative Case

 \[sn\_gsm\_icm\_case\]

</td><td>

Contains information about the investigative case record.

</td><td>

CSM Investigative Case

 \[sn\_csm\_icm\_case\]

</td></tr><tr><td>

Investigative Task\[sn\_gsm\_icm\_task\]

</td><td>

Contains information about the investigative tasks records associated with the case.

</td><td>

CSM Investigative Task

 \[sn\_csm\_icm\_task\]

</td></tr><tr><td>

Evidence\[sn\_gsm\_icm\_evidence\]

</td><td>

Contains evidence records created within the case. Specific to PSDS ICM.

</td><td>

N/A

</td></tr><tr><td>

Chain of Custody Log\[sn\_gsm\_icm\_chain\_of\_custody\]

</td><td>

Contains the custody log files created each time a piece of evidence is transferred. Specific to PSDS ICM.

</td><td>

N/A

</td></tr><tr><td>

CSM Investigative Case\[sn\_csm\_icm\_case\]

</td><td>

Investigative case parent table. Non-specific to PSDS ICM.

</td><td>

N/A

</td></tr><tr><td>

CSM Investigative Task\[sn\_csm\_icm\_task\]

</td><td>

Investigative case task parent table. Non-specific to PSDS ICM.

</td><td>

N/A

</td></tr></tbody>
</table>**Parent Topic:**[Investigative Case Management Data Model](psds-data-model-icm.md)

