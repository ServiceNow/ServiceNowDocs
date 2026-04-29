---
title: RTE transforms template scripts included within the Integration Commons for CMDB app
description: The Robust Transform Engine \(RTE\) transforms are templated operations included within the Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app.
locale: en-US
release: australia
product: CMDB Integration Commons
classification: cmdb-integration-commons
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 19
breadcrumb: [Integration Commons for CMDB, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# RTE transforms template scripts included within the Integration Commons for CMDB app

The Robust Transform Engine \(RTE\) transforms are templated operations included within the Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app.

The following script-based RTE transforms are available in the Integration Commons for CMDB app.

## CI Lookup Operation

Use to get the value of a field on an existing configuration item \(CI\) in the CMDB by the source native key.

<table id="table_bqc_ynv_qwb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine CI Lookup Operation \[sn\_cmdb\_int\_util\_ci\_lookup\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_field** Input in order is:

1.  Discovery Source
2.  Source Native Key
3.  CI Field

The operation queries the Source \[sys\_object\_source\] table for the discovery source and the associated source native key, and then returns the CI Field value of the matching record in the target table and the associated target sys ID.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the value of the field name on the CI matched by the source native key lookup or an empty string if there is no match.

</td></tr></tbody>
</table>The Source \[sys\_object\_source\] table is queried using the discovery source and source native key ordering by the last scan. The table iterates through the results of the query and queries the target table by the target sys ID until a valid CI is found. After a valid CI is found, the operation returns the value of the CI Field on the matching CI.

|Discovery Source|Source Native Key|CI Field|Result|
|----------------|-----------------|--------|------|
|ServiceNow|ServiceNow\|\|\|COMPUTER-NAME\|\|\|Computer-01|name|Computer-01|

## Cleanse Company

Use to cleanse hardware manufacturer name and add the record to the Company \[core\_company\] table to populate a reference, when the manufacturer is not linked to a model or software \(cpu\_manufacturer\).

<table id="table_jfy_3k1_nkb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine Entity Cleanse Company Operation \[sn\_cmdb\_int\_util\_cleanse\_company\_operation\]

</td></tr><tr><td>

Input field

</td><td>

**source\_sys\_rte\_eb\_field** Input is a company/manufacturer name.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the resulting sys\_id and name of the company in core\_company, concatenated by triple pipe \(\|\|\|\).

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationHardwareModelUtil\(\).cleanseCompany\(input\)**

</td></tr></tbody>
</table>If a matching record does not exist, then a new record is created in core\_company so the return always includes a sys\_id and name \(unless the input is empty or invalid\). The name is cleansed and a fuzzy lookup is done via the CmdbIntegrationCompanyModelUtil script include before the MakeAndModelJS platform API is called.

|Input|Result|
|-----|------|
|SERVICENOW|93d4ecfac0a8000b6294d71b733977fb\|\|\|ServiceNow|

## Cleanse Hardware Model

Use to create, cleanse, or lookup a hardware model to create a reference \(model\_id\).

<table id="table_ekx_zl1_nkb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine Entity Cleanse Hardware Model Operation \[sn\_cmdb\_int\_util\_cleanse\_hardware\_model\_operation\]

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Input in order is:

1.  The manufacturer name
2.  The model name

 If either value is provided by itself, then the operation only processes what is found.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the resulting sys\_id and name of the company in core\_company, and sys\_id and name of the model in cmdb\_model - all concatenated by triple pipe \(\|\|\|\).

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationHardwareModelUtil\(\).cleanseModelAndCompany\(manufacturer\_in, model\_in\)**

</td></tr></tbody>
</table>For either the manufacturer or model, if a matching record does not exist then a new record is created so the return always includes sys\_ids and names for both records \(unless the input is empty or invalid\).

The manufacturer name is processed like the Cleanse Company transform and then the manufacturer name and model name are sent to the MakeAndModelJS platform API.

|Manufacturer Name|Model Name|Result|
|-----------------|----------|------|
|ServiceNow Incorporated|SERVICENOW|93d4ecfac0a8000b6294d71b733977fb\|\|\|ServiceNow\|\|\|ba29cb303710200044e0bfc8bcbe5d6d \|\|\|ServiceNow|

## Cleanse Hardware Model with Model Number

Use to create, cleanse, or lookup a hardware model to create a reference \(model\_id\).

<table id="table_yrv_lxm_4yb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine Entity Cleanse Hardware Model With Model Number Operatio \[sn\_cmdb\_int\_util\_cleanse\_hardware\_model\_number\_operation\]

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Input in order is:

1.  The manufacturer name
2.  The model name
3.  The model number
4.  CI Class

**Note:** The `CI Class` field is an optional input field, and when included, the MakeAndModelJS platform API gets the model record by querying the product model class from the Model Category \[cmdb\_model\_category\] table. Else, the API gets the model record from the Hardware Models \[cmdb\_hardware\_product\_model\] table only.


If either value is provided by itself, then the operation only processes what is found.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the resulting sys\_id and name of the company in core\_company, and sys\_id and name of the model in cmdb\_model - all concatenated by triple pipe \(\|\|\|\).

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationHardwareModelUtil\(\).cleanseModelAndCompany\(manufacturer\_in, model\_in\)**

</td></tr></tbody>
</table>For either the manufacturer or model, if a matching record does not exist then a new record is created so the return always includes sys\_ids and names for both records \(unless the input is empty or invalid\).

The manufacturer name is processed like the Cleanse Company transform and then the manufacturer name, model name, and model number are sent to the MakeAndModelJS platform API.

|Manufacturer Name|Model Name|Model Number|Result|
|-----------------|----------|------------|------|
|ServiceNow Incorporated|SERVICENOW|BC0AA8000C56|93d4ecfac0a8000b6294d71b733977fb\|\|\|ServiceNow\|\|\|ba29cb303710200044e0bfc8bcbe5d6d \|\|\|ServiceNow|

## Cleanse IP Address

Use when a field provides an IP address.

<table id="table_qzx_km1_nkb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine Entity Cleanse IP Operation \[sn\_cmdb\_int\_util\_cleanse\_ip\_operation\]

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_field** Input is the IP address to cleanse.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the resulting IP address, which can be empty.

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationNetworkUtil\(\).cleanseIpAddress\(input\)**

</td></tr></tbody>
</table>The IP address is tested for both IPv4 and IPv6 structures along with some known derivations \(an IPv4 with spaces instead of periods\). If a result is found, then it is formatted and returned.

|Ip|Ip Results|
|---|----------|
|192.160.89.1|192.160.89.1|
|192.160.89.1,54.21.12.311|192.160.89.1|
|192 160 89 1 54 21 12 311|192.160.89.1|
|192-160-89-1|192.160.89.1|
|2001:0db8:0000:0000:0000:ff00:0042:8329|2001:0db8:0000:0000:0000:ff00:0042:8329|
|junk| |
|175912537|10.124.54.89|
|-1| |
|0| |

## Cleanse IP Version

Use when the source of data does not provide an IP version or when the IP version might be unreliable.

<table id="table_bnb_bn1_nkb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine Entity Cleanse IP Version Operation \[sn\_cmdb\_int\_util\_cleanse\_ip\_version\_operation\]

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_field** Input is the IP address to cleanse.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the resulting cmdb\_ci\_ip\_address.ip\_version lookup key \(either 4, 6, or empty\).

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationNetworkUtil\(\).deriveIpVersion\(input\)**

</td></tr></tbody>
</table>The input IP address value is checked for either proper IPv4 or IPv6 structure, otherwise the return is empty. This function provides no IP cleansing.

|Input|Result|
|-----|------|
|192.160.89.1|4|

## Cleanse MAC Address

Use when a field provides a MAC address.

<table id="table_o5n_fl1_nkb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine Entity Cleanse MAC Operation \[sn\_cmdb\_int\_util\_cleanse\_mac\_operation\]

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_field** Input is the MAC address to cleanse.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the resulting MAC address which can be empty.

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationNetworkUtil\(\).cleanseMacAddress\(input\)**

</td></tr></tbody>
</table>The MAC address is tested for proper structure along with some known derivations \(for example, a MAC address with spaces instead of colons\). If a result is found, then it is formatted and returned.

|Input|Result|
|-----|------|
|00 0A 95 9D 68 16|00:0a:95:9d:68:16|

## Cleanse Operating System

Use to extract, cleanse, and format an operating system name, when the source provides an operating system value.

<table id="table_pzz_241_nkb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine Entity Cleanse OS Operation \[sn\_cmdb\_int\_util\_cleanse\_os\_operation\]

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_field** Input is the operating system name to cleanse.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the resulting operating system name. The resulting operating system name is also written to the cmdb\_ci\_computer.os list field.

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationOsUtil\(\).cleanseAndInsertOs\(input\)**

</td></tr></tbody>
</table>Most of the current cleansing is centered on Microsoft operating system values aside from common cleansing such as fixing casing.

|Operating System|Operating System Results|
|----------------|------------------------|
|Windows Server 2003 R2 64 bit Edition Service Pack 2|Windows Server 2003 R2|
|Windows 2003|Windows 2003|
|Windows Vista 64 bit Edition|Windows Vista|
|Windows 2000 Professional Service Pack 4|Windows 2000 Professional|
|Windows XP Service Pack 2-3|Windows XP|
|Microsoft Windows Server 2003 R2 64 bit Edition Service Pack 2|Windows Server 2003 R2|
|Microsoft Windows 2003|Windows 2003|
|Microsoft Windows Vista 64 bit Edition|Windows Vista|
|Microsoft Windows 2000 Professional Service Pack 4|Windows 2000 Professional|
|Microsoft Windows XP Service Pack 2-3|Windows XP|
|linux ubuntu|Linux Ubuntu|
|Linux Ubuntu Server|Linux Ubuntu Server|

## Cleanse Serial Number

Use to cleanse and remove invalid serial numbers.

<table id="table_hty_g2d_jmb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine Entity Cleanse Serial Number Operation \[sn\_cmdb\_int\_util\_cleanse\_serial\_number\_operation\]

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Input is the serial number to cleanse.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the resulting serial number.

</td></tr></tbody>
</table>|Serial Number|Serial Number Results|
|-------------|---------------------|
|ec2aa2da-5312-aa3e-804c-c35feabeda5f|ec2aa2da-5312-aa3e-804c-c35feabeda5f|
|1045–1209–6738–4668–7696–2783|1045–1209–6738–4668–7696–2783|

## Cleanse Serial Number With Alternate Value Return if Invalid

Use to cleanse Serial Number and verify the length of the cleansed serial number. Returns the alternate value if the length of serial number is invalid.

<table id="table_mhm_tp1_4cc"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine Entity Cleanse Serial Number With Alternate Value Return \[sn\_cmdb\_int\_util\_cle$anse\_serial\_number\_with\_alternate\_value\_return\_if\_invalid\]

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Inputs: serial number, Alternate value

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output: Cleansed serial number if the length is valid, Alternate value otherwise.

</td></tr><tr><td>

Script include function

</td><td>

**global.SerialNumberManager\(\).isValid\(input\)**

</td></tr></tbody>
</table>The operation cleanses the serial number and checks If the cleansed serial number length is greater than or equal to the value specified in the **sn\_cmdb\_int\_util.minimum\_valid\_serial\_number\_length** system property. The default value of the property is set to `7`.

## Cleanse IMEI Number With Alternate Value Return if Invalid

Use to cleanse the IMEI number and verify the length of the cleansed IMEI number. Returns the alternate value if the length of IMEI number is invalid.

<table id="table_vcg_fs1_4cc"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine Entity Cleanse IMEI With Alternate Value Return if Inval \[sn\_cmdb\_int\_util\_cleanse\_imei\_with\_alternate\_value\_return\_if\_invalid\]

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Inputs: IMEI number, Alternate value

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output: IMEI number if the length is valid, Alternate value otherwise.

</td></tr><tr><td>

Script include function

</td><td>

None

</td></tr></tbody>
</table>The operation cleanses the IMEI number and checks If the cleansed IMEI number length is equal to the value specified in the **sn\_cmdb\_int\_util.valid\_imei\_number\_length** system property. The default value of the property is set to `15`.

## Cleanse Software Model

Use to cleanse and create a software model. Also, to create manufacturer and software model if they do not exist and follow with a split operation.

<table id="table_pyv_h41_nkb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine Entity Cleanse Software Model Operation \[sn\_cmdb\_int\_util\_cleanse\_software\_model\_operation\]

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Input in order is:

1.  The manufacturer name
2.  The software name
3.  The software version \(not required\)

 If only manufacturer or name is provided, then only those values are processed and returned.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the resulting sys\_id and name of the company in core\_company, the cleansed software name, and the cleansed software version all concatenated by a triple pipe \(\|\|\|\).

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationSoftwareModelUtil\(\).cleanseSoftwareModel\(company, model, version\)**

</td></tr></tbody>
</table>If a matching manufacturer record does not exist, then a new record is created so the return always includes the sys\_id and name for the manufacturer \(if the manufacturer is not empty or invalid\).

The manufacturer name is processed the same as in the Cleanse Company transform and then the manufacturer name is sent to the MakeAndModelJS platform API.

The software name and version are cleansed and formatted and returned. The version is removed from the software name if present.

<table id="table_pr2_jp1_nkb"><thead><tr><th>

Manufacturer

</th><th>

Software Name

</th><th>

Software Version

</th><th>

Results

</th></tr></thead><tbody><tr><td>

Dell Inc.

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

 

</td><td>

NoManufacturer

</td><td>

 

</td><td>

 

</td></tr><tr><td>

 

</td><td>

 

</td><td>

1.0.0.0

</td><td>

 

</td></tr><tr><td>

Dell Inc.

</td><td>

DataEngine

</td><td>

1.0.17.2

</td><td>

b7e7d7d8c0a8016900a5d7f291acce5c\|\|\|Dell Inc.\|\|\|DataEngine\|\|\|1.0.17.2

</td></tr><tr><td>

GenuineIntel

</td><td>

TestSoftware

</td><td>

1.0.0.1

</td><td>

7aad6d00c611228400f00e0f80b67d2d\|\|\|Intel\|\|\|TestSoftware\|\|\|1.0.0.1

</td></tr><tr><td>

Dell Inc.

</td><td>

TestSoftware

</td><td>

232

</td><td>

b7e7d7d8c0a8016900a5d7f291acce5c\|\|\|Dell Inc.\|\|\|TestSoftware\|\|\|232

</td></tr><tr><td>

Dell Inc.

</td><td>

TestSoftware

</td><td>

123.0.0.0

</td><td>

b7e7d7d8c0a8016900a5d7f291acce5c\|\|\|Dell Inc.\|\|\|TestSoftware\|\|\|123.0

</td></tr><tr><td>

America Online

</td><td>

TestSoftware

</td><td>

1.0.0.0

</td><td>

0c43d035c61122750000251553f6f8e8\|\|\|America Online\|\|\|TestSoftware\|\|\|1.0

</td></tr><tr><td>

America Online

</td><td>

TestSoftware

</td><td>

1.0.0.0

</td><td>

0c43d035c61122750000251553f6f8e8\|\|\|America Online\|\|\|TestSoftware\|\|\|1.0

</td></tr><tr><td>

dell

</td><td>

LowerCase

</td><td>

1.0.0.0

</td><td>

b7e7d7d8c0a8016900a5d7f291acce5c\|\|\|Dell Inc.\|\|\|LowerCase\|\|\|1.0

</td></tr><tr><td>

Dell Corporation.

 Incorporated, Corp.

</td><td>

TestSoftware

</td><td>

1.0.0.0

</td><td>

b7e7d7d8c0a8016900a5d7f291acce5c\|\|\|Dell Inc.\|\|\|TestSoftware\|\|\|1.0

</td></tr><tr><td>

Microsoft

</td><td>

Microsoft SQL

 Server 2016 Enterprise

</td><td>

2.0.0

</td><td>

0e8b8e650a0a0b3b004f285ffbb1a4fc\|\|\|Microsoft\|\|\|Microsoft SQL Server 2016 Enterprise\|\|\|2.0

</td></tr><tr><td>

Dell Computer

</td><td>

DataEngine

</td><td>

1.0.17.2

</td><td>

b7e7d7d8c0a8016900a5d7f291acce5c\|\|\|Dell Inc.\|\|\|DataEngine\|\|\|1.0.17.2

</td></tr><tr><td>

Adobe

</td><td>

TestSoftware

</td><td>

1

</td><td>

b7e8b5c4c0a80169008b49e468920048\|\|\|Adobe Systems\|\|\|TestSoftware\|\|\|1.0

</td></tr></tbody>
</table>## Create Software Instance Name

Use when a hardware name, software name, and software version is provided, to create a new software instance name.

<table id="table_ryb_cb2_jmb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine Entity Create Software Instance Name Operation \[sn\_cmdb\_int\_util\_create\_software\_instance\_name\_operation\]

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Input in order is:

 1.  The hardware name
2.  The software name
3.  The software version \(not required\)

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the software instance name.

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationSoftwareModelUtil\(\).createSoftwareInstanceName\(hw\_name\_in, sw\_name\_in, sw\_version\_in\)**

</td></tr></tbody>
</table>|Hardware Name|Software Name|Software Version|Results|
|-------------|-------------|----------------|-------|
|computer1|microsoft|2.0.1|microsoft 2.0.1-computer1|
|computer2|adobe| |adobe-computer2|
|computer3|adobe|2.1|adobe 2.1-computer3|
|hw2|sw3|301|sw3 301-hw2|

## Derive CI Class from Model

Use when processing a computer record and a model is provided but the class of the computer is ambiguous otherwise. Can be used along with other Derive CI Class transforms.

<table id="table_xsx_h41_nkb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine Entity Derive Class From Model Operation \[sn\_cmdb\_int\_util\_derive\_class\_from\_model\_operation\]

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Input in order is:

1.  The model name
2.  The current class name

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the resulting class name.

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationClassUtil\(\).deriveClassNameFromModelInput\(model\_in, class\_in\)**

</td></tr></tbody>
</table>Does not return a value of a class which is higher in the class hierarchy \(a parent class\) than the provided input class. For example, does not return cmdb\_ci\_computer if the input is cmdb\_ci\_server. Looks only at the cmdb\_ci\_computer hierarchy, going through cmdb\_ci\_server \(cmdb\_ci\_computer, cmdb\_ci\_server, children of cmdb\_ci\_server\).

Currently looks for Server, Windows Server, and Linux Server indicators in the model.

|Model|Class|Class Results|
|-----|-----|-------------|
|window server|cmdb\_ci\_computer|cmdb\_ci\_win\_server|
|Microsoft server|cmdb\_ci\_computer|cmdb\_ci\_win\_server|
|linux server|cmdb\_ci\_computer|cmdb\_ci\_linux\_server|
|Microsoft server|cmdb\_ci\_server|cmdb\_ci\_win\_server|
|linux server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Red hat server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Arch server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Centos server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Debian server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Fedora server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Suse server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Oracle server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Rhel server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Ubuntu server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Junk| | |
| |cmdb\_ci\_server|cmdb\_ci\_server|
|Junk server|cmdb\_ci\_computer|cmdb\_ci\_server|
|Junk|cmdb\_ci\_computer|cmdb\_ci\_computer|

## Derive CI Class from Native Class Identifier

Use when processing a computer record and a native class indicator is provided but the class of the computer is ambiguous otherwise. Can be used along with other Derive CI Class transforms.

<table id="table_igz_h41_nkb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine Entity Derive Class From Native Value Operation \[sn\_cmdb\_int\_util\_derive\_class\_from\_native\_value\_operation\]

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Input in order is:

1.  The native class identifier
2.  The current class name

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the resulting class name.

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationClassUtil\(\).deriveClassNameFromNativeValue\(native\_id\_in, class\_in\)**

</td></tr></tbody>
</table>Does not return a value of a class which is higher in the class hierarchy \(a parent class\) than the provided input class. For example, does not return cmdb\_ci\_computer if the input is cmdb\_ci\_server. Looks only at the cmdb\_ci\_computer hierarchy, going through cmdb\_ci\_server \(cmdb\_ci\_computer, cmdb\_ci\_server, children of cmdb\_ci\_server\).

Currently looks for Server, Windows Server, and Linux Server indicators in the native identifier.

|Native Class|Class|Class Results|
|------------|-----|-------------|
|window server|cmdb\_ci\_computer|cmdb\_ci\_win\_server|
|Microsoft server|cmdb\_ci\_computer|cmdb\_ci\_win\_server|
|linux server|cmdb\_ci\_computer|cmdb\_ci\_linux\_server|
|Microsoft server|cmdb\_ci\_server|cmdb\_ci\_win\_server|
|linux server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Red hat server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Arch server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Centos server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Debian server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Fedora server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Suse server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Oracle server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Rhel server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Ubuntu server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Junk| | |
| |cmdb\_ci\_server|cmdb\_ci\_server|
|Junk server|cmdb\_ci\_computer|cmdb\_ci\_server|
|Junk|cmdb\_ci\_computer|cmdb\_ci\_computer|

## Derive CI Class from Operating System

Use when processing a computer record and an operating system is provided but the class of the computer is ambiguous otherwise. Can be used along with other Derive CI Class transforms.

<table id="table_uc1_341_nkb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine Entity Derive Class From OS Operation \[sn\_cmdb\_int\_util\_derive\_class\_from\_os\_operation\]

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Input in order is:

1.  The operating system name
2.  The current class name

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the resulting class name.

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationClassUtil\(\).deriveClassNameFromOsName\(os\_in, class\_in\)**

</td></tr></tbody>
</table>Does not return a value of a class which is higher in the class hierarchy \(a parent class\) than the provided input class. For example, does not return cmdb\_ci\_computer if the input is cmdb\_ci\_server. Looks only at the cmdb\_ci\_computer hierarchy, going through cmdb\_ci\_server \(cmdb\_ci\_computer, cmdb\_ci\_server, children of cmdb\_ci\_server\).

Currently looks for Server, Windows Server, and Linux Server indicators in the operating system name.

|Operating System|Class|Class Results|
|----------------|-----|-------------|
|window server|cmdb\_ci\_computer|cmdb\_ci\_win\_server|
|Microsoft server|cmdb\_ci\_computer|cmdb\_ci\_win\_server|
|linux server|cmdb\_ci\_computer|cmdb\_ci\_linux\_server|
|Microsoft server|cmdb\_ci\_server|cmdb\_ci\_win\_server|
|linux server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Red hat server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Arch server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Centos server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Debian server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Fedora server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Suse server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Oracle server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Rhel server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Ubuntu server|cmdb\_ci\_server|cmdb\_ci\_linux\_server|
|Junk| | |
| |cmdb\_ci\_server|cmdb\_ci\_server|
|Junk server|cmdb\_ci\_computer|cmdb\_ci\_server|
|Junk|cmdb\_ci\_computer|cmdb\_ci\_computer|

## Derive Virtual From Hardware Model

Use when processing a computer record that may be virtual, a hardware model is provided, and the virtual status is ambiguous. Can be used along with other Derive Virtual From transforms.

<table id="table_e51_341_nkb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Robust Transform Engine Entity Derive Virtual From Model Operation \[sn\_cmdb\_int\_util\_derive\_virtual\_from\_model\_operation\]

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Input in order is:

1.  The hardware model name
2.  The current virtual flag value

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the resulting virtual flag \(true/false\). If the current virtual flag is ‘true’, the result is true. Otherwise the result is ‘true’ or ‘false’.

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationVirtualDetectionUtil\(\).detectVirtualFromModelName\(model\_in, is\_virtual\_in\)**

</td></tr></tbody>
</table>Looks for indicators in the model name for a virtual device \(VMware\).

|Hardware Model|Virtual Flag|Virtual Flag Results|
|--------------|------------|--------------------|
|thinkpad|true|true|
|thinkpad|false|false|
|thinkpad| |false|
|vmware inc|true|true|
| |true|true|
| |false|false|
| | |false|

## Derive Virtual From Native Indicator

Use when processing a computer record that may be virtual, a virtual indicator is provided by the source, and the virtual status is ambiguous. Can be used along with other Derive Virtual From transforms.

<table id="table_pmb_341_nkb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sn\_cmdb\_int\_util\_derive\_virtual\_from\_native\_value\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Input in order is:

1.  The native indicator
2.  The current virtual flag value

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the resulting virtual flag \(true/false\). If the current virtual flag is ‘true’, the result is true. Otherwise the result is ‘true’ or ‘false’.

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationVirtualDetectionUtil\(\).detectVirtualFromNativeIdentifier\(native\_in, is\_virtual\_in\)**

</td></tr></tbody>
</table>Tests native indicator against a list of common values and looks for a ‘true’ boolean indicator.

|Native Virtual Value|Virtual Flag|Virtual Flag Results|
|--------------------|------------|--------------------|
|virtual|false|true|
|virtual| |true|
|virtual|true|true|
|y|false|true|
|y| |true|
|y|true|true|
|yes|false|true|
|yes| |true|
|yes|true|true|
|true|false|true|
|true| |true|
|true|true|true|
|t|false|true|
|t| |true|
|t|true|true|
|other|false|false|
|other| |false|
|other|true|true|
|not virtual|false|false|
|not virtual| |false|
|not virtual|true|true|
| |false|false|
| | |false|
| |true|true|

## Derive Virtual From Serial Number

Use when processing a computer record that may be virtual, a serial number is provided by the source, and the virtual status is ambiguous. Can be used along with other Derive Virtual From transforms.

<table id="table_qcc_341_nkb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sn\_cmdb\_int\_util\_derive\_virtual\_from\_serial\_number\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Input in order is:

1.  The serial number
2.  The current virtual flag value

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the resulting virtual flag \(true/false\). If the current virtual flag is ‘true’, the result is true. Otherwise the result is ‘true’ or ‘false’.

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationVirtualDetectionUtil\(\).detectVirtualFromSerialNumber \(serial\_in, is\_virtual\_in\)**

</td></tr></tbody>
</table>Looks for indicators in the serial number for a virtual device \(VMware\).

|Serial Number|Virtual Flag|Virtual Flag Results|
|-------------|------------|--------------------|
|123|true|true|
|123|false|false|
|123| |false|
|vmware-123|true|true|
| |true|true|
| |false|false|
| | |false|

## Extract and Scale by Units

Use when the source has numerical values that need to be scaled and numerical value with an input such as 2048Mb. The source does not always provide the units so it may be required to calculate or guess the units being provided. The target units depend on the target field in the CMDB. If not specified, the decimal place field is set at 2 by default.

**Note:** This field is case sensitive.

|Details| |
|-------|---|
|Table|sn\_cmdb\_int\_util\_extract\_and\_scale\_by\_units\_operation|
|Input fields|**source\_sys\_rte\_eb\_fields**|
|Output field|**target\_sys\_rte\_eb\_field**|
|Script include function|**sn\_cmdb\_int\_util.CmdbIntegrationExtractScaleUnitUtil\(\).extractAndScaleUnits\(input,defaultUnit,outputUnit,decimalPlaces\)**|

|Input Value|Default Unit|Output Unit|Result|
|-----------|------------|-----------|------|
|2048Mb|Mb|GB|2GB|
|17179869184|B|GB|16GB|

## First Non Null Value

Use when you have a list of fields providing similar information that must map to a single field and you want to rank the order in which they can provide those values.

For Example Internally in SolarWinds, there is a hierarchy of tables that are join. In one example, a computer’s name could come from the child most table or any of that tables parents but each of those is a separate field in the pull. Starting with the most specific table, the values are searched for the first instance of a name value.

<table id="table_hpc_341_nkb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sn\_cmdb\_int\_util\_first\_non\_null\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Input is a list of fields of any length.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the value from the first field in the list that doesn’t have a null \(or empty\) value.

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationFirstNonNullValueUtil\(\).firstNonNullValue\(batch\[i\]\)**

</td></tr></tbody>
</table>|Field 1|Field 2|Field 3|Result|
|-------|-------|-------|------|
| |foo|foo2|foo|

## Process Name, Domain, FQDN, DNS set

Use when the source provides name, domain, FQDN, or DNS information. Can be used for only a subset of these \(if for example, the source only provides name and domain\). In the case that a source only provides fields that are lower in the input list \(FQDN\) the CmdbIntegrationHardwareNameUtil script include can be called from a script operation to minimize having to create empty dummy fields.

<table id="table_p2d_341_nkb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sn\_cmdb\_int\_util\_process\_name\_set\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Takes up to four Input fieldss \(any additional fields are ignored\), in the following order:

1.  Name
2.  Domain
3.  FQDN
4.  DNS

 You don't have to provide all four input values, but you must provide those values in the specified order. If for example, you only want to cleanse domain, you must provide a name attribute, even it if empty.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is a concatenated set of values in the same order, using a triple pipe \(\|\|\|\): \{name\}\|\|\|\{domain\}\|\|\|\{fqdn\}\|\|\|\{dns\}

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationHardwareNameUtil\(\).processNameDomainFqdnDnsSet\(name, domain, fqdn, dns\)**

</td></tr></tbody>
</table>FQDN and DNS are first processed to see if their formats are correct. FQDN has an additional discovery regex it must pass \(via properties\): `glide.discovery.fqdn.regex – default : ^([^.]+)\\.((?:[^.]+\\.)+[^.]+)$`

Possible name and domain values are extracted if possible. When name and domain are processed, if there is no FQDN, a value is generated if possible. A resulting name value is also modified using the following discovery flags:

1.  glide.discovery.hostname.case – default: No change. Can be set to ‘Lower case’, ‘Upper case’, ‘No change’
2.  glide.discovery.hostname.include\_domain – default: false. If ‘true’ the domain is added to the final name value

|Name|Domain|FQDN|DNS|Results|
|----|------|----|---|-------|
|myName|other.net|otherName.other.net|mycomp.servicenow.com|myName\|\|\|other.net\|\|\|otherName.other.net\|\|\|mycomp.servicenow.com|
|na|other.net|otherName.other.net|mycomp.servicenow.com|otherName\|\|\|other.net\|\|\|otherName.other.net\|\|\|mycomp.servicenow.com|
| | | |servicenow.com|\|\|\|servicenow.com\|\|\|\|\|\||
| | | |name.servicenow.com|name\|\|\|servicenow.com\|\|\|name.servicenow.com\|\|\|name.servicenow.com|
| | |name.servicenow.com| |name\|\|\|servicenow.com\|\|\|name.servicenow.com\|\|\||
| | |name.servicenow.com| |name\|\|\|servicenow.com\|\|\|name.servicenow.com\|\|\||
|name|servicenow.com| | |name\|\|\|servicenow.com\|\|\|name.servicenow.com\|\|\||

## Process FQDN

Use when the source provides a suspected FQDN value but no other naming fields such as name, domain, or DNS.

<table id="table_yd4_vvk_4kb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sn\_cmdb\_int\_util\_process\_fqdn\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_field** Input is a single field containing an FQDN.

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is a concatenated set of values in the same order using a triple pipe \(\|\|\|\): \{name\}\|\|\|\{domain\}\|\|\|\{fqdn\}\|\|\|\{dns\}

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationHardwareNameUtil\(\).processNameDomainFqdnDnsSet\('’, '’, fqdn, '’\)**

</td></tr></tbody>
</table>The processing follows the same logic as the ‘Process Name, Domain, FQDN, DNS set’ transform except that only FQDN is used as an input.

|Input|Result|
|-----|------|
|mycomputer.servicenow.com|mycomputer\|\|\|servicenow.com\|\|\|mycomputer.servicenow.com\|\|\||

## Scale Unit

Use when the source has numerical inputs that must be scaled. The source does not always provide the current units so it may be required to calculate or guess the units being provided. The target units depend on the field being targeted in the CMDB.

<table id="table_p5d_341_nkb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sn\_cmdb\_int\_util\_scale\_unit\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Inputs in order are:

1.  The input value
2.  The current units
3.  The target units

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the input value scaled from the current units to the target units. If no units are found for the current units, then the input value is returned. If no current or target units are found the input is returned as the output.

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationScaleUnitUtil\(\).scaleUnits\(input\_value, input\_unit, output\_unit\)**

</td></tr></tbody>
</table><table id="table_wnt_by1_bmb"><thead><tr><th>

Input

</th><th>

Result

</th></tr></thead><tbody><tr><td>

-   Input Field 1: 1
-   Input Field 2: GB
-   Input Field 3: MB

</td><td>

1024

</td></tr></tbody>
</table>## Software Bundle ID Lookup

Use when a source, such as Jamf, does not provide the software publisher but does provide a Mac software bundle ID. Software Bundle ID Lookup looks up records in the Bundleid Lookup \[sn-cmdb\_int\_util\_bundleid\_lookup\] table by bundle\_id. If a record with the specified bundle\_id exists, it extracts the respective software publisher. Otherwise, it creates a new record which will be queried the next time the Lookup Mac Software Bundle IDs data source runs.

<table id="table_gwq_yzw_kqb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sn\_cmdb\_int\_util\_software\_bundle\_id\_lookup\_operation

</td></tr><tr><td>

Input fields

</td><td>

-   source\_sys\_rte\_eb\_field
-   Bundle ID

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** Output is the resulting artist name, track name, and seller name, all concatenated by a triple pipe \(\|\|\|\), or an empty string if no match is found.

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationSoftwareBundleIdLookup. lookupSoftware\(bundleId\)**

</td></tr></tbody>
</table>|Input|Result|
|-----|------|
|Input Field 1: com.microsoft.Word|Microsoft Corporation\|\|\|Microsoft Word\|\|\| Microsoft Corporation|

## User Lookup

Use to look up a user in the User \[sys\_user\] table by user name or email, attempting to match in the following order:

1.  The User Name matching the **user\_name** attribute.
2.  The Email matching the email attribute.
3.  If nothing is matching, it returns empty.

<table id="table_ksx_t2x_kqb"><thead><tr><th colspan="2">

Details

</th></tr></thead><tbody><tr><td>

Table

</td><td>

sn\_cmdb\_int\_util\_user\_lookup\_operation

</td></tr><tr><td>

Input fields

</td><td>

**source\_sys\_rte\_eb\_fields** Inputs in order are:

1.  User Name
2.  Email \(Optional\)

</td></tr><tr><td>

Output field

</td><td>

**target\_sys\_rte\_eb\_field** sysId of the sys\_user.

</td></tr><tr><td>

Script include function

</td><td>

**sn\_cmdb\_int\_util.CmdbIntegrationUserLookup. lookupUser\(username, email\)**

</td></tr></tbody>
</table><table id="table_lsx_t2x_kqb"><thead><tr><th>

Input

</th><th>

Result

</th></tr></thead><tbody><tr><td>

Input Field 1: abel.tuter

</td><td>

62826bf03710200044e0bfc8bcbe5df1

</td></tr><tr><td>

-   Input Field 1: atuter
-   Input Field 2: abel.tuter@example.com

</td><td>

62826bf03710200044e0bfc8bcbe5df1

</td></tr></tbody>
</table>