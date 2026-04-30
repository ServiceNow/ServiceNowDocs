---
title: Create and select an update set as the current set
description: Create an update set to store customization changes and select it as the current set.
locale: en-US
release: xanadu
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Update set use, System update sets, Deploying applications, Building applications]
---

# Create and select an update set as the current set

Create an update set to store customization changes and select it as the current set.

## Before you begin

Role required: admin.

## About this task

You can select an update set as the current set when you create it, or you can select it later from the Settings panel.

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets** and click **New**.

2.  Complete the form from the fields in the table.

3.  Click **Submit** to create the update set.

4.  If the picker is enabled and the update set is in the In progress state, click **Submit and Make Current** to select the new update set as the target for configuration changes.

    ![New update set](../image/UpdateSetNew.png "New update set")

<table id="table_nln_kgn_vp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name for the update set. You can use naming conventions to organize update sets. For example, add the problem number to the name of the update that fixes it, identify the application scope, or use sequence numbers to keep track of the order in which update sets need to be committed.

</td></tr><tr><td>

State

</td><td>

Select **In progress** for a new update set. Selecting an In progress update set tracks customizations in the update set. The [update set picker](select-update-set-system-settings.md) only displays In progress update sets.Select **Completed** only when you are certain that the update set is complete. After it is marked Completed, do not set it back to In progress. Instead, create a new update set with further customizations, and make sure to commit the update sets in the order that they were marked Completed. Use Completed update sets to transfer changes from one instance to another.

 Select **Ignore** when you are no longer working on an update set but do not want it to be transferred to another instance. You should always set Completed update sets on the production instance to Ignore. This state ensures the update set is not committed again when cloning the instance.

 Update set picker only displays In progress update sets. See [Select the current update set in Unified Navigation](select-update-set-system-settings.md).Select **Completed** only when you are certain that the update set is complete. After it is marked Completed, do not set it back to In progress. Instead, create a new update set with further customizations, and make sure to commit the update sets in the order that they were marked Completed. Use Completed update sets to transfer changes from one instance to another.

 Select **Ignore** when you are no longer working on an update set but do not want it to be transferred to another instance. You should always set Completed update sets on the production instance to Ignore. This state ensures the update set is not committed again when cloning the instance.

</td></tr><tr><td>

Release date

</td><td>

Enter the date on which you plan to release the update set.

</td></tr><tr><td>

Application

</td><td>

Populates the application scope that is currently selected in the Application picker. All changes in the update set apply only to the current scope.

</td></tr><tr><td>

Description

</td><td>

Enter a description of the update set.

</td></tr></tbody>
</table>
