---
title: File-based Discovery issue resolution
description: If you have any issues while setting up or running File-based Discovery, follow the actions listed here to help resolve them.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-25"
reading_time_minutes: 1
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

Check the Internal properties managed by the Discovery \[discovery\_private\_properties\] table for the following items. To view this table, enter **discovery\_private\_properties.list** in the navigation filter and press **Enter**.-   File\_discovery.file\_extensions\_windows should contain a list of Windows file extensions to be scanned.
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

</td></tr></tbody>
</table>**Related topics**  


[File-based Discovery references](file-based-discovery-references.md)

