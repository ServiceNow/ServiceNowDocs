---
title: Set the MID Server JVM memory size
description: The MID Server starts with a default JVM memory allocation, but you can modify this setting in the configuration file.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/t\_MIDServerOptionalConfiguration.html
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Set the MID Server JVM memory size

The MID Server starts with a default JVM memory allocation, but you can modify this setting in the configuration file.

## Before you begin

Role required: admin

<table id="table_l5y_xrf_khb"><tbody><tr><td>

![Links to each of the MID Server sections](../image/MIDRefIconBar.png)

</td></tr></tbody>
</table>## About this task

In the base ServiceNow system, the MID Server JVM memory is set to 1024 MB, which is configured in the `\agent\conf\wrapper-override.conf` file in the MID Server installation directory. This setting might not be appropriate for the way your organization uses the MID Server. If you want the MID Server to work harder, allocate more resources to it. If the MID Server is located in a small branch office and runs in an environment where memory allocation is shared between a print server, mail server, or web proxy server, the allocation might have to be reduced.

**Note:** For a complete list of minimum MID Server requirements, see [MID Server system requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerSystemRequirements.md).

## Procedure

1.  Open the `\ServiceNow\<MID Server name>\agent\conf\wrapper-override.conf` file in a text editor.

    For more information about this file, see [Installing Multiple MID Servers on a Single System](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_InstallMultplMIDSvrOnASingleSys.md).

2.  Locate the following lines in the file:

    ```
    # OPTIONAL: Maximum Java Heap Size (in MB)
    wrapper.java.maxmemory=1024
    ```

3.  Edit the memory allocation.

4.  Remove the comment tag \(\#\) from the memory allocation parameter.

5.  Save the file.

6.  Restart the MID Server service.


**Parent Topic:**[MID Server reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-reference-information.md)

**Related topics**  


[MID Server system requirements]()

[MID Server upgrades]()

[Resolving MID Server issues]()

[MID Server dashboard]()

[MID Server properties]()

[MID Server parameters]()

[MID Server Configuration Parameter settings and priority]()

[MID Server File Cleaner]()

[MID Server protected records and reserved characters]()

[MID Server privileged commands]()

[MIDSystem methods]()

[Manually start, stop, and restart a MID Server]()

[MID Server heartbeat]()

[Pause the MID Server]()

