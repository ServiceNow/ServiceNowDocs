---
title: Schedule a horizontal discovery
description: A discovery schedule determines what horizontal discovery searches for, when it runs, and which MID Servers are used. Create a discovery schedule for your local environment or a schedule for discovering the resources in your cloud service account.Quick Discovery, or DiscoverNow, allows an administrator to run a CI Configuration discovery on a single IP address without requiring a schedule.You can run DiscoverNow from a script, such as a background job, a business rule, or web services.Validate the results of your discovery by accessing the ECC queue, analyzing the XML payload, and checking the Discovery log.The Discovery application follows this sequence to find a MID Server.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Running discoveries in your network, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Schedule a horizontal discovery

A discovery schedule determines what horizontal discovery searches for, when it runs, and which MID Servers are used. Create a discovery schedule for your local environment or a schedule for discovering the resources in your cloud service account.

## Before you begin

Ensure that your Discovery schedule conforms to security best practices, such as limiting the range of discovery targets and using the most secure credentials.

Make sure to [test your credentials](https://www.servicenow.com/docs/access?context=t_CreateCredential&version=australia&pubname=australia-platform-security&ft:locale=en-US) before you run a schedule. Bad credentials are a leading cause of failed discoveries.

Roles required: discovery\_admin or admin

## About this task

You can use a Discovery schedule to launch horizontal discovery, which uses probes, sensors, and pattern operations to scan your network for CIs. Use this procedure to create a schedule manually from the **Discovery Schedules** form.

Service Mapping also provides a Discovery schedule for top-down discovery. See [Schedule a top-down discovery by Service Mapping](../../service-mapping/task/t_CreateDiscoSchedForCITypes.md) for more information.

Use the **Discovery Schedules** module in the Discovery application to:

-   Configure a schedule to discover resources in your cloud service account.
-   Configure a schedule to discover certificates from URL scans.
-   Configure device identification by IP address or other identifiers.
-   Determine if credentials are used in device probes.
-   Name the MID Server to use for a particular type of discovery.
-   Create or disable a schedule that controls when the discovery runs in your network.
-   Configure the use of multiple Shazzam probes for load balancing.
-   Configure the use of multiple MID Servers for load balancing.
-   Run a discovery schedule manually.
-   Run a discovery on a single IP address.

**Note:** To view the run-results of your schedules for both IP-based and Cloud Discovery, use the summaries on the [Discovery Home page](../concept/discovery-home-page.md#). The Home page publishes the details of any errors that might have occurred and displays possible actions to take to remediate problems.

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules** to create a new record.

2.  Select the type of schedule to open:

    -   **New**: Creates a new horizontal schedule for discovering components in your network.
    -   **Quick Discovery**: Runs a horizontal discovery on a single IP address without requiring a schedule.
    -   **Create a Cloud Discovery schedule**: Creates a schedule, using the Discovery Manager wizard, for discovering resources in a cloud service account.
3.  Complete the Discovery schedule form, using the fields in the table.

    For more information, see [Discovery Schedule form reference](../reference/discovery-schedule-form.md).

4.  Right-click in the header of the record and select **Save** from the context menu.

5.  To create a range of IP addresses to discover, click **Quick Ranges** under **Related Links**.

    **Note:** To improve security, limit the range of discovery targets to exclude unnecessary networks and devices.

6.  Define the frequency of schedule running as described in [Run options for discovery schedules](../../it-operations-management/reference/discovery-schedule-run-options.md).


## What to do next

After you create and save a Discovery schedule, you can optionally configure the following settings:

-   Define IP addresses or ranges to exclude from all Discovery schedules. See [Use Global Excludes List for IP addresses and ranges](../reference/discovery-ip-address-configuration.md#).
-   Define Discovery schedule attributes to automatically set CI field values such as location or asset tag on discovered CIs. You can define attributes at the schedule, range set, or IP address range level. See [Define CI field attributes](define-ci-attributes.md).
-   Configure Discovery behaviors to use multiple MID Servers for load balancing or to scan with multiple credentials. See [Discovery behaviors](../concept/c_DiscoveryBehaviors.md).

## Run a Quick Discovery

Quick Discovery, or DiscoverNow, allows an administrator to run a CI Configuration discovery on a single IP address without requiring a schedule.

### Before you begin

Role required: discovery\_admin

### About this task

The platform automatically selects the correct MID Server to use for the discovery if one is associated with the IP address selected. If no MID Server is configured for the network in which that address appears, you can select a MID Server. Use this feature to discover new devices in the network as soon as they are connected to the network, rather than waiting for a regularly scheduled discovery.

To configure the system to automatically determine which MID Server to use, set up the IP range capabilities for each MID Server in your system.

You can run DiscoverNow from a Discovery schedule form or from a script.

**Note:** Quick Discovery using a IPv6 target address is supported.

### Procedure

1.  Open Quick Discovery from one of these locations:

    -   Navigate to **Discovery** &gt; **Discovery Schedules** and click **Quick Discovery** in the header bar.
    -   Navigate to **Discovery** &gt; **Home** and click **Discovery Quick Start** under the Schedules tile.
    A dialog box appears asking for an IP address and the name of the MID Server to use. Only **Up** and **Validated** MID Servers are available.

2.  Enter the target IP address for a discovery in the **Target IP** field.

    **Note:** DiscoverNow does not currently support IP network discovery. Make sure that you enter a single IP address only and not an entire network, such as 10.105.37.0/24.

    When a MID Server is assigned to the subnet containing the target IP address and currently in an operational status of **Up**, the name appears automatically in the **MID Server** field. If multiple MID servers are found, the system selects one for you. The value in the **MID Server** field can be overwritten if you want to select a different MID Server.

    **Important:** If the selected MID Server is part of a load balanced cluster and becomes unavailable for any reason, the instance does not assign another MID Server from that cluster to the quick Discovery. You must select another MID Server from the list of appropriate MID Servers.

3.  If no MID Server is defined for that network, select one from the list of available MID Servers.

    ![Quick discovery](../image/QuickDiscoveryDialog.png "Quick Discovery Dialog")

4.  Click **OK** to run discovery.

    The status record for that discovery appears. The **Schedule** column is empty because no schedule is associated with this discovery.

    ![Quick discovery status list](../image/QuickDiscoveryStatusList.png "Quick Discovery Status List")


## Run DiscoverNow from a script

You can run DiscoverNow from a script, such as a background job, a business rule, or web services.

### Before you begin

Role required: admin

### Procedure

1.  Create the following script:

    ```
    var d = new Discovery();
    var statusID = d.discoveryFromIP(TARGET_IP, TARGET_MIDSERVER);
    ```

    The **discoveryFromIP** method takes two arguments: *IP* and *MID Server*. The *IP* argument is mandatory, but the *MID Server* argument is optional.

2.  To choose the MID Server, supply either the *sys\_id* or name of the MID Server as the argument.

    If you do not name a MID Server, the system attempts to find a valid one automatically. A valid MID Server has a status of **Up** and can discover the given IP address. If the system finds a valid MID Server and runs a Discovery, the **discoveryFromIP** method returns the *sys\_id* of the Discovery status record. If no MID Server can discover this IP address, the method returns the value **undefined**.

    If you manually specify the TARGET\_MIDSERVER, the system validates the given value and ensures that the MID Server table contains the specified MID Server record. If the validation passes, the discoveryFromIP method returns the sys\_id of the discovery status record. If the validation fails, the method return the value **undefined**.


## Validate discovery results

Validate the results of your discovery by accessing the ECC queue, analyzing the XML payload, and checking the Discovery log.

### Before you begin

Role required: discovery\_admin

### About this task

Initial discoveries often reveal unexpected results, such as previously unknown devices and processes or failed authentication. Results should also accurately identify known devices and update the CMDB appropriately. Become familiar with the network that is being discovered and the types of data returned for the different types of discoveries. Use the Discovery Log and the ECC Queue to monitor the Discovery process as data is returned from probes or pattern operations.

### Procedure

1.  To view the actual payload of a probe, click the **XML** icon in a record in the ECC Queue.

    ![ECC Queue](../image/DiscoveryECCQueueView.png "ECC Queue")

2.  To view the actual payload of a probe, click the **XML** icon in a record in the ECC Queue.

3.  Use the Discovery Log form for a quick look at how the probes are doing.

    To display the Discovery Log, navigate to **Discovery** &gt; **Discovery Log**.

    ![The Discovery log](../image/DiscoveryLog.png "Discovery Log")

    The Discovery Log provides this information:

<table id="table_gq5_q3x_wp"><thead><tr><th>

Column

</th><th>

Information

</th></tr></thead><tbody><tr><td>

Created

</td><td>

Displays the timestamp for the probe launched. Click this link to view the record for the probe launched in this list.

</td></tr><tr><td>

Level

</td><td>

Displays the type of data returned by this probe. The possible levels are:-   Debug
-   Error
-   Information
-   Warning


</td></tr><tr><td>

Message

</td><td>

Message describing the action taken on the information returned by the probe.

</td></tr><tr><td>

ECC queue input

</td><td>

Displays the ECC queue name associated with the log message.

</td></tr><tr><td>

CI

</td><td>

The CI discovered. Click this link to display the record from the CMDB for this CI.

</td></tr><tr><td>

Source

</td><td>

Displays the probe name that generated the log message.

</td></tr><tr><td>

Device

</td><td>

Displays the IP address explored by the probe. Click this link to examine all the log entries for the action taken on this IP address by this Discovery.

</td></tr></tbody>
</table>    **Note:** If you cancel an active discovery, note the following information:

    -   Existing sensor jobs that have started processing are immediately terminated.
    -   The existing sensor jobs that are in a **Ready** state, but have not started processing, are deleted from the system.
4.  View the [Discovery Home page](../concept/discovery-home-page.md#) for details about all schedules, cloud resources \(virtual machines\), discovered devices, and related errors that might have occurred.

    [Error details](../concept/discovery-home-page.md#) include possible remediation steps.


## MID Server selection sequence for Discovery schedules

The Discovery application follows this sequence to find a MID Server.

### MID Server auto-selection

Discovery follows this sequence when you select **Auto-Select MID Server** for the **MID Server selection method** on the Discovery Schedule form.

**Note:** MID Server auto-select isn’t supported with IPv6.

1.  Discovery looks for a MID Server that also has an appropriate IP range configured.
2.  If no MID Servers meet these criteria, it looks for a MID Server that has the **ALL** application that also has an appropriate IP range configured.
3.  If more than one MID Server meet the criteria, Discovery chooses the first MID Server with the status of **Up**. If more than one MID Server is up, it randomly picks one.
4.  If none are up, it uses the default MID Server specified for the Discovery application, assuming it’s up.
5.  If no default MID Server is specified, it uses the default MID Server specified for the **ALL** application, assuming it’s up.
6.  If no default MID Server is specified, Discovery cycles through the previous steps and looks for MID Servers with the status of **Paused** or **Upgrading**.

    **Note:** When a MID Server is paused or upgrading, it doesn’t actually process commands until it returns to the status of **Up**.


### MID Server clusters

These steps are followed when you select **Specific MID Cluster** for the **MID Server selection method** on the **Discovery** form, and the cluster is a load balancing cluster:

1.  **Discovery** uses the first MID Server in the cluster that it finds with the status of **Up**.
2.  If more than one MID Server is up, it randomly picks one. If it can’t find any MID Servers, it looks for MID Servers in the cluster with the status of **Paused** or **Upgrading**.

These steps are followed when the cluster is a failover cluster:

1.  **Discovery** uses the MID Server with the lowest **Order** value that also has the status of **Up**.
2.  If no MID Servers are found, it looks for MID Servers in the cluster with the status of **Paused** or **Upgrading**, choosing the one with the lowest **Order** value.

**Note:** **Discovery** ignores the default MID Server for it and **ALL** applications when selecting a MID Server from the cluster.

### Port scan \(Shazzam\) phase

During the port scan phase, Discovery collects all the target IP addresses. It splits them equally between MID Servers matching the criteria \(MID Servers are qualified to do the port scan\). The Shazzam batch size, which you configured on the Discovery schedule, determines the number of IP addresses that each Shazzam probe can scan. This phase helps determine how much work each MID Server does during the port scan phase.

For example, you have 16,000 IP addresses to scan among three qualified MID Servers, and you use the default Shazzam batch size of 5,000. Two of the MID Servers handle 5,000 IP address scans \(one Shazzam probe each\). The other MID Server handles 6,000 IP address scans by launching two Shazzam probes.

**Note:**

Shazzam can process IP lists containing up to 20,000 addresses that include both IPv4 and IPv6 types. If a schedule contains any IPv6 addresses \(&gt; 0\), the combined total of IPv4 + IPv6 addresses must not exceed 20,000 or else the Discovery fails. If you’re using only IPv6 addresses, you must use a list and not an IP address range. IPv6 address ranges and networks aren't supported and are ignored.

**Related topics**  


[MID Server pause](https://www.servicenow.com/docs/access?context=t_PauseTheMIDServer&version=australia&pubname=australia-servicenow-platform&section=c_MIDServerPause&ft:locale=en-US)

[MID Server cluster configuration](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=australia&pubname=australia-servicenow-platform&section=mid-server-clusters&ft:locale=en-US)

