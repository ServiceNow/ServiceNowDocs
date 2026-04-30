---
title: Field descriptions for log-based CI candidates
description: Field descriptions for the Log-based CI candidates table, the Log-based CI candidate form, and the Add CI candidate to CMDB form.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Enhancing the CMDB with host data found in logs, Administering Health Log Analytics, Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Field descriptions for log-based CI candidates

Field descriptions for the Log-based CI candidates table, the Log-based CI candidate form, and the Add CI candidate to CMDB form.

<table id="table_wrh_xmt_frb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Host name

</td><td>

The host name that Health Log Analytics discovered in the log data.

</td></tr><tr><td>

CI class type

</td><td>

The CI class type discovered in the log data. The CI class type is determined by the data input type:

-   Rsyslogs – CI class type: Linux Server
-   Linux Filebeat - CI class type: Linux Server
-   Windows Filebeat - CI class type: Windows Server
-   Winlogbeat - CI class type: Windows Server

</td></tr><tr><td>

Last log time

</td><td>

\(Read only\) The last time this host was found in the log data.

</td></tr><tr><td>

Operation

</td><td>

\(Read only\) The suggested action to take: Add - Add the CI to the CMDB.

</td></tr><tr><td>

Status

</td><td>

\(Read only\) The status of the suggested action.-   Pending - No action has been taken.
-   If the taken action failed, this field contains an error message.

</td></tr></tbody>
</table><table id="table_d1k_k25_frb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CI class type

</td><td>

The CI class type discovered in the log data. The CI class type is determined by the data input type:

-   Rsyslogs – CI class type: Linux Server
-   Linux Filebeat - CI class type: Linux Server
-   Windows Filebeat - CI class type: Windows Server
-   Winlogbeat - CI class type: Windows Server

</td></tr><tr><td>

CI name

</td><td>

The host name that Health Log Analytics discovered in the log data.

</td></tr><tr><td>

Operation

</td><td>

\(Read only\) The suggested action to take: Add - Add the CI to the CMDB.

</td></tr><tr><td>

Last log time

</td><td>

\(Read only\) The last time this host was found in the log data.

</td></tr><tr><td>

Status

</td><td>

\(Read only\) The status of the suggested action:-   Pending - No action has been taken.
-   If the taken action failed, this field contains an error message.

</td></tr></tbody>
</table><table id="table_eyh_vws_hrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the CI.

</td></tr><tr><td>

Asset tag

</td><td>

Alphanumeric information to help track the asset associated with the CI.

</td></tr><tr><td>

Manufacturer

</td><td>

The device manufacturer.

</td></tr><tr><td>

Asset

</td><td>

\(Read-only\) The asset associated with the CI.

</td></tr><tr><td>

Class

</td><td>

The asset group. For example, Linux Server.

</td></tr><tr><td>

Comments

</td><td>

Information about the asset.

</td></tr><tr><td>

Company

</td><td>

The company associated with the CI.This field is required.

</td></tr><tr><td>

Serial number

</td><td>

The serial number associated with the CI.

</td></tr><tr><td>

Model ID

</td><td>

The device model ID.

</td></tr><tr><td>

Assigned to

</td><td>

The person using or primarily responsible for this item.

</td></tr><tr><td>

Host name

</td><td>

The host name of the CI.

</td></tr><tr><td>

OS Domain

</td><td>

The OS domain of the CI.

</td></tr><tr><td>

Operating System

</td><td>

The OS running on the CI.

</td></tr><tr><td>

OS Version

</td><td>

The version of the OS running on the CI.

</td></tr><tr><td>

OS Service Pack

</td><td>

The service pack installed on the OS​.

</td></tr><tr><td>

DNS Domain

</td><td>

The DNS domain of the CI.

</td></tr><tr><td>

IP Address

</td><td>

The IP address of the CI.

</td></tr><tr><td>

Disk space \(GB\)

</td><td>

The amount of disk space, in GB.

</td></tr><tr><td>

Description

</td><td>

Textual description of the CI.

</td></tr><tr><td>

RAM \(MB\)

</td><td>

The amount of RAM on the computer​, in MB.

</td></tr><tr><td>

CPU manufacturer

</td><td>

The CPU manufacturer.

</td></tr><tr><td>

CPU type

</td><td>

The CPU type.

</td></tr><tr><td>

CPU speed \(MHz\)

</td><td>

The speed of the CPU, in MHz​.

</td></tr><tr><td>

CPU count

</td><td>

The number of CPUs​.

</td></tr><tr><td>

CPU core count

</td><td>

The number of cores per CPU​.

</td></tr><tr><td>

IsVirtual

</td><td>

Option for indicating whether the device is running on a virtual machine instance.​

</td></tr></tbody>
</table>**Parent Topic:**[Enhancing the CMDB with host data found in logs](../concept/hla-cmdb-enrich-concept.md)

