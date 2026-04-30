---
title: Create a Discovery process handler
description: Process handlers prevent the creation of duplicate CIs by filtering out parameters known to have inconsistent values before process classification occurs. You can create new classifiers or edit existing ones.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a Discovery process classification, Discovery classifiers, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Create a Discovery process handler

Process handlers prevent the creation of duplicate CIs by filtering out parameters known to have inconsistent values before process classification occurs. You can create new classifiers or edit existing ones.

## Before you begin

Role required: none

## Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **CI Classification** &gt; **Process Handlers**.

2.  Click **New**.

3.  Complete the fields on the Process Handler form.

<table id="table_egg_1wv_1q"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name for the process handler record.

</td></tr><tr><td>

Active

</td><td>

Select the check box to run the process handler.

</td></tr><tr><td>

Classify

</td><td>

-   Select the check box to enable classification of any Running Process \[cmdb\_running\_process\] record that matches this Process Handler's conditions.
-   Clear the checkbox to disable classification of any Running Process \[cmdb\_running\_process\] record that matches this Process Handler's conditions.


</td></tr><tr><td>

Condition

</td><td>

Select the conditions that trigger the process handler to run the script. In most cases, this condition contains either specific executable names or the presence of certain parameters.

</td></tr><tr><td>

Script

</td><td>

Enter the JavaScript you want to run on the current record in the Running Process \[cmdb\_running\_process\] table when the **Condition** is met. The `current` variable is a reference to a Running Process GlideRecord. The script should examine `current.parameters` for certain values, perform string replacement to manipulate these values, and save the result to `current.key_parameters`. ServiceNow uses the **key\_parameters** field, together with the process name, to determine whether the process is unique on a specific machine.

See [On classification script objects for Discovery](../reference/r_OnClassificationScriptObjects.md) for additional options.

</td></tr></tbody>
</table>4.  Click **Submit**.


## What to do next

Run a discovery through the [Discovery Schedule](t_CreateADiscoverySchedule.md) to search for applications and then [verify the results in the CMDB](../concept/c_Software.md) for the applications that are found.

