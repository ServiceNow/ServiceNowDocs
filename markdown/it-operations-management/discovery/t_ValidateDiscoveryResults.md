---
title: Validate discovery results
description: Validate the results of your discovery by accessing the ECC queue, analyzing the XML payload, and checking the Discovery log.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Schedule a horizontal discovery, Running discoveries in your network, Discovery, ITOM Visibility, IT Operations Management]
---

# Validate discovery results

Validate the results of your discovery by accessing the ECC queue, analyzing the XML payload, and checking the Discovery log.

## Before you begin

Role required: discovery\_admin

## About this task

Initial discoveries often reveal unexpected results, such as previously unknown devices and processes or failed authentication. Results should also accurately identify known devices and update the CMDB appropriately. Become familiar with the network that is being discovered and the types of data returned for the different types of discoveries. Use the Discovery Log and the ECC Queue to monitor the Discovery process as data is returned from probes or pattern operations.

## Procedure

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


