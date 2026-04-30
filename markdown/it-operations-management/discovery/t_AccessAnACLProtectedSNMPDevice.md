---
title: Discovery behavior example: access an ACL protected SNMP device
description: Access an SNMP device protected by an ACL using a Discovery behavior.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-11-25"
reading_time_minutes: 5
breadcrumb: [Discovery behaviors, Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery behavior example: access an ACL protected SNMP device

Access an SNMP device protected by an ACL using a Discovery behavior.

## Before you begin

Role required: discovery\_admin or admin

## About this task

A specific type of Access Control List \(ACL\) on an SNMP device can prevent Discovery from identifying that device. This list defines host machines by IP addresses that are permitted to run agents on SNMP devices. In this example, we want to classify, identify, and update all the devices in an IP range, including the SNMP devices protected by an ACL. To do this, we must install a MID Server with access to the protected SNMP devices and then create a Behavior that allows us to scan for all protocols without missing any devices or doing any extra work.

## Procedure

1.  Install a MID Server on a host permitted by the ACL.

    To scan the SNMP devices in a network protected by an ACL, a MID Server must be installed on a host machine specified by IP address in the ACL as having access to the SNMP devices. Because this MID Server is scanning SNMP devices only, it can be installed on any supported operating system. The other MID Server, configured to discover WMI and SSH, can be installed on any Windows host that has visibility to the specified IP ranges.

2.  Install additional MID Servers if you intend to configure either functionality to load balance.

3.  Create the behavior record.

    1.  Create a new Discovery Behavior record, and name it something descriptive, such as Southwest-SNMP.

    2.  Right-click in the header bar and select **Save** from the pop-up menu.

        This action saves the record and creates the Discovery Functionality related list in the form.

    3.  To complete this behavior \(as shown in [Figure 1](t_AccessAnACLProtectedSNMPDevice.md#f_DiscoveryBehaviorRecordACL)\) we must create functionalities using the MID Servers we installed for that purpose.

        For the functionality that scans for the WMI protocol, we must define criteria that specify the Windows domain and MID Server being used. Because this Discovery is being performed on one Windows domain, we can configure a functionality for WMI and SSH \(**All except SNMP**\) using the same MID Server.

    ![Discovery behaviors](../image/DiscoveryBehaviorRecordACL.png "Completed Discovery Behavior")

4.  Define the functionalities.

    For this behavior, we create two functionalities, one for SNMP on the MID Server installed on the host specified in the ACL and another for WMI and SSH on a second MID Server.

    1.  Click **New** in the Discovery Functionality related list to add functionalities.

    2.  **Note:** We configure the MID Server installed on the privileged host machine to scan for the SNMP protocol only.

        Create the first functionality using the following values:

        |Field|Input Value|
        |-----|-----------|
        |Phase|Type a phase number of `1` in this field. Both functionalities in this example use the same phase number, which launches a single Shazzam probe for all the functionalities in that phase. A single phase, when feasible, is the most efficient use of the Shazzam probe.|
        |Functionality|Select SNMP only from the list. This functionality defines the protocol that will be scanned.|
        |MID Servers|We select a MID Server \(sansol02\_Solaris\) installed on a Solaris host that is granted access to the SNMP devices by the ACL. You can select multiple MID Servers if you want Discovery to load balance this functionality automatically.|
        |Active|Make sure this check box is selected to enable this behavior.|
        |Match criteria|Leave the default criteria of Any. Criteria are not used for SNMP functionalities.|

        ![Scan for SNMP Only](../image/DiscoveryFunctionalitySNMPOnly.png "Scan for SNMP Only")

    3.  **Note:** In the second functionality, Discovery will scan our domain for WMI and SSH protocols. Because WMI is one of the protocols, the MID Server for this functionality must be installed on a Windows machine and must have criteria.

        Create the second functionality using the following values:

        |Field|Input Value|
        |-----|-----------|
        |Phase|Type a phase number of `1` in this field. All functionalities in this example use the same phase number, which launches a single Shazzam probe for all protocol scans. A single phase, when feasible, is the most efficient use of the Shazzam probe.|
        |Functionality|Select All except SNMP from the list. This functionality defines the protocols for which scanning will occur. Because WMI is one of the protocols selected, we must use a Windows MID Server for this functionality.|
        |MID Servers|We select a Windows MID Server from our domain. In this case we select disco-win2003. You can select multiple MID Servers if you want Discovery to load balance this functionality automatically.|
        |Active|Make sure this check box is selected to enable this behavior.|
        |Match criteria|Change the criteria to All.|

        ![Scan for All Except SNMP](../image/DiscoveryFunctionalityAllExceptSNMP.png "Scan for All Except SNMP")

    4.  **Note:** Functionalities that scan for WMI require criteria to identify the domain and the MID Server. In our example, we will create two criteria for this functionality.

        To create functionality criteria for a WMI scan, click **New** in the related list.

    5.  Enter the following values for the MID Server doing the WMI scanning on our domain:

<table id="table_ufh_gg1_wp"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Create the following criteria:-   Enter `mid_server` to name the MID Server that will execute the WMI scans.
-   Enter `win_domain` to name the Windows domain that Discovery will scan with the MID Server defined.


</td></tr><tr><td>

Operator

</td><td>

Select equals as the operator in this criteria.

</td></tr><tr><td>

Value

</td><td>

-   For the mid\_server value, enter the name of the MID Server that will scan our domain for Windows devices.
-   For the win\_domain value, enter the name of our Windows domain.


</td></tr><tr><td>

Active

</td><td>

Be sure to enable the criteria by selecting this check box \(**true**\).

</td></tr></tbody>
</table>        The completed criteria appear as follows in the Discovery Functionality form for this behavior.

        ![Functionality Criteria for a WMI Scan](../image/WMICriteria.png "Functionality Criteria for a WMI Scan")

5.  Create the schedule.

    1.  Create a Discovery Schedule record and name the behavior we just created.

    2.  Navigate to **Discovery** &gt; **Discovery Schedules** and click **New** in the record list.

    3.  Select a **Discover** mode of Configuration items.

        This action displays the **Behavior** field.

    4.  Click the magnifier icon and select the behavior to use.

        In our example, we select Southwest-SNMP.

    5.  Select the appropriate time to run Discovery for this location.

    6.  Click **Quick Ranges** and define the IP address ranges, networks, or lists to scan for this domain.

    7.  Save the record.

    ![Schedule Record](../image/DiscoveryBehaviorScheduleACL.png "Discovery Schedule Record")


**Parent Topic:**[Discovery behaviors](../concept/c_DiscoveryBehaviors.md)

**Related topics**  


[Create a Discovery behavior](create-disco-behavior.md)

[Set up a load balancing behavior](t_SetUpLoadBalDiscoBehavr.md)

[Examples of Discovery behavior functionalities](../reference/r_DefineTheFunctionalities.md)

