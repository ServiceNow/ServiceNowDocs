---
title: MID Server Resource Reservation
description: This feature allows resources to be reserved before a task is assigned to a thread. If the resources the task needs aren’t available, then that task waits in the MID Server work queue while other tasks are assigned to the thread.A resource is just a name and a count. Define the name of the resource, which probes use it, and how many of the resources those probes should use.In addition to the work queue, the MID Server contains a waiting queue. When picking a task for execution, the waiting queue is always checked first. If no task in the waiting queue can execute, then the work queue is tried. Probes and patterns in the waiting queue reserve all necessary resources until they’re able to execute.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server Resource Reservation

This feature allows resources to be reserved before a task is assigned to a thread. If the resources the task needs aren’t available, then that task waits in the MID Server work queue while other tasks are assigned to the thread.

<table id="table_p53_ms4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>For Discovery, the MID Server tasks are the probes or patterns it executes. While probes are waiting to be executed on the MID Server, they provide resource requirements \(CPU, memory, and so on\) and if they cannot be met, the probe waits in the work queue until the resources are available.

**Note:** MID Server Resource Reservation delays probe execution until resources are available. This is based on extremely flexible criteria. The MID Server Resource Reservation feature is for advanced users and should not be configured until a problem is identified. This configuration depends entirely on the problem details.

Using the MID Server Resource Reservation allows for better use of threads since the threads are not assigned a task it cannot complete.

Features:

-   Resource reservations apply to a single MID Server only
-   Resources can depend on system or MID Server properties
-   Resources can depend on probe parameters, allowing you to limit the number of active probes and patterns against a given IP
-   Reports resource usage
-   Extensible \(the customer defines their own resources\)
-   Scriptable

Benefits:

-   Keeps PowerShell probes from impacting execution of other probes
-   Can be used to limit the impact Discovery has on a target system
-   Can be used to limit the number of ”large” probes being executed by a MID Server at the same time
-   Can be used to throttle Discovery \(to minimize impact on the instance\)

## Use MID Server Resource Reservation

A resource is just a name and a count. Define the name of the resource, which probes use it, and how many of the resources those probes should use.

### Before you begin

Role required: admin

-   Make sure the MID Server property **mid.probe.wait.resources** is set to true to enable MID Server Resource Reservation. Changing this property requires restarting the MID Server.
-   Choose a resource name. Anything in \{ \} in the name is replaced by the probe parameter with that name. This name is typically used for per-host resources, for example, ssh\{source\} means a separate resource named “ssh” is available on every host being discovered. \(“source” is the name of the probe parameter that contains the IP address being probed.\)
-   Decide how to specify the number of the resource used by probes or patterns.
    -   Every probe uses a constant number of the resource: Create a “simple value” resource.
    -   The number of resources used depends on a system property: Create an “expanding” resource.
    -   The number depends on multiple factors: Create a “scripted” resource.
    -   Expanding: Anything in \{ \} is replaced by the system or MID Server property with that name. Logical operators are allowed, for example, "\{mid.windows.management\_protocol\}".toLowerCase\(\) == "winrm" ? 1:0
    -   Scripted: the script is evaluated. The return value is expanded.

### Procedure

1.  Create a new resource.

    1.  Navigate to **Discovery Definition** &gt; **Limited Resources**&gt; **Simple Value** and click **New**.

    2.  Enter a resource name.

    3.  Enter the number of resources used and click **Save**.

2.  Define which probes use the resource.

3.  Navigate to the desired tab and select from the list.

    -   **Used by Topic** tab: Includes all probes with that topic. Click **Invert Topic** to include all probes without that topic. For example: SSHCommand with Invert Topic, means all probes except for SSH. Heartbeat and queue messages are always excluded.
    -   **Used by probes** tab: Includes a list of probes. Click **Invert Probes List** to include all probes without that probe. Horizontal Discovery probe means apply to all patterns.
    -   **Used by patterns** tab: Includes a list of patterns. You can also click Invert Pattern list.
4.  Define availability on the MID Server.

5.  Navigate to **Discovery Definition** &gt; **Limited Resources** &gt; **MID Resources**.

    -   Resource: This is the reference to the resource.
    -   Available: Number available. Anything inside brackets, is replaced by the system or MID Server property.
    -   MID Server: MID Server to apply this to. \(Empty\) means all.
6.  Set the resource order.

    1.  Click in the **Order** field of each resource.

    2.  Type in the number.

    3.  Click the check mark to Save.

7.  **Note:** Less valuable resources should have a lower order – these resources are reserved and held until higher order resources can be obtained. For example, both the total PowerShell sessions \(resource is “PowerShell”\) and the number of simultaneous sessions to any host \(resource is “PowerShell\{host\}”\) are limited. Therefore, PowerShell\{host\} resource should have a lower order. Obtaining PowerShell first would impact all other PowerShell probes. Obtaining “PowerShell\{host\}” first only impacts other PowerShell probes to that host.

8.  Review the Resource State that you have set up.

    1.  Run a Discovery.

    2.  Observe Resource State.

    3.  Click **Get resource state** from the MID Server page or view in an ECC input payload.

        Result of Get resource state:

        -   PowerShell\{source\} has additional entries for every \{source\} with a current allocation.
        -   “Reserved by” may show multiple resources if the probe requires more than one resource.
        Result of ECC input payload:

        -   The resource\_wait attribute only exists if the probe had to wait for a resource.
        -   The time displayed is in milliseconds.
        -   The probe may have waited on multiple resources, with different wait time for each.

## How MID Server Resource Reservation works

In addition to the work queue, the MID Server contains a waiting queue. When picking a task for execution, the waiting queue is always checked first. If no task in the waiting queue can execute, then the work queue is tried. Probes and patterns in the waiting queue reserve all necessary resources until they’re able to execute.

The first probe or pattern in the queue is offered available resources. It takes any of the lowest order resource that is available. After getting the required number of lowest order resources, the probe or pattern goes to the next lowest order resources, and so on. The order allows the user to configure which resources are more or less important. Lowest order resources are gathered first because holding these resources has less impact on execution of other probes and patterns.

### Tables

**mid\_limited\_resource**

-   Defines the resources used by a probe or pattern.
-   Extended by mid\_limited\_resource\_value, mid\_limited\_resource\_expanded, and mid\_limited\_resource\_script each containing a single additional field.
    -   mid\_limited\_resource\_value adds a single field named “value” to the base table.
    -   mid\_limited\_resource\_expanding adds a field named “expanding.”
    -   mid\_limited\_resource\_script adds a field named “script”.

**mid\_resource**

-   Sets the resources available on a MID Server.
-   Values from this table are copied to ecc\_agent\_property.
-   A business rule on this table creates the corresponding MID Server properties.
-   It has a reference to a resource and the number available. If the number available is inside \{ \} then it’s the name of a system property, MID Server config, or MID Server property \(all three places are checked\). So \{mid.powershell\_api.session\_pool.max\_size\} is the value of that MID Server config that sets the size of the PowerShell session pool.

|Label|Column|Type|Size|Information|
|-----|------|----|----|-----------|
|Resource Name|name|String|100|Unexpanded name of the resource|
|Active|active|Boolean| |Allows temporary disable|
|Invert Topic|invert\_topic|Boolean| | |
|Invert Probe List|invert\_probe\_list|Boolean| | |
|Invert Pattern List|invert\_pattern\_list|Boolean| | |

**Note:** There are m2m tables that associate a mid\_limited\_resource record with topics, probes, and patterns. The “invert\_” fields change the list from inclusion to exclusion.

|Label|Column|Type|Size|Information|
|-----|------|----|----|-----------|
|Value|value|Integer| | |
|Expanding|expanding|String|1000|A slightly extended version of the availability number because it accepts logical and ternary operations, for example, "\{mid.windows.management\_protocol\}" == "WinRM" ? 1 : 0. If the management protocol is WinRM this evaluates to 1, otherwise it’s 0.|
|Script|script|String|4000|The script is evaluated. If the result is a string, then it’s expanded|

|Label|Column|Type|Size|Information|
|-----|------|----|----|-----------|
|Active|active|Boolean| |Allows temporary disable|
|Available|available|String|255|Number of this resource available on MID Server|
|MID Server|ecc\_egent|Reference| |Reference to MID Server or empty for all|
|Order|order|Integer| |Order in which resources are allocated|
|Resource|resource|Reference| |Reference to the resource|

