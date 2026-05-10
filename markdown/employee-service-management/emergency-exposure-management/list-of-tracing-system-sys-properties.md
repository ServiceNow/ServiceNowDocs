---
title: System properties for tracing systems in Emergency Exposure Management
description: System properties associated with tracing systems that are available in the Emergency Exposure Management application.
locale: en-US
release: australia
product: Emergency Exposure Management
classification: emergency-exposure-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Tracing systems in Emergency Exposure Management, Set up Emergency Exposure Management, Emergency Exposure Management, Emergency Response Management, Employee Service Management]
---

# System properties for tracing systems in Emergency Exposure Management

System properties associated with tracing systems that are available in the Emergency Exposure Management application.

To configure the system properties available for a tracing system, navigate to **Emergency Exposure Management** &gt; **Administration** &gt; **Tracing Systems** and open the tracing system record.

For more information on setting up or modifying a tracing system, see [Set up a tracing system for an exposure data source](../task/set-up-tracing-system.md).

## System properties for tracing systems installed with Contact Tracing

For more information, see [Setting up Contact Tracing](../../contact-tracing/concept/set-up-contact-tracing.md).

<table id="table_slw_cd1_w4b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Tracing system: Badge reader

</td></tr><tr><td>

**sn\_imt\_tracing.badge\_data\_page\_size**

</td><td>

Number of records to process at a time for badge reader data. The default value is 500.

</td></tr><tr><td>

**sn\_imt\_tracing.badge\_reader\_location**

</td><td>

The field in the Badge Access Register \[sn\_imt\_tracing\_badge\_access\_register\] table that refers to the location of the badge reader when the **Use badge reader** option is selected on the Diagnostic Request form. You can also specify a dot-walked field, for example, floor.floor\_name. The default value is the floor\_name field in the \[sn\_imt\_tracing\_badge\_reader\] table.

</td></tr><tr><td>

**sn\_imt\_tracing.badge\_owner\_field**

</td><td>

The field in the Badge Access Register \[sn\_imt\_tracing\_badge\_access\_register\] table that refers to the badge owner when the **Use badge reader** option is selected on the Diagnostic Request form. You can also specify a dot-walked field, for example, user.user\_name. The default value is the user field in the \[sn\_imt\_tracing\_user\_badge\] table.

</td></tr><tr><td class="sub-head" colspan="2">

Tracing system: Wi-Fi access log

</td></tr><tr><td>

**sn\_imt\_tracing.wifi\_client\_table**

</td><td>

The CMDB Class table to look up to identify the device and owner matching the Wi-Fi client in Wi-Fi access logs. The default value is cmdb\_ci\_computer.

</td></tr><tr><td>

**sn\_imt\_tracing.wifi\_client\_mac\_field**

</td><td>

The field in the CMDB Class \[cmdb\_ci\_computer\] table that stores the mac address of the Wi-Fi client. The default value is mac\_address.

</td></tr><tr><td>

**sn\_imt\_tracing.wifi\_client\_owner\_field**

</td><td>

The field in the CMDB Class \[cmdb\_ci\_computer\] table that identifies the owner of the Wi-Fi client from the Wi-Fi access logs. The default value is assigned\_to.

</td></tr><tr><td>

**sn\_imt\_tracing.wifi\_client\_identification\_fields**

</td><td>

The fields in the CMDB Class \[cmdb\_ci\_computer\] table that identify the Wi-Fi client matching the Wi-Fi client in the Wi-Fi access log. The default values are mac\_address, name.

</td></tr><tr><td>

**sn\_imt\_tracing.wifi\_ble\_client\_table**

</td><td>

The CMDB Class table to look up to identify the device and owner matching the Wi-Fi Bluetooth LE \(BLE\) client in the Wi-Fi access logs. The default value is cmdb\_ci\_wearable.**Note:** The Wearable Technology table \[cmdb\_ci\_wearable\] is installed with the CMDB CI Class Models application available through the ServiceNow Store. For more information, see [CMDB CI Class Models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-iot.md).

</td></tr><tr><td>

**sn\_imt\_tracing.wifi\_ble\_client\_mac\_field**

</td><td>

The field in the CMDB Class \[cmdb\_ci\_wearable\] table that stores the mac address of the Wi-Fi BLE client. The default value is mac\_address.

</td></tr><tr><td>

**sn\_imt\_tracing.wifi\_ble\_client\_owner\_field**

</td><td>

The field in the CMDB Class \[cmdb\_ci\_wearable\] table that identifies the owner of the Wi-Fi BLE client from the Wi-Fi access logs. The default value is assigned\_to.

</td></tr><tr><td>

**sn\_imt\_tracing.wifi\_ble\_client\_identification\_fields**

</td><td>

The fields in the CMDB Class \[cmdb\_ci\_wearable\] table that identify the Wi-Fi asset matching the Wi-Fi BLE client in the Wi-Fi access log. The default values are mac\_address,asset\_tag.

</td></tr><tr><td class="sub-head" colspan="2">

Tracing system: Mist systems

</td></tr><tr><td>

**sn\_imt\_tracing.mist\_api**

</td><td>

API that accesses the Wi-Fi access logs from Mist Systems. The default value is https://api.mist.com/api/v1. **Note:** This property applies only if you collect Wi-Fi access logs using Mist Systems.

</td></tr><tr><td>

**sn\_imt\_tracing.mist\_visits\_page\_size**

</td><td>

Maximum number of records to process by Mist Systems API calls. The default value is 1000.**Note:** This property applies only if you collect Wi-Fi access logs using Mist Systems.

</td></tr><tr><td class="sub-head" colspan="2">

Tracing system: Cisco DNA Spaces

</td></tr><tr><td>

**sn\_imt\_tracing.wifi\_proximity\_preference**

</td><td>

Level of proximity to consider employee interaction with an affected employee as potential exposure. The available options are `30ft`, `Floors`, or `Buildings`. The default value is 30ft.**Note:** This property applies only if you collect proximity reports using Cisco DNA Spaces.

</td></tr><tr><td colspan="2">

Properties that apply only if you collect Wi-Fi raw data from Cisco DNA Spaces using Wi-Fi raw data files

</td></tr><tr><td>

**sn\_imt\_tracing.wifi\_log\_sftp\_server**

</td><td>

URL or IP Address \(for example, 192.168.1.1\) of the secured FTP \(SFTP\) server from which to access the Wi-Fi raw data files imported into the Wi-Fi Access Register \[sn\_imt\_tracing\_wifi\_access\_register\] table.

</td></tr><tr><td>

**sn\_imt\_tracing.wifi\_log\_sftp\_port**

</td><td>

Port on the SFTP server to allow an FTP connection to access the files.

</td></tr><tr><td>

**sn\_imt\_tracing.wifi\_log\_sftp\_file\_path**

</td><td>

File path on the SFTP server where the Wi-Fi access data files from Cisco DNA Spaces are stored.For example, in the file path `/upload/Visit Data/Daily/ServiceNow_Daily_Visits_:`

 -   `/upload/Visit Data/Daily/` is the folder location on the SFTP server where the files are stored.

-   `ServiceNow_Daily_Visits_` is the first part of the default file name that Cisco DNA Spaces uses, followed by the date and the upload time.


 For example, the default file name for the Wi-Fi access data for 19 August 2020 at 0100 UCT would be `ServiceNow_Daily_Visits_2020-08-19 0100 UTC.csv`:

-   `ServiceNow_Daily_Visits_` is a fixed value
-   `2020-08-19` is the date the Wi-Fi access data was captured
-   `0100 UTC` is the time scheduled by you for Cisco DNA Spaces to upload the file

 **Note:** Make sure that only a limited number of users have read and write access to this location.

</td></tr><tr><td>

**sn\_imt\_tracing.wifi\_log\_sftp\_load\_time**

</td><td>

Time in HH:mm format when the Cisco DNA Spaces system uploads the day's Wi-Fi access data files on the SFTP server. This timestamp is the last part of the name of the Wi-Fi access data file.

</td></tr><tr><td>

**sn\_imt\_tracing.wifi\_log\_sftp\_username**

</td><td>

User name required to log in to the SFTP server.**Note:** Make sure that the SFTP user is not a privileged user such as an administrator. Assign the minimal privilege required to read the files in the directory set in the **sn\_imt\_tracing.wifi\_log\_sftp\_file\_path** property.

</td></tr><tr><td>

**sn\_imt\_tracing.wifi\_log\_sftp\_password**

</td><td>

Password required to log in to the SFTP server.

</td></tr><tr><td>

**sn\_imt\_tracing.wifi\_log\_cisco\_tier**

</td><td>

Integration tier with Cisco DNA Spaces to fetch Wi-Fi access data. The available options are proximity\_report and wifi\_log\_report.**Note:** This property applies only if you are using integration with Cisco DNA Spaces to get the Wi-Fi access data.

</td></tr><tr><td class="sub-head" colspan="2">

Tracing system: Kinexon SafeZone

</td></tr><tr><td>

**sn\_imt\_tracing.kinexon\_api\_endpoint**

</td><td>

API endpoint used to log in to the KINEXON SafeZone instance and access KINEXON data. This API endpoint is also used to fetch information required for Contact Tracing. Replace the default endpoint with the endpoint of your instance.

</td></tr><tr><td>

**sn\_imt\_tracing.kinexon\_api\_username**

</td><td>

KINEXON administrator user name.

</td></tr><tr><td>

**sn\_imt\_tracing.kinexon\_api\_password**

</td><td>

KINEXON administrator password.

</td></tr><tr><td>

**sn\_imt\_tracing.kinexon\_api\_param\_min\_duration**

</td><td>

The minimum duration of contact \(in seconds\) between two KINEXON sensors required to determine whether a user is a potentially exposed contact. The query omits all records with values below this duration. The default value is `300`.

</td></tr><tr><td>

**sn\_imt\_tracing.kinexon\_api\_param\_min\_acc\_duration**

</td><td>

The minimum total duration \(in seconds\) of all contact between two KINEXON sensors within the queried date range. If the total duration is shorter than this value, the query omits all records of contact between the pair of sensors. The default value is `300`.

</td></tr><tr><td>

**sn\_imt\_tracing.kinexon\_api\_param\_max\_distance**

</td><td>

The maximum distance \(in meters\) between two KINEXON sensors that determines whether users are in contact. The query omits any instances of contact beyond this distance. The default value is `2`.

</td></tr><tr><td>

**sn\_imt\_tracing.kinexon\_api\_param\_max\_time\_gap\_in\_sequence**

</td><td>

Determines the amount of time that can pass \(in seconds\) between any two consecutive instances of contact before the potential exposure is considered two potential exposures. The default value is `15`.

</td></tr></tbody>
</table>