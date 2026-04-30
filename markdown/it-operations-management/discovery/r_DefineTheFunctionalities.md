---
title: Examples of Discovery behavior functionalities
description: This example of a Discovery behavior requires three functionalities for the behavior.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Discovery behaviors, Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Examples of Discovery behavior functionalities

This example of a Discovery behavior requires three functionalities for the behavior.

We will create three functionalities for this Behavior: one MID Server to scan Domain A for Windows devices only; a second functionality for the same MID Server to scan for all SSH and SNMP devices; and a third functionality that names a second MID Server to scan Domain B for Windows devices. The rationale for this is as follows:

-   A Windows MID Server can only discover Windows machines on the Windows domain to which it is joined. This is entirely due to the way Windows authentication works. For this reason, we need a WMI functionality for each domain.
-   A Windows MID Server, provided with the correct credentials, can discover SSH and SNMP devices anywhere; however, we cannot combine WMI, SSH, and SNMP functionalities across Windows domains. This is because the functionality criteria for the WMI scans locks in the Discovery to one specific domain. For this reason, SSH and SNMP discoveries require a separate functionality.
-   We want to scan each machine only once.

## Functionality 1: WMI Scanning on Domain A

We configure a MID Server to scan for the WMI protocol on Domain A. WMI scans authenticate on Windows machines using the domain credentials of the Windows MID Server machine. Windows MID Servers cannot scan for the WMI protocol outside their own domains.

Create the first functionality using the following values:

|Field|Input Value|
|-----|-----------|
|Phase|Type a phase number of **1** in this field. All functionalities in this example use the same phase number, which launches a single Shazzam probe for all the functionalities in that phase. A single phase, when feasible, is the most efficient use of the Shazzam probe.|
|Functionality|Select **Windows, DNS, and WINS** from the list. This functionality defines the WMI protocol that will be scanned and resolves the domain. Because we selected to scan for WMI, we must select a Windows MID Server for this functionality.|
|MID Servers|We select a Windows MID Server from Domain A - in this case **sandb01-358**.|
|Active|Make sure this check box is selected to enable this behavior.|
|Match criteria|Change the criteria to **All**.|

## Create Functionality Criteria

All Windows functionality requires criteria to identify the domain and the MID Server. In our example, we will create two criteria for this functionality. To create Functionality Criteria, click **New** in the Related List and enter the following values for the MID Server doing the WMI scanning on Domain A:

<table id="table_ajk_pzc_5p"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Create the following criteria:-   Enter `mid_server` to name the MID Server that will execute the WMI scans on Domain A.
-   Enter `win_domain` to name the Windows domain that Discovery will scan with the MID Server defined.

</td></tr><tr><td>

Operator

</td><td>

Select **equals** as the operator in this criteria.

</td></tr><tr><td>

Value

</td><td>

-   For the mid\_server value, enter the name of the MID Server that will scan Domain A for Windows devices.
-   For the win\_domain value, enter the name of Domain A that this MID Server will scan for Windows devices.

</td></tr><tr><td>

Active

</td><td>

Be sure to enable the criteria by selecting this check box \(true\).

</td></tr></tbody>
</table>The completed criteria appear in the Discovery Functionality form for this behavior.

## Functionality 2: SSH and SNMP

In our network, we want to scan for UNIX computers and netgear, but we don't want to classify these devices twice. One of our MID Servers will be configured to classify SSH and SNMP using a different functionality than it does for WMI scans. We do not need to create criteria for non-WMI functionality.

Create the second functionality using the following values:

|Field|Input Value|
|-----|-----------|
|Phase|Type a phase number of `1` in this field. All functionalities in this example use the same phase number, which launches a single Shazzam probe for all the functionalities in that phase. A single phase, when feasible, is the most efficient use of the Shazzam probe.|
|Functionality|Select **All except Windows \(no WMI\)** from the list. This functionality will scan SSH and SNMP protocols only.|
|MID Servers|We select the MID Server from Domain A - in this case **sandb01-358**.|
|Active|Make sure this check box is selected to enable this behavior.|
|Match criteria|Leave the default criteria of Any. Criteria are not used for non-WMI functionalities.|

## Functionality 3: WMI Scanning on Domain B

All that remains is to create a functionality for the WMI scans on Domain B. Because of the Windows authentication mechanism, we must configure a Windows MID Server to scan Domain B that is a member of that domain.

Create the third functionality using the following values:

|Field|Input Value|
|-----|-----------|
|Phase|Type a phase number of `1` in this field. All functionalities in this example use the same phase number, which launches a single Shazzam probe for all the functionalities in that phase. A single phase, when feasible, is the most efficient use of the Shazzam probe.|
|Functionality|Select **Windows, DNS, and WINS** from the list. This functionality defines the WMI protocol that will be scanned and resolves the domain. Because we selected to scan for WMI, we must select a Windows MID Server for this functionality.|
|MID Servers|We select a Windows MID Server from Domain B - in this case **disco-win2003**.|
|Active|Make sure this check box is selected to enable this behavior.|
|Match criteria|Change the criteria to All.|

## Create Functionality Criteria

All Windows functionality requires criteria to identify the Windows domain and the MID Server. In our example, we will create two criteria for this functionality. To create Functionality Criteria, click **New** in the Related List and enter the following values for the MID Server doing the WMI scanning on Domain B:

<table id="table_inm_5bd_5p"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Create the following criteria:-   Enter `mid_server` to name the MID Server that will execute the WMI scans on Domain B.
-   Enter `win_domain` to name the Windows domain that Discovery will scan with the MID Server defined.

</td></tr><tr><td>

Operator

</td><td>

Select **equals** as the operator in this criteria.

</td></tr><tr><td>

Value

</td><td>

-   For the mid\_server value, enter the name of the MID Server that will scan Domain B for Windows devices.
-   For the win\_domain value, enter the name of Domain B that this MID Server will scan for Windows devices.

</td></tr><tr><td>

Active

</td><td>

Be sure to enable the criteria by selecting this check box \(true\).

</td></tr></tbody>
</table>The completed criteria appear in the Discovery Functionality form for this behavior.

**Parent Topic:**[Discovery behaviors](../concept/c_DiscoveryBehaviors.md)

**Related topics**  


[Create a Discovery behavior](../task/create-disco-behavior.md)

[Set up a load balancing behavior](../task/t_SetUpLoadBalDiscoBehavr.md)

[Discovery behavior example: access an ACL protected SNMP device](../task/t_AccessAnACLProtectedSNMPDevice.md)

