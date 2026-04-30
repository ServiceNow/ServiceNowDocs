---
title: Create a Task Mining project
description: Create a Task Mining project to analyze data for a specific purpose, and define how long project data is collected for.
locale: en-US
release: yokohama
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2024-08-28"
reading_time_minutes: 1
breadcrumb: [Defining the scope of projects, Use, Task Mining, Platform Analytics]
---

# Create a Task Mining project

Create a Task Mining project to analyze data for a specific purpose, and define how long project data is collected for.

## Before you begin

Role required: sn\_tm\_core.analyst, sn\_tm\_core.power\_user, sn\_tm\_core.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Select **New project**.

3.  On the form, fill in the fields.

4.  <table id="table_plp_4db_kcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the project.

</td></tr><tr><td>

Anonymization level

</td><td>

How users are identified for the project. Available options are determined by the Minimum level of anonymization configuration record. The available options are:-   **Login Name**: Identified by name.
-   **Initial**: Identified by initial.
-   **Anonymized Code**: Identified by a string of random characters.


</td></tr><tr><td>

Start date

</td><td>

Date to start collecting workstation user data.

</td></tr><tr><td>

End date

</td><td>

Date to stop collecting workstation user data.

</td></tr><tr><td>

Description

</td><td>

Optional description of the project.

</td></tr></tbody>
</table>5.  Select **Save**.


## What to do next

Select workstation users you want to collect activity data from and create data requests. For more information, see [Add workstation users to a Task Mining project](add-users-to-task-mining-project.md).

