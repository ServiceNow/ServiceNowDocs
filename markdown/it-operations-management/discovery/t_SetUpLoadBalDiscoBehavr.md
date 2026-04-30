---
title: Set up a load balancing behavior
description: When multiple MID Servers are configured to scan the same protocol, you can set up load balancing behavior to automatically balance the work between MID Servers.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-12-16"
reading_time_minutes: 4
breadcrumb: [Discovery behaviors, Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Set up a load balancing behavior

When multiple MID Servers are configured to scan the same protocol, you can set up load balancing behavior to automatically balance the work between MID Servers.

## Before you begin

Role required: agent\_admin, discovery\_admin, or admin

## About this task

Behaviors enable load balancing when multiple MID Servers are configured to scan the same protocol.

For example, an organization has 50 remote locations, varying in size from 10 devices to several hundred devices. All the satellite offices are part of the same Windows domain, which is administered from a central location. There are three MID Servers installed at this central location: Two to scan all the Windows devices and one to scan the remaining devices. Since remote offices are in different time zones, you must create different schedules to run Discovery at off-peak hours in each time zone. You can use the same behavior for each schedule, and the behavior load balances the two Windows MID Servers automatically.

## Procedure

1.  Create the behavior record.

    1.  Create a Discovery behavior record and name it something descriptive, such as LoadBalanced.

    2.  Select and hold \(or right-click\) the header bar and select **Save** from the pop-up menu.

        You save the record and create the Discovery Functionality related list in the form.

2.  Define the Windows functionality.

    1.  In the Discovery Functionality related list, select **New**.

    2.  Create a record using the fields described in the following table.

    3.  Select and hold \(or right-click\) the header bar and select **Save** from the pop-up menu.

    |Field|Input Value|
    |-----|-----------|
    |Phase|Enter a phase number of `1` in this field.|
    |Functionality|Select Windows only \(WMI\) from the list. This functionality defines the protocol that is scanned. Because you selected to scan WMI, you must select Windows MID Servers for this functionality.|
    |MID Servers|Select the two MID Servers you want to share the load for the WMI probes. By entering multiple MID Servers in this field, you tell Discovery to balance the load between these servers automatically. If you create separate functionality for each server, load balancing wouldn’t occur.|
    |Active|Select this check box to enable this behavior.|
    |Match criteria|Leave the default criteria of Any.|

    ![Discovery functionality](../image/FunctionalityLoadBalance.png "Discovery Functionality Form")

3.  Create Functionality Criteria.

    **Note:** All Windows functionality requires criteria to identify the Windows domain and define any special behavior for the MID Servers named.

    1.  In the related list, select **New**.

    2.  Enter the following values:

        |Field|Input Value|
        |-----|-----------|
        |Name|Enter `win_domain` to name the Windows domain that Discovery scans with the MID Servers you have defined.|
        |Operator|Select equals as the operator.|
        |Value|The name of the Windows domain that these MID Servers scans for devices.|
        |Active|Enable the criteria by selecting this check box \(**true**\).|

4.  Define the functionality for the remaining scans.

    Create a second record to scan for all the remaining protocols \(SSH, SNMP, and so on\) using the following settings:

    |Field|Input Value|
    |-----|-----------|
    |Phase|Enter a phase number of `1` in this field. This phase runs concurrently with WMI scans using the same Shazzam probe. The same phase number is used because the target IP ranges don't include devices running multiple protocols \(such as SSH or SNMP\). If any devices were running multiple protocols, additional phases \(second or third\) should be specified to identify the correct protocol for each device before proceeding.|
    |Functionality|Select All except Windows \(no WMI\) from the list. This functionality causes the MID Server to scan all remaining protocols after Discovery has run the WMI scans.|
    |MID Servers|Enter the name of the MID Server that scans all remaining devices. To enable automatic load balancing, add an additional MID Server in this field.|

5.  Create a [Discovery schedule](t_CreateADiscoverySchedule.md#) for each time zone and name the behavior you created.

    1.  Navigate to **Discovery** &gt; **Discovery Schedules** and select **New** in the record list.

    2.  Select a **Discover** type of Configuration items.

    3.  In the **MID Server selection method** field, select Use Behavior.

        **Warning:** If this option isn't selected, the required value for the next step may not be available.

    4.  Select the search icon ![](../../health-log-analytics-operator/image/icon-search-sow.png) and choose the behavior to use.

        In this example, select LoadBalanced.

    5.  Select the appropriate time to run Discovery for this location.

    6.  Select **Quick Ranges** and define the IP address ranges, networks, or lists to scan for this location.

    7.  Save the record.

    8.  Create additional schedules for each time zone or region in the network and select the same behavior.

    ![Discovery Schedule](../image/DiscoverySchedule.png "Discovery Schedule")


**Parent Topic:**[Discovery behaviors](../concept/c_DiscoveryBehaviors.md)

**Related topics**  


[Create a Discovery behavior](create-disco-behavior.md)

[Examples of Discovery behavior functionalities](../reference/r_DefineTheFunctionalities.md)

[Discovery behavior example: access an ACL protected SNMP device](t_AccessAnACLProtectedSNMPDevice.md)

