---
title: Create and select an update set as the current set
description: Create an update set to store customization changes and select it as the current set.
locale: en-US
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with update sets, System update sets, Deploying applications, Building applications]
---

# Create and select an update set as the current set

Create an update set to store customization changes and select it as the current set.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets** and select **New**.

2.  Fill in the form.

<table id="table_nln_kgn_vp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name for the update set. You can use naming conventions to organize update sets.

</td></tr><tr><td>

State

</td><td>

-   In progress: The update set tracks customizations and displays in progress update sets in the picker.
-   Completed: The update set is complete. Use completed update sets to transfer changes from one instance to another.
-   Ignore: The work on an update set is stopped, but you don’t want it to be transferred to another instance. Set completed update sets on the production instance to ignore to help prevent additional commits when cloning the instance.


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
</table>3.  Select **Submit** to create the update set or select **Submit and Make Current**.


**Parent Topic:**[Working with update sets](../concept/using-system-update-sets.md)

