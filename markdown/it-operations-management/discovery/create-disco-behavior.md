---
title: Create a Discovery behavior
description: Create a Discovery behavior to determine which probes Shazzam launches and which MID Server is used.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Discovery behaviors, Advanced Discovery configuration, Discovery, ITOM Visibility, IT Operations Management]
---

# Create a Discovery behavior

Create a Discovery behavior to determine which probes Shazzam launches and which MID Server is used.

## Before you begin

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **Behavior** and click **New**.

2.  Enter a name.

3.  Right-click the form header and select **Save**.

    ![Discovery behavior form](../image/DiscoveryBehavior.png)

4.  In the Discovery Functionality related list, click **New**.

    Discovery Functionality defines what each MID Server in this behavior must do, specifically which protocols to detect.

5.  Fill out the form fields:

<table id="table_lzj_wlf_wbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Phase

</td><td>

Enter an integer that represents an arbitrary phase. The phase is used to group one or more functionalities together. All the functionalities within a specified phase are executed together, and all phases are executed in numerical order. All functionalities in a behavior can have the same phase.

 The Shazzam probe runs once for each phase in a behavior, which makes fewer phases desirable. Run multiple phases for behaviors only when devices in the network are running multiple protocols, such as SSH and SNMP. In that example, set one phase for the SSH scan and another phase for the SNMP scan.

</td></tr><tr><td>

Active

</td><td>

Keep this option selected to apply the discovery functionality.

</td></tr><tr><td>

Functionality definition

</td><td>

Click the lookup icon, and then select a pre-configured functionality that defines the protocol or list of protocols that each MID Server scans.

</td></tr><tr><td>

Match criteria

</td><td>

Define criteria here for Windows MID Servers.

</td></tr><tr><td>

MID Servers

</td><td>

Select one or more MID Servers to perform this functionality for the following Discovery types:-   IP Scan
-   CI Scan
 Discovery automatically balances the load when multiple MID Servers are selected.

</td></tr></tbody>
</table>6.  Right-click the form header and select **Save**.

7.  To add criteria that the functionality must meet in order to be triggered, click **New** in the Functionality Criteria related list, fill out the form fields, and then click **Submit**.

<table id="table_f1v_ts2_vp"><thead><tr><th>

Field

</th><th>

Input Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name in the criteria is the variable that passes the following information:-   `mid_server`: MID Server that processes the results from the Shazzam probe.
-   `win_domain`: Windows domain of the target device.


</td></tr><tr><td>

Operator

</td><td>

Select a logical operator.

</td></tr><tr><td>

Value

</td><td>

Enter the actual name of the MID Server \(`mid_server`\) or domain \(`win_domain`\) to pass to Discovery for this criteria. This field can also have a value of `mid_domain`, which defines the Windows domain of the MID Server that is processing the Shazzam results.

</td></tr></tbody>
</table>    **Note:** Functionality criteria are required for Windows MID Servers only, and only when the behavior controls Discovery across multiple domains. When the instance launches the Shazzam probe for a Discovery in which a behavior defines multiple MID Servers to scan multiple domains, the functionality criteria determine which MID Server process the results of the probe.

    The following graphic shows an example of functionality criteria. ![Discovery functionality criteria](../image/DiscoveryFunctionalityCriteria.png)


## What to do next

[Schedule a horizontal discovery](t_CreateADiscoverySchedule.md) of type **Configuration Item**, and select **Use Behavior** for the MID Server selection method.

**Parent Topic:**[Discovery behaviors](../concept/c_DiscoveryBehaviors.md)

**Related topics**  


[Set up a load balancing behavior](t_SetUpLoadBalDiscoBehavr.md)

[Examples of Discovery behavior functionalities](../reference/r_DefineTheFunctionalities.md)

[Discovery behavior example: access an ACL protected SNMP device](t_AccessAnACLProtectedSNMPDevice.md)

