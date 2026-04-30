---
title: Create a fix script
description: Create fix scripts to ensure the system installs or updates an application properly.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Fix scripts, Anatomy of an application, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Create a fix script

Create fix scripts to ensure the system installs or updates an application properly.

## Before you begin

Role required: script\_fix\_admin or admin

## About this task

Use fix scripts to add, update, and delete data, including rules, scripts, and property settings.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Fix Scripts**.

2.  Click **New**.

3.  Define the fix script by filling in the fields on the form.

<table id="table-fix-script-fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique, descriptive name for the fix script.

</td></tr><tr><td>

Unloadable

</td><td>

Option to create Customer Update records \[sys\_update\_xml\] when the fix script runs. Fix script tests enforce the Unloadable option.

</td></tr><tr><td>

Before

</td><td>

Option to run the fix script before installing or upgrading the application.

</td></tr><tr><td>

Record for rollback

</td><td>

Option to record execution of the script so that it can be reverted if needed.

</td></tr><tr><td>

Description

</td><td>

Description of the fix script.

</td></tr><tr><td>

Script

</td><td>

Code for the fix script.

</td></tr></tbody>
</table>4.  Click **Submit**.

5.  Test the fix script and make any necessary changes.


