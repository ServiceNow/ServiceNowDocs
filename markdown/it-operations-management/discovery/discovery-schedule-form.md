---
title: Discovery Schedule form reference
description: The Discovery Schedule form provides details about the configuration items \(CIs\) targeted for discovery, the associated MID Server, and the schedule settings for when and how the discovery runs.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-05-01"
reading_time_minutes: 10
breadcrumb: [Discovery reference, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Schedule form reference

The Discovery Schedule form provides details about the configuration items \(CIs\) targeted for discovery, the associated MID Server, and the schedule settings for when and how the discovery runs.

For instructions on this procedure, see [Schedule a horizontal discovery](../task/t_CreateADiscoverySchedule.md#).

<table id="table_xnx_zrb_5p"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="row_name578654"><td>

Name

</td><td>

Enter a unique, descriptive name for your schedule.

</td></tr><tr><td>

Discover

</td><td>

Select one of the following scan types:-   **Configuration items**: Uses Discovery identifiers to match devices with CIs in the CMDB and update the CMDB appropriately. Perform a simple discovery by selecting a specific MID Server to scan for all protocols \(SSH, WMI, and SNMP\). Or, perform advanced discoveries with discovery behaviors. When you select a behavior, the MID Server field isn’t available.

**Note:** An IPv6 via address list scan is enabled on Discovery schedule for Configuration Items.

-   **IP addresses**: Scans devices without the use of credentials. These scans discover all the active IP addresses in the specified range and create device history records, but don’t update the CMDB. IP address scans also show multiple IP addresses that are running on a single device. Identify devices by class and by type, such as Windows computers and Cisco network gear. The Max range size Shazzam probe property determines the maximum number of IP addresses Shazzam scans. See [Configure Shazzam probe](../task/t_ConfigureTheShazzamProbe.md#) for details.
-   **Networks**: Discovers IP networks \(routers and switches\). Results from this search are used to populate the IP Network \[cmdb\_ci\_ip\_network\] table in **Discovery** &gt; **IP Networks** with a list of IP addresses and network masks. Network scans update routers and layer 3 switches in the CMDB.
-   **Service**: Discovers services for the Service Mapping application. See [Schedule a top-down discovery by Service Mapping](../../service-mapping/task/t_CreateDiscoSchedForCITypes.md) for instructions.
-   **Serverless**: Finds CIs without needing to run discovery on a host, or CIs on a proxy host that is already in the CMDB. See [Serverless Discovery](../concept/serverless-discovery.md) for more information.
-   **Cloud application**: Discovers only the cloud resources for the patterns that you specify. See [Discovery for cloud environment](../concept/cloud-discovery-wizard.md) for instructions.
-   **Cloud resources**: Discovers resources for one of the supported [cloud providers](../concept/cloud-discovery-wizard.md). This option only appears when you [run Discovery](../concept/discovery-manager.md#) on a cloud service account. You can’t select it from a new Discovery schedule.
-   **Certificates**. Discovers certificates based on URLs. Selecting this option adds the Certificate Discovery Type field: URL Certificate Discovery. See [Run Certificate Discovery via individual URL scans](../task/run-cert-inventory-mgmt-urls.md) for more information.

</td></tr><tr><td>

MID Server selection method

</td><td>

Select the method that Discovery uses to select a MID Server:-   **Auto-Select MID Server**: Enable Discovery to select the MID Server automatically based on the discovery IP ranges you configure. To find a matching MID Server, you must configure MID Servers to use:

    -   The Discovery application, or ALL applications. This setting authorizes the MID Server access from Discovery.
    -   The IP range that includes the ranges you configure on the discovery schedule.
**Note:** MID Server auto-select isn’t supported with IPv6.

-   **Specific MID Cluster**: Use a preconfigured cluster of MID Servers. Select the cluster. You aren’t required to specify one member of the cluster. The MID Server can’t be part of multiple clusters, such as one that supports load balancing and one that supports failover. You can add any cluster regardless of the application that the MID Servers are assigned to. When you select the cluster, the **Discovery** application is automatically added when it doesn’t exist for the MID Servers in the cluster.
-   **Specific MID Server**: Use only one MID Server. If that MID Server is part of a cluster, only that MID Server is used. The cluster isn’t used. You can add any MID Server regardless of the application it’s assigned to. The **Discovery** application is automatically added when it isn’t already assigned for the MID Server you select. You can assign a specific MID Server for all types of Discover scans except **Service**.
-   **Use Behavior**: [Use a behavior](../task/create-disco-behavior.md) when a single schedule requires the use of multiple MID Servers to perform any of the following activities:
    -   Scans requiring multiple Windows credentials.
    -   A schedule that must execute two or more particular protocols \(SNMP, SSH, or WMI\) using more than one MID Server.
    -   Load balancing for large discoveries where a single MID Server would be inadequate.
    -   Scanning multiple domains.

 **Note:** The discovery schedule enforces domain separation. The MID Servers that are available for selection are limited to the same domain of the user who is configuring the schedule.

 See [MID Server selection sequence for Discovery schedules](../task/t_CreateADiscoverySchedule.md#) for additional information.

</td></tr><tr><td>

MID Server

</td><td>

Select the MID Server to use for this schedule. This field is available if MID Server selection method is set to Specific MID Server, or if you discover IP addresses, networks, or web services.To verify that the MID Server you selected is up and validated, look at the [MID Server dashboard](https://www.servicenow.com/docs/access?context=c_MIDServerDashboard&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

MID Server Cluster

</td><td>

Select the MID Server cluster to use for this schedule. This field is available if MID Server selection method is set to Specific MID Cluster.

</td></tr><tr><td>

Behavior

</td><td>

Select a behavior configured for the MID Servers in your network. This field is available only if MID Server selection method is set to Use Behavior.

</td></tr><tr id="row_Active739273"><td>

Active

</td><td>

Select the check box to enable this schedule. If you clear the check box, the schedule is inactive, but you can still run a discovery manually from this form, using the configured values.

</td></tr><tr><td>

Location

</td><td>

Choose a location to assign to the CIs that the schedule discovers. If this field is empty, then no location is assigned.

</td></tr><tr id="row_MaxRunTime787656"><td>

Max run time

</td><td>

Set a time limit for running this schedule. When the configured time elapses, the remaining tasks for the discovery are canceled, even if the scan isn’t complete. Use this field to limit system load to a desirable time window. If no value is entered in this field, this schedule runs until complete.

</td></tr><tr><td>

Max Idle time

</td><td>

Set a time limit for inactivity during discovery to automatically cancel stalled processes and log the event. A discovery is considered idle only when no input records are being processed and nothing is left in the processing state. Idle time is measured from the most recent change to an ECC Queue record. The configured idle time is fixed at the start of the discovery and won’t reflect any edits until the next run. If no value is entered in this field, this schedule runs until complete or canceled.**Note:** By default, the **Max Idle time** field doesn’t display in the Discovery Schedule form. To include this parameter, open the Discovery Schedules \[discovery\_schedule\] table, add the column, and configure the Max Idle time directly in the table. For information about customizing columns in tables, see [Personalize a list](https://www.servicenow.com/docs/access?context=c_PersonalLists&version=zurich&pubname=zurich-platform-user-interface&section=t_PersonalizeAList&ft:locale=en-US).

</td></tr><tr id="row_Run893873"><td>

Run and related fields

</td><td>

Determines the run schedule of the discovery. Configure the frequency in the **Run** field and the other fields that appear to specify an exact time. **Note:** The run time uses the system time zone. If you add the optional **Run as tz** field, it has no effect on the actual runtime.

</td></tr><tr><td>

Log state changes

</td><td>

Select this check box to create a log entry every time the state changes during a discovery, such as a device going from Active to Classifying. View the discovery states from the Discovery Devices related list on the Discovery Status form. The Completed activity and Current activity fields display the states.

</td></tr><tr><td>

Shazzam batch size

</td><td>

Enter the number of IP addresses that each Shazzam probe can scan. Dividing the IP addresses into batches improves performance by enabling classification for each batch to begin after the batch completes, rather than after all IP addresses have been scanned. The probes run sequentially. For example, the value is set to 1000 and a discovery scans 10,000 IP addresses using a single MID Server. It creates 10 Shazzam probes with each probe scanning 1000 IP addresses. By default, the batch size is 1000. A UI policy enforces a minimum batch size of 256 because batch sizes below 256 IP addresses don’t benefit from clustering. The policy converts any value below 256 to a value of zero.The value for this field can’t exceed the value defined in the maximum range size property for the Shazzam probe.

</td></tr><tr><td>

Discovery Agent

</td><td>

Select the agent to perform this discovery:-   **AWS MID**: Use AWS SSM to perform discovery.
-   **MID**: Use the MID Server to perform discovery.

By default, the Discovery Agent is set to MID. This field is available only when the system property **glide.discovery.enable\_ssm** is enabled, the **Discover** type is set to **Configuration Items**, and the **Run after** field is configured to follow a Cloud Resources schedule.

</td></tr><tr><td>

Shazzam cluster support

</td><td>

Select the check box to distribute Shazzam processing among multiple MID Servers in a cluster and improve performance. This setting works with the Shazzam batch size. For example, a schedule is created to scan 100,000 IP addresses, with 10 MID Servers assigned to do the work. Each MID Server is assigned to scan 10,000 IP addresses. If the Shazzam batch size is set to 5,000 IP addresses per probe, the schedule runs two Shazzam probes per MID Server \(10,000 IP addresses/5,000 per batch\). These probes are run in sequence and not concurrently.

</td></tr><tr><td>

Use SNMP Version

</td><td>

Use this field to designate the SNMP version to use for this discovery. The default value is **ALL**. You can change this value to **v1**, **v2c**, or **v3**.

</td></tr><tr><td>

URL Certificate Batch Size

</td><td>

Define the number of URLs to discover per batch during discovery. Leave the batch size as it is unless recommended to change.

</td></tr><tr><td>

Quick ranges

</td><td>

Define IP addresses and address ranges to scan by entering IP addresses in multiple formats \(network, range, or list\) in a single, comma-delimited string. For more information, see [Create a Quick IP range for a Discovery schedule](discovery-ip-address-configuration.md#).

</td></tr><tr><td>

Discover now

</td><td>

Use this link to immediately start this Discovery.

</td></tr><tr><td colspan="2">

**Related lists**

</td></tr><tr><td>

IP Ranges

</td><td>

This related list defines the ranges of IP addresses to scan with this schedule. If you’re using a simple CI scan \(no behaviors\), use this related list to define the IP addresses to discover. **Note:** To improve security, limit the range of discovery targets to exclude unnecessary networks and devices.

</td></tr><tr><td>

Discovery Range Sets

</td><td>

This related list defines each range set in a schedule to scan by one or more Shazzam probes.

</td></tr><tr><td>

Discovery Status

</td><td>

This related list displays the results of current and past schedule runs.

</td></tr><tr><td>

Certificate URLs

</td><td>

This related list displays the URLs that are discovered using this schedule. You can add or delete URLs from this list.

</td></tr></tbody>
</table>**Parent Topic:**[Discovery reference](discovery-references.md)

