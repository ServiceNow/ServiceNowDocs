---
title: File-based Discovery issue resolution
description: If you have any issues while setting up or running File-based Discovery, follow the actions listed here to help resolve them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/file-based-discovery-troubleshooting.html
release: brazil
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-10-13"
reading_time_minutes: 2
breadcrumb: [File-based Discovery references, File-based Discovery, Running discoveries in your network, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# File-based Discovery issue resolution

If you have any issues while setting up or running File-based Discovery, follow the actions listed here to help resolve them.

<table id="table_v13_l1v_phb"><thead><tr><th>

Issue

</th><th>

Cause/Action

</th></tr></thead><tbody><tr><td>

Error message: File Discovery data not yet synced...

</td><td>

-   Allow Content Data Service \(CDS\) time to synchronize the samp\_file\_\* tables. Initial synchronization can take approximately 24 hours.
-   Review the Data Services: Download Schedules \(cds\_client\_schedule\) table to check if the timestamp has been updated for “samp\_file\_\*” tables.

</td></tr><tr><td>

File-based Discovery is not triggered during discovery.

</td><td>

-   Feature has not been enabled. Check the Discovery Definition Configuration Console and verify that File-based Discovery is enabled.
-   Interval between scans is too long. Check the interval setting on the Discovery Definition Configuration Console.

</td></tr><tr><td>

File-based Discovery is not triggered during discovery.

</td><td>

Check the Internal properties managed by the Discovery \[discovery\_private\_properties\] table for the following items. To view this table, enter `discovery_private_properties.list` in the navigation filter and press **Enter**.-   File\_discovery.file\_extensions\_windows should contain a list of Windows file extensions to be scanned.
-   File\_discovery.unix\_filename\_timestamp should be something other than 1970 timestamp.
-   File\_discovery\_windows\_filename.timestamp should be something other than 1970 timestamp.

If either timestamp shows 1970, CDS content hasn't downloaded yet. To trigger an immediate download, navigate to the Data Services: Download Schedules \(cds\_client\_schedule\) table and search for records where the **Table** field is `samp_file_name`, `samp_file_map`, or `samp_file_set`. Open each record and select **Execute Now**. To verify the download, navigate to **System Logs &gt; Outbound HTTP Requests** and confirm the **Response status** is 200 for requests where the **URL hostname** is `sncdataservices.service-now.com`.

</td></tr><tr><td>

Errors in MID Server log from FileDiscoveryFilter or MID Server issue created.

</td><td>

-   Check if the File-based discovery inclusion list exists. The inclusion list is in the MID Server installation folder in `/agent/work`. If it does not exist, the synchronization did not succeed.
-   Review the MID Server record on the instance to see if a MID Server issue was created.
-   MID Server uses the GetMIDInfo scripted soap service to synchronize the inclusion list. See if errors are generated from this script.
-   Select the **File discovery filter refresh** Related Link in the MID Server record to synchronize the file names to this MID Server.

</td></tr><tr><td>

PowerShell errors

</td><td>

-   Include the script in your anti-virus software.
-   Add ServiceNow publisher to your trusted publisher repository.

</td></tr><tr><td>

The **Version** field is empty in the File Information \[cmdb\_file\_information\] table for Linux or UNIX devices.

</td><td>

This is expected behavior. The Unix - File Discovery probe returns file name and file size only for Linux and UNIX devices. It is not designed to return version metadata, so the **Version** field is empty for those devices by design.

 Linux software versions in the Software Installation \[cmdb\_sam\_sw\_install\] table are populated by the rpm- and dpkg-based discovery probes, such as the Linux - Install Software probe. File-based Discovery does not populate this table.

 To obtain version information for software on Linux and UNIX devices, enable SWID tag scanning for products that provide valid SWID tags. SWID tags include version data and populate the Swid Tags \[cmdb\_swid\_tag\] table. Enable SWID tag scanning selectively for products known to provide valid SWID tags rather than enabling it across all servers. For more information, see [File-based Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/file-based-discovery.md).

</td></tr></tbody>
</table>**Related topics**  


[File-based Discovery references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/file-based-discovery-references.md)

