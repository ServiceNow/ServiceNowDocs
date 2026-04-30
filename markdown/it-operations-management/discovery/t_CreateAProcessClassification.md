---
title: Create a Discovery process classification
description: A process classification allows Discovery to create a particular CI type from information gathered during the identification and exploration phases.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Discovery classifiers, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Create a Discovery process classification

A process classification allows Discovery to create a particular CI type from information gathered during the identification and exploration phases.

## Before you begin

Role required: none

## About this task

When a process matches the classification criteria, Discovery uses the process classification record to create a CI.You can also have Discovery update existing CIs or ignore certain processes by creating a [process handler](t_CreateAProcessHandler.md).

**Note:** There is no support for dot-walk on the parent running the process command.

## Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **CI Classification** &gt; **Processes**.

2.  Click **New**.

3.  Enter the classification fields \(see table\).

<table id="table_ofm_py5_1q"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Select the table where this classification generates CI records. This table must be an extension of the Applications \[cmdb\_ci\_appl\] table.

</td></tr><tr><td>

Relation type

</td><td>

Select the CI relationship type for this classification. The relationship field is only available for Process and Scan Application classifications.Discovery process classifications typically use one of these relationship types:

 -   Runs on::Runs: Defines the relationship of an application to the host on which it runs. This relationship is expressed from the perspective of the host and the application. For example: My database application runs on server001::server001 runs my database application.
-   Depends on::Used by: Defines the relationship of an application that communicates with another application. This relationship is expressed from the perspective of each application. For example: The Tomcat application depends on the MySQL database:: The MySQL database is used by Tomcat.
-   Virtualized by::Virtualizes: Defines the relationship of a virtual machine to its host. This relationship is expressed from the perspective of the virtual machine and of the host. For example: server001 is virtualized by Server ESX::Server ESX virtualizes server001.


</td></tr><tr><td>

Active

</td><td>

Select this option to enable the process classification record. Only active process classifications can create application CI records.

</td></tr><tr><td>

Order

</td><td>

Enter the order in which Discovery should run this process classification when there are multiple classifications available for a table. Discovery runs process classifications from the lowest to highest order.

</td></tr><tr><td>

Test with

</td><td>

Lists the host CI where an automatically generated process classification conditioncons were met. Use this field to test changes to the process classification to ensure that the updated classification behaves as expected.

</td></tr><tr><td>

Condition

</td><td>

Use the condition builder to create the match and classification criteria for the process classification. This field replaces both the **Match criteria** field and **Classification Criteria** related list. The upgrade process converts all existing classification criteria into conditions.

 **Note:** Condition filters in process classifiers are case-sensitive.

 **Note:** Only these conditions work:

-   name
-   PID
-   PPID
-   command
-   parameters
-   listening\_on\_ports
-   connecting\_to\_ports
-   connecting\_to
-   key\_parameters
-   classify


</td></tr><tr><td>

On classification script

</td><td>

Enter a script to run when the condition and classification criteria are met. Use this script to perform any special tasks after a device is classified. It is possible to use the `g_probe_parameters` hashmap from within a classification script to set probe parameters for any configured, triggered probes. For example, this code sets a `'node_port'` parameter to 16001 for all triggered probes.`g_probe_parameters['node_port'] = 16001;`

 See [On classification script objects for Discovery](../reference/r_OnClassificationScriptObjects.md) for more examples and for a list of the objects you can use in this kind of script.

</td></tr><tr><td>

Triggers probes

</td><td>

Select the exploration probes you want Discovery to launch. These probes gather detailed information about a classified CI. Discovery will not launch these probes when it is configured to stop after classification. If you want to use patterns for horizontal discovery, add the [Horizontal Pattern](../reference/r-HorizontalPatternProbe.md) probe in the **Probe** column, and then specify your pattern in the **Pattern** column. **Warning:** Do not specify your pattern in the **Probe** column. You must choose the Horizontal Pattern probe which launches the specified pattern.

</td></tr><tr><td>

Applications

</td><td>

Use this related list to view the application CIs that match this process classification.

</td></tr><tr><td>

Test results

</td><td>

Use this related list to view the how Discovery classifies processes on the **Test with** host and build better classification conditions.

</td></tr><tr><td>

Parameters

</td><td>

Use this related list to view the parameters associated with this process and build better classification conditions. See [Discovery classification parameters](../reference/classification-parameters.md) for a list of the parameters you can use.

</td></tr><tr><td>

Versions

</td><td>

Use this related list to view previous versions of the process classification record.

</td></tr></tbody>
</table>4.  Right-click the header bar and click **Save**.

5.  Enter items from related lists.

6.  Click **Update**.


## Example

![Process classification](../image/ProcessClassificationForm.png "An example process classification record")

## What to do next

Run a discovery through the [Discovery Schedule](t_CreateADiscoverySchedule.md) to search for applications. You can also [create or modify process handlers](t_CreateAProcessHandler.md) that prevent the creation of duplicate CIs based on process classifiers if that is an issue for your environment.

