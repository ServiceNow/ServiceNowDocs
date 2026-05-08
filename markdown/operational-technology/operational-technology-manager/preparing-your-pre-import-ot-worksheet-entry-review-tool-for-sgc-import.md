---
title: Prepare your Pre-import OT Worksheet Entry Review tool for Service Graph Connector import
description: Prepare your spreadsheet by positioning your existing data in the correct columns is crucial to the success of your upload.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Create an import task, Using the Service Graph Connector for Microsoft Excel through import tasks, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Prepare your Pre-import OT Worksheet Entry Review tool for Service Graph Connector import

Prepare your spreadsheet by positioning your existing data in the correct columns is crucial to the success of your upload.

## Before you begin

Role required: ot\_excel\_import\_user

## About this task

## Procedure

1.  Fill the following columns in the Microsoft Excel spreadsheet.

    **Note:** Column names cannot be changed. Extra columns can be added to the staging table. For more information about adding a new custom field mapping in the staging table, see [Add a custom field mapping in the staging table for Service Graph Connector for Microsoft Excel](add-new-column-mappings-excel-service-graph.md).

    Refer to the following tables for guidance while filling in the spreadsheet. The spreadsheet contains many columns. The examples and field descriptions are split into multiple sections.

    -   Filling in columns A through K
    -   Filling in columns L through Y
    -   Filling in columns Z through AI
    -   Filling in columns AJ through AT
    -   Filling in columns AU through BD
    -   Filling in columns BE through BR
    -   Filling in columns BS to BW
    -   Filling in columns 1 to 8
<table id="table_pf2_p4g_vpc"><thead><tr><th>

Column

</th><th>

Required column name

</th><th>

Type

</th><th>

Description and example

</th></tr></thead><tbody><tr><td>

A

</td><td>

Device criticality

</td><td>

string

</td><td>

Measure of how critical, or important, the OT device is, based on its role. Examples: -   High or Most critical
-   Medium or somewhat critical
-   Low or Less critical
-   None or not critical


</td></tr><tr><td>

B

</td><td>

Assigned to

</td><td>

string

</td><td>

Email address of the user that this OT device is assigned to. For example: bob@example.com

</td></tr><tr><td>

C

</td><td>

Backplane id

</td><td>

string

</td><td>

Unique ID that is used for the identification of the backplane and mapping to control modules. For example: BPSN123

</td></tr><tr><td>

D

</td><td>

Backplane name

</td><td>

string

</td><td>

Name of the backplane, if any, for the OT device. Examples: Backplane \#51, PLC1 Backplane

</td></tr><tr><td>

E

</td><td>

Control module parent id

</td><td>

string

</td><td>

Unique ID that is used for the identification of the control modules to the parent control system backplane. For example: 482bb239-05e8-4bad-ba59-925eb87ff06e

</td></tr><tr><td>

F

</td><td>

Correlation id

</td><td>

string

</td><td>

Unique ID that is used for identification of the OT device. Enter the correlation\_id a string. Examples: 482bb239-05e8-4bad-ba59-925eb87ff06e or 5123456. This column entry is required. -   Each imported OT device must have a correlation\_id that is unique.
-   The OT device data that you import normally originates in an external source system, which usually assigns a unique identifier to each record.


</td></tr><tr><td>

G

</td><td>

Custom field 1

</td><td>

string

</td><td>

\(Optional\) Custom data for the OT device is stored in the Attributes field on the CI. You can use this column to associate free-form data to the OT device for categorization or other purposes. Examples: Refurbished, Used

</td></tr><tr><td>

H

</td><td>

Custom field 2

</td><td>

string

</td><td>

\(Optional\) Custom data for the OT device is stored in the Attributes field on the CI. You can use this column to associate free-form data to the OT device for categorization or other purposes. Examples: Painting, Stamping

</td></tr><tr><td>

I

</td><td>

Custom field 3

</td><td>

string

</td><td>

\(Optional\) Custom data for the OT device is stored in the Attributes field on the CI. You can use this column to associate free-form data to the OT device for categorization or other purposes.

</td></tr><tr><td>

J

</td><td>

Custom field 4

</td><td>

string

</td><td>

\(Optional\) Custom data for the OT device is stored in the Attributes field on the CI. You can use this column to associate free-form data to the OT device for categorization or other purposes.

</td></tr><tr><td>

K

</td><td>

Custom field 5

</td><td>

string

</td><td>

\(Optional\) Custom data for the OT device is stored in the Attributes field on the CI. You can use this column to associate free-form data to the OT device for categorization or other purposes.

</td></tr></tbody>
</table><table id="table_ol4_lwj_stb"><thead><tr><th>

Column

</th><th>

Required column name

</th><th>

Type

</th><th>

Description and example

</th></tr></thead><tbody><tr><td>

L

</td><td>

Display name

</td><td>

string

</td><td>

Used to populate the display name of OT devices.

</td></tr><tr><td>

M

</td><td>

Equipment model entity path

</td><td>

string

</td><td>

Path of the equipment model entity that the OT device is mapped to.

</td></tr><tr><td>

N

</td><td>

Firmware version

</td><td>

string

</td><td>

Firmware version of the OT device, if any. For example: 12.0

</td></tr><tr><td>

O

</td><td>

First discovered

</td><td>

datetime

</td><td>

ISO-formatted timestamp of the first time that the OT device was first discovered on your network. For example: YYYY-MM-DD HH:MM:SS.

</td></tr><tr><td>

P

</td><td>

Hardware version

</td><td>

string

</td><td>

Hardware version of the OT device, if any. For example: 13.2

</td></tr><tr><td>

Q

</td><td>

Has module

</td><td>

Boolean

</td><td>

For control systems with modules, indicates that this system has modules. Examples: True, False

</td></tr><tr><td>

R

</td><td>

IO field device type

</td><td>

string

</td><td>

If this device is a field device, indicates if it is used for input, output, or both. Examples:-   input
-   output
-   input\_output

The device acts as both input and output.

</td></tr><tr><td>

S

</td><td>

IP Address 1

</td><td>

string

</td><td>

First IP address, if any, that is associated with the OT device. If there are multiple IP addresses, use the next IP address column \(IP Address 2\). Examples: 10.0.0.22, 10.0.0.12

</td></tr><tr><td>

T

</td><td>

IP Address 2

</td><td>

string

</td><td>

Second IP address, if any, that is associated with the OT device. Examples: 192.168.100.1, 192.168.100.5

</td></tr><tr><td>

U

</td><td>

IP Address 3

</td><td>

string

</td><td>

Third IP address, if any, that is associated with the OT device.

</td></tr><tr><td>

V

</td><td>

IP Address 4

</td><td>

string

</td><td>

Fourth IP address, if any, that is associated with the OT device.

</td></tr><tr><td>

W

</td><td>

IP Address 5

</td><td>

string

</td><td>

Fifth IP address, if any, that is associated with the OT device.

</td></tr><tr><td>

X

</td><td>

IP Address 6

</td><td>

string

</td><td>

Sixth IP address, if any, that is associated with the OT device.

</td></tr><tr><td>

Y

</td><td>

IP Address 7

</td><td>

string

</td><td>

Seventh IP address, if any, that is associated with the OT device.

</td></tr></tbody>
</table><table id="table_ayw_lyj_stb"><thead><tr><th>

Column

</th><th>

Required column name

</th><th>

Type

</th><th>

Description and example

</th></tr></thead><tbody><tr><td>

Z

</td><td>

IP Address 8

</td><td>

string

</td><td>

Eighth IP address, if any, that is associated with the OT device.

</td></tr><tr><td>

AA

</td><td>

IP Address 9

</td><td>

string

</td><td>

Ninth IP address, if any, that is associated with the OT device.

</td></tr><tr><td>

AB

</td><td>

MAC Address 1

</td><td>

string

</td><td>

First MAC address, if any, that is associated with the OT device. If there are multiple MAC addresses, use the next Mac address column \(MAC Address 2\). Examples: 94:94:1d:01:6d:5f, cc:7c:4a:fb:20:71**Note:** For an OT device, you must create an entry in at least one of these three spreadsheet columns, all values in these columns must be unique for the spreadsheet:

-   MAC Address 1
-   Name
-   Serial number


</td></tr><tr><td>

AC

</td><td>

MAC Address 2

</td><td>

string

</td><td>

Second MAC address, if any, that is associated with the OT device. For example: e5:4d:c8:36:b1:2d

</td></tr><tr><td>

AD

</td><td>

MAC Address 3

</td><td>

string

</td><td>

Third MAC address, if any, that is associated with the OT device.

</td></tr><tr><td>

AE

</td><td>

MAC Address 4

</td><td>

string

</td><td>

Fourth MAC address, if any, that is associated with the OT device.

</td></tr><tr><td>

AF

</td><td>

MAC Address 5

</td><td>

string

</td><td>

Fifth MAC address, if any, that is associated with the OT device.

</td></tr><tr><td>

AG

</td><td>

MAC Address 6

</td><td>

string

</td><td>

Sixth MAC address, if any, that is associated with the OT device.

</td></tr><tr><td>

AH

</td><td>

MAC Address 7

</td><td>

string

</td><td>

Seventh MAC address, if any, that is associated with the OT device.

</td></tr><tr><td>

AI

</td><td>

MAC Address 8

</td><td>

string

</td><td>

Eighth MAC address, if any, that is associated with the OT device.

</td></tr></tbody>
</table>    |Column|Required column name|Type|Description and example|
    |------|--------------------|----|-----------------------|
    |AJ|MAC Address 9|string|Ninth MAC address, if any, that is associated with the OT device.|
    |AK|Manufacturer|string|Name of the manufacturer of the OT device. Examples: Rockwell Automation, Dell|
    |AL|Memory card serial 1|string|Assigned serial number of the first memory card, if any, that is installed in the OT device. If there are multiple memory cards, use the next memory card serial column \(Memory card serial 2\). Examples: MMC DA362131, MemSN123|
    |AM|Memory card serial 2|string|Assigned serial number of the second memory card, if any, that is installed in the OT device. For example: MemSN123|
    |AN|Memory card serial 3|string|Assigned serial number of the third memory card, if any, that is installed in the OT device.|
    |AO|Memory size 1|string|Size of the first memory card, if any, that is installed in the OT device. Examples: 256 GB or 1 GB|
    |AP|Memory size 2|string|Size of the second memory card, if any, that is installed in the OT device. Examples: 256 GB or 1 GB|
    |AQ|Memory size 3|string|Size of the third memory card, if any, that is installed in the OT device. Examples: 256 GB or 1 GB|
    |AR|Memory type 1|string|Type of memory card that is installed in the OT device. If there are multiple memory cards, use multiple columns. For example: RAM|
    |AS|Memory type 2|string|Type of memory card that is installed in the OT device. Examples: RAM|
    |AT|Memory type 3|string|Type of memory card that is installed in the OT device.|

<table id="table_g1j_m5k_stb"><thead><tr><th>

Column

</th><th>

Required column name

</th><th>

Type

</th><th>

Description and example

</th></tr></thead><tbody><tr><td>

AU

</td><td>

Model number

</td><td>

string

</td><td>

Manufacturer's model number for the OT device. Examples: ThinkServer TD230, XPS 15z

</td></tr><tr><td>

AV

</td><td>

Module type

</td><td>

string

</td><td>

Description of the function of the control module, if this device is one. Examples: Input, Output

</td></tr><tr><td>

AW

</td><td>

Name

</td><td>

string

</td><td>

Host name of the OT device, usually as part of the FQDN. Examples: PLC1, Door Assembly HMI, and Robot Control Module.**Note:** For an OT device, you must create an entry in at least one of these three spreadsheet columns. All values in these columns must be unique for the spreadsheet:

-   MAC Address 1
-   Name
-   Serial number


</td></tr><tr><td>

AX

</td><td>

Operating system

</td><td>

string

</td><td>

Operating system, if any, that is installed on the OT device. Examples: Linux Fedora, Windows 10, Windows 2000, Mac OS 8. **Note:** For an OT device, you should create entries in the following spreadsheet columns, even though they are not required:

-   Type
-   If available, Operating System
-   If available, Firmware version


</td></tr><tr><td>

AY

</td><td>

OS version

</td><td>

string

</td><td>

Reported version of the operating system, if any, that is installed on the OT device. Examples: 10.0, 13.5.2 **Note:** For an OT device, you should create entries in the following spreadsheet columns, even though they are not required:

-   type
-   If available, os\_version
-   If available, firmware version


</td></tr><tr><td>

AZ

</td><td>

OT Staging Task

</td><td>

string

</td><td>

Tasks created to remediate invalid records on the staging table.

</td></tr><tr><td>

BA

</td><td>

Purdue level

</td><td>

string

</td><td>

Assigned Purdue level for the OT device. Assigning a Purdue level ensures that the Discovery for the Operational Technology function properly locates each item at the correct ICS level and produces accurate Discovery results. Examples: 1, 2, 3

</td></tr><tr><td>

BB

</td><td>

Rack number

</td><td>

string

</td><td>

Rack where the control module is mounted. Examples: 1, 2, 3

</td></tr><tr><td>

BC

</td><td>

Serial number

</td><td>

string

</td><td>

Assigned serial number, if any, for the OT device. Examples: SN545, SN998**Note:** For an OT device, you must create an entry in at least one of these three spreadsheet columns. All values in these columns must be unique for the spreadsheet:

-   MAC Address 1
-   Name
-   Serial number


</td></tr><tr><td>

BD

</td><td>

Serial number type

</td><td>

string

</td><td>

Normally set to the value of "system," but it could be a different type of serial number. For example: uuid

</td></tr></tbody>
</table><table id="table_mgh_5wk_stb"><thead><tr><th>

Column

</th><th>

Required column name

</th><th>

Type

</th><th>

Description and example

</th></tr></thead><tbody><tr><td>

BE

</td><td>

Short description

</td><td>

string

</td><td>

Short description of the OT device. Examples: HMI for the Door Painting Cell, Controls the door assembly robot.

</td></tr><tr><td>

BF

</td><td>

Site

</td><td>

string

</td><td>

The equipment models start at the site level and contain a detailed hierarchical structure that describes each industrial site.For more information, see [ISA-95 equipment model](../../mftg-manufacturing-process-mgr/concept/isa-95-equipment-model.md).

</td></tr><tr><td>

BG

</td><td>

Slot number

</td><td>

string

</td><td>

For a control module, indicates the slots that this device occupies in the chassis of the control system. Examples: 1, 2

</td></tr><tr><td>

BH

</td><td>

Software install date 1

</td><td>

datetime

</td><td>

Date that the application software was installed on the OT device. If there are multiple dates, use multiple columns.

 Use only UTC format for the date.

For example: YYYY-MM-DD HH:MM:SS

</td></tr><tr><td>

BI

</td><td>

Software install date 2

</td><td>

datetime

</td><td>

Date that the application software was installed on the OT device. If there are multiple dates, use multiple columns.Use only UTC format for the date. For example: YYYY-MM-DD HH:MM:SS

</td></tr><tr><td>

BJ

</td><td>

Software install date 3

</td><td>

datetime

</td><td>

Date that the application software was installed on the OT device. If there are multiple dates, use multiple columns.Use only UTC format for the date. Example: YYYY-MM-DD HH:MM:SS.

</td></tr><tr><td>

BK

</td><td>

Software installed 1

</td><td>

string

</td><td>

Name of the application software, if any, that is installed on the OT device. If there are multiple names, use multiple columns. For example: Rockwell HMI Vision

</td></tr><tr><td>

BL

</td><td>

Software installed 2

</td><td>

string

</td><td>

Name of the application software, if any, that is installed on the OT device.

</td></tr><tr><td>

BM

</td><td>

Software installed 3

</td><td>

string

</td><td>

Name of the application software, if any, that is installed on the OT device.

</td></tr><tr><td>

BN

</td><td>

Software version 1

</td><td>

string

</td><td>

Reported version of the application software, if any, that is installed on the OT device. If there are multiple versions, use multiple columns. For example: v1.2 or v2011 SP3 HF2 or 4.54.32145

</td></tr><tr><td>

BO

</td><td>

Software version 2

</td><td>

string

</td><td>

Reported version of the application software, if any, that is installed on the OT device.For example: v1.2 or v2011 SP3 HF2 or 4.54.32145

</td></tr><tr><td>

BP

</td><td>

Software version 3

</td><td>

string

</td><td>

Reported version of the application software, if any, that is installed on the OT device.For example: v1.2 or v2011 SP3 HF2 or 4.54.32145

</td></tr><tr><td>

BQ

</td><td>

Status

</td><td>

string

</td><td>

Status of the OT device:

-   **--None--**

No assigned status.

-   **Absent**

OT device is absent in your facilities.

-   **In Maintenance**

OT device is in maintenance and currently is off line.

-   **In stock**

OT device is in stock in your facilities.

-   **Installed**

OT device is installed in your facilities.

-   **Pending Install**

OT device is pending installation in your facilities.

-   **Pending repair**

OT device is pending repair but is not online yet.

-   **Retired**

OT device is retired.

-   **Stolen**

OT device has been stolen.

 **Note:**

The values in this field are mapped to **Life Cycle Stage** and **Life Cycle Stage Status** fields on the CI form.

</td></tr><tr><td>

BR

</td><td>

Support group

</td><td>

string

</td><td>

Name of the primary support group for this OT device. Examples: Door Support, Corporate IT Support.

</td></tr></tbody>
</table><table id="table_uyz_tlz_mzb"><thead><tr><th>

Column

</th><th>

Required column name

</th><th>

Type

</th><th>

Description and example

</th></tr></thead><tbody><tr><td>

BS

</td><td>

Transformed name

</td><td>

string

</td><td>

Users must not fill this column.

 By default, the transformed name value is populated using transformed column system properties.

 A user cannot edit the Transformed name.

 For system properties, see [Review the system properties used by the Service Graph Connector for Microsoft Excel](access-system-properties-used-by-service-graph-connector.md).

</td></tr><tr><td>

BT

</td><td>

Type

</td><td>

string

</td><td>

Type of OT device/configuration item \(CI\). Examples: PLC, DCS**Note:**

-   For a listing and explanation of valid CI types, see Operation Technology \(OT\) extension classes.
-   For an OT device, you should create entries in the following spreadsheet columns, even though they are not required:
    -   type
    -   os\_version


</td></tr><tr><td>

BU

</td><td>

Validation comments

</td><td>

string

</td><td>

Users must not fill this column.

 By default, Validation comments are populated after the validations are run on the staging table records that are imported from excel.

 Validation comments are not updated when records are imported.

 User cannot edit the Validation comments.

</td></tr><tr><td>

BV

</td><td>

Validation state

</td><td>

string

</td><td>

Users must not fill this column.

 By default, the validation state is populated when the data is imported in the staging table.

 Status of the OT device:

-   **Pending validation**

Default state when records are imported into the staging table.

-   **Invalid**

Cannot uniquely create a CI record in the CMDB.

-   **Partially valid**

One of the Transformed Name, MAC Address 1, and Serial number has no value. All the other fields \(correlation id, control module parent id\) have values.

-   **Valid**

All identifiers are present and are ready for import​.

-   **Imported**

Completed the import of the data from the staging table to the Import set table.

 User cannot edit the Validation state.

</td></tr><tr><td>

BW

</td><td>

Vendor

</td><td>

string

</td><td>

Name of the vendor of the OT device.

</td></tr></tbody>
</table><table id="table_p4d_th4_sbc"><thead><tr><th>

Column

</th><th>

Required column name

</th><th>

Type

</th><th>

Choice columns if applicable

</th><th>

Description and example

</th></tr></thead><tbody><tr><td>

1

</td><td>

Backup configuration status

</td><td>

choice list

</td><td>

Backup Enabled, Backup Disabled, Unknown, Not Applicable, Planned, Not Planned

</td><td>

Indicates whether the CI has been configured in the backup service or appliance with relevant policies. Examples: Backup Enabled

</td></tr><tr><td>

2

</td><td>

Backup execution mode

</td><td>

choice list

</td><td>

Manual, Automatic, Manual or Automatic, Unknown

</td><td>

Indicates whether the backup is configured to run automatically on a periodic basis, or if it is manually executed on an as-needed basis.Examples: Manual, Automatic

</td></tr><tr><td>

3

</td><td>

Backup source id

</td><td>

string

</td><td>

 

</td><td>

Backup service source identifier for a device, which identifies the device in external or internal backup services. Backup source id can include host\_id, vcenter\_id, instance\_id, db\_id.Examples: AdvWrks2008R2Backup

</td></tr><tr><td>

4

</td><td>

Last backup attempt

</td><td>

glide\_date\_time

</td><td>

 

</td><td>

Date and time of the last backup attempt made for a device.Examples: 2024-06-18 09:53:37

</td></tr><tr><td>

5

</td><td>

Last successful backup

</td><td>

glide\_date\_time

</td><td>

 

</td><td>

Date and time of the last successful backup made for a device.Examples: 2024-06-18 09:53:37

</td></tr><tr><td>

6

</td><td>

Backup recovery point objective

</td><td>

glide\_duration

</td><td>

 

</td><td>

Represents the amount of time that can elapse between backups and the amount of data lost.Examples: 90 12:00:00

</td></tr><tr><td>

7

</td><td>

Backup managed by

</td><td>

string

</td><td>

 

</td><td>

Email ID of the user responsible for managing the backup.Examples: firstname.lastname@example.com

</td></tr><tr><td>

8

</td><td>

Backup managed by group

</td><td>

string

</td><td>

 

</td><td>

Name of the primary support group responsible for managing the backup.Examples: App Engine Admins

</td></tr></tbody>
</table>2.  After populating the Microsoft Excel spreadsheet, save it in a known location for easy access to upload.


**Parent Topic:**[Create an import task](create-import-task-excel-sgc.md)

