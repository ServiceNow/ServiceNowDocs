---
title: Standard import set tables
description: Several Import Set tables are available by default.
locale: en-US
release: xanadu
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Import sets, Imports, Creating integrations with applications]
---

# Standard import set tables

Several Import Set tables are available by default.

## Notification

A standard object for describing an external interface for a notification in the system, such as alarms and alerts from monitoring systems. The default transform map for this object will create or update an incident record. The incoming notifications are coalesced into incidents based on the UUID field.

<table id="table_r3s_cb1_tq"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

uuid

</td><td>

The universally unique identification number or string that uniquely identifies this notification. It is marked as the coalescing value in the default transform map for the corresponding Incident and is mapped to the correlation\_id field of Incident.

</td><td>

Character \(40\)

</td></tr><tr><td>

corrective\_message

</td><td>

A free form string value that indicates the corrective or followup steps to be taken to address the issue identified in this notification. This field is not mapped by default.

</td><td>

Character \(40\)

</td></tr><tr><td>

duration

</td><td>

A string value representing the time value duration affecting the issue reported in this notification. Out of box, the duration field is not mapped. The format of the time is up to the calling program and must be mapped accordingly in the default map to be used.

</td><td>

Character \(40\)

</td></tr><tr><td>

expires\_on

</td><td>

A string value representing the datetime value that the issue reported in this notification will expire. Out of box, the expires\_on field is not mapped. The format of the time is up to the calling program and must be mapped accordingly in the default map to be used.

</td><td>

Character \(40\)

</td></tr><tr><td>

message

</td><td>

A string value describing the nature of the issue related to this notification. It should be a concise description and is mapped to the short\_description field of the Incident.

</td><td>

Character \(80\)

</td></tr><tr><td>

comments

</td><td>

A string value containing additional comments related to this notification. The value is mapped to the comments field of the Incident.

</td><td>

Character \(4000\)

</td></tr><tr><td>

category

</td><td>

A string value categorising the nature of this notification. The value is mapped to the category field of the Incident, and therefore should be one of its valid values. If an existing value does not exist, the default behavior is to create a new category.

</td><td>

Character \(40\)

</td></tr><tr><td>

assignment\_group

</td><td>

A string value of the assignment group for this notification. The value is mapped to the assignment\_group field of the Incident, and therefore should be one of its valid values. If an existing value does not exist, the default behavior is to create a new assignment group and set it for the resulting incident.

</td><td>

Character \(40\)

</td></tr><tr><td>

severity

</td><td>

A string representation of a numeric value that indicates the severity of the issue being reported in this notification. This field is mapped to the severity field on Incident. The out of box numeric values and their meanings are:-   1 - High
-   2 - Medium
-   3 - Low

</td><td>

Character \(40\)

</td></tr><tr><td>

state

</td><td>

A string that indicates the state of the issue being reported in this notification. This field is mapped to the incident\_state field on Incident. The out of box values are:-   New
-   Active
-   Resolved
-   Closed

</td><td>

Character \(40\)

</td></tr><tr><td>

source

</td><td>

A string value to indicate the source of the issue or the configuration item \(by unique identifier eg IP address, host name etc\) related to the issue in this notification. It s mapped to the cmdb\_ci field of Incident.

</td><td>

Character \(40\)

</td></tr><tr><td>

timestamp

</td><td>

A string value representing the datetime value that marks the beginning of the issue reported in this notification. Out of box, the timestamp field is not mapped. The format of the time is up to the calling program and must be mapped accordingly in the default map to be used.

</td><td>

Character \(40\)

</td></tr><tr><td>

type

</td><td>

A string value categorizing the type of issue related to this notification. Out of box, this field is not mapped to any field on Incident. Integrations using this Notification message may use this field to identify its source and trigger additional scripts.

</td><td>

Character \(40\)

</td></tr></tbody>
</table>## Computer

A standard object for describing an external interface for a computer in the system. The default transform map will create/update a Computer \(cmdb\_ci\_computer\) or Server \(cmdb\_ci\_server, cmdb\_ci\_win\_server, cmdb\_aix\_server etc ..\) based on the operating\_system field value. The incoming computers are coalesced based on the serial\_number field. Additionally, the transform script of the map will map to various extensions of the Computer \(cmdb\_ci\_computer\) based on the operating\_system value being entered.

-   UNIX Server \(cmdb\_ci\_unix\_server\)
    -   AIX
    -   HP/UX
    -   Solaris
    -   AIX
-   Windows Server \(cmdb\_ci\_win\_server\)
    -   Windows 2000 Server
    -   Windows 2003 Server
    -   Windows NT 4.0
-   Server \(cmdb\_ci\_server\)

    Any operating system that contains the word "Linux".


<table id="table_mhh_wc1_tq"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Data type

</th></tr></thead><tbody><tr><td>

serial\_number

</td><td>

The unique identifier for this computer. It is marked as the coalescing value in the default transform map for the correcponding Computer and is mapped to the serial\_number field of Computer \(cmdb\_ci\_computer\).

</td><td>

Character \(40\)

</td></tr><tr><td>

cpu\_count

</td><td>

The number of CPUs that this computer has. It is mapped to the cpu\_count field of the Computer \(cmdb\_ci\_computer\) table.

</td><td>

Character \(40\)

</td></tr><tr><td>

cpu\_speed

</td><td>

The clock speed of the CPU in MHz. This field is mapped to the cpu\_speed field of Computer \(cmdb\_ci\_computer\)

</td><td>

Character \(40\)

</td></tr><tr><td>

cpu\_type

</td><td>

Free form text describing the type of CPU. Example values are "GenuineIntel", "IBM", or "Pentium 4". This field is mapped to the cpu\_type field of Computer \(cmdb\_ci\_computer\)

</td><td>

Character \(40\)

</td></tr><tr><td>

disk\_space

</td><td>

A numeric value describing the total disk space available to the computer in GB. This field is mapped to the disk\_space field of Computer \(cmdb\_ci\_computer\)

</td><td>

Character \(40\)

</td></tr><tr><td>

manufacturer

</td><td>

A string name for the manufacturer of the computer. This field is mapped to the manufacturer field of Computer \(cmdb\_ci\_computer\) which is a reference to Company \(core\_company\)

</td><td>

Character \(40\)

</td></tr><tr><td>

model\_id

</td><td>

A string name for the model of the computer. This field is mapped to the model\_id field of Computer \(cmdb\_ci\_computer\) which is a reference to Model Name \(cmdb\_model\)

</td><td>

Character \(40\)

</td></tr><tr><td>

name

</td><td>

A string value representing the name of the Computer, usually a host name or IP/MAC address. It is mapped to the name field of Computer \(cmdb\_ci\_computer\)

</td><td>

Character \(40\)

</td></tr><tr><td>

operating\_system

</td><td>

A string value for the main operating system running on the computer. It is mapped to the os field of Computer \(cmdb\_ci\_computer\). Out of box values are:-   AIX
-   GNU/Linux

-   HP/UX
-   Linux Fedora
-   Linux Red Hat
-   Linux SuSE
-   macOS OS 10 \(OS/X\)
-   macOS OS 8
-   macOS OS 9
-   macOS OS/X
-   OS/400
-   Solaris
-   SunOS
-   Windows
-   Windows 2000
-   Windows 2000 Advanced Server
-   Windows 2000 Datacenter Server
-   Windows 2000 Professional
-   Windows 2000 Server
-   Windows 2003 Datacenter
-   Windows 2003 Enterprise
-   Windows 2003 Standard
-   Windows 2003 Web
-   Windows 95
-   Windows 98
-   Windows ME
-   Windows NT 4.0
-   Windows XP
-   Windows XP Home
-   Windows XP Professional
-   Windows 2000 Server
-   Windows 2003 Enterprise

</td><td>

Character \(40\)

</td></tr><tr><td>

ram

</td><td>

A numeric value for the total number of memory installed on this computer in MB. This value is mapped to the ram field of Computer \(cmdb\_ci\_computer\)

</td><td>

Character \(40\)

</td></tr></tbody>
</table>## User

A standard object for describing an external interface for a user in the system. The default transform map script sets the user\_name field value to first\_name.last\_name if the web service's user\_id field value is not supplied, otherwise, the user\_id value is mapped directly to the user\_name field in the User \(sys\_user\) table.

|Field|Description|Data type|
|-----|-----------|---------|
|email|A string value containing the user's email address. This value is mapped to the email field in User \(sys\_user\) and is set as the coalesce value for the transform.|Character \(40\)|
|department|The department the user is in. This field is mapped to the department field in User \(sys\_user\) which is a reference to the Department \(cmn\_department\) table.|Character \(40\)|
|first\_name|The first name of the user, mapped to the first\_name field of the User \(sys\_user\) table.|Character \(40\)|
|last\_name|The last name of the user, mapped to the last\_name field of the User \(sys\_user\) table.|Character \(40\)|
|location|The location the user is in, mapped to the location field of the User \(sys\_user\) table which is a reference field to Location \(cmn\_location\)|Character \(40\)|
|phone|The phone number of the user, mapped to the phone \(Business Phone\) field of the User \(sys\_user\) table.|Character \(40\)|
|user\_id|This is the user identification, usually a login name, that maps to the user\_name \(User ID\) field of the User \(sys\_user\) table.|Character \(40\)|

## Location

A standard object for describing an external interface for a location in the system. The web service will create or modify records in the Location \(cmn\_location\) table.

|Field|Description|Data type|
|-----|-----------|---------|
|name|The name of the location, for example "Headquarters", "Sales office" etc. This field is mapped to the name field of Location \(cmn\_location\) and is part of the coalesce to search for an existing location.|Character \(40\)|
|street|The street address of the location, for example "1234 ServiceNow way" etc. This field is mapped to the street field of Location \(cmn\_location\) and is part of the coalesce to search for an existing location.|Character \(40\)|
|city|The city of the location, for example "San Diego", "Madrid" etc. This field is mapped to the city field of Location \(cmn\_location\) and is part of the coalesce to search for an existing location.|Character \(40\)|
|state|The state of the location, for example "California", "Connecticut" etc. This field is mapped to the city field of Location \(cmn\_location\) and is part of the coalesce to search for an existing location.|Character \(40\)|
|zip|The zip code for the location, for example "92130", "10001" etc. This field is mapped to the zip field of Location \(cmn\_location\) and is part of the coalesce to search for an existing location.|Character \(40\)|
|country|The country for the location, for example "USA", "United Kingdom" etc. This field is mapped to the country field of Location \(cmn\_location\).|Character \(40\)|

