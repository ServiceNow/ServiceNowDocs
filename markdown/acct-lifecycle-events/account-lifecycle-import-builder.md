---
title: Configure the account onboarding data import task
description: Use the Import Builder to configure the account onboarding data import task.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Data capture and validation, Set up the account onboarding playbook, Configuring account onboarding, Account onboarding, Account Lifecycle Events]
---

# Configure the account onboarding data import task

Use the Import Builder to configure the account onboarding data import task.

## Before you begin

-   Role required: sn\_acct\_lc\_agent
-   One or more Playbooks roles. See [Playbooks roles](https://www.servicenow.com/docs/access?context=process-automation-designer-roles&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) for details.
-   Ensure that you are in the same application scope in which the target table is present.

## Procedure

1.  Navigate to **All** &gt; **Account Lifecycle Events** &gt; **Data Validation Assist Support** &gt; **Import builder**.

2.  Click **New**.

3.  In the **Create template** tab, enter the name and select the **Target table** from the drop down list.

4.  Click the Attachments icon, upload an Excel template and click **Continue**.

    **Note:** The label names in the attached template must match the field names in the target table.

5.  In the Data source step, you can modify the default **Import set table name** and click **Continue**.

    The data source is created and is displayed in the Data Source tab in the Related List. Click the **Name** link to view the data source. Note that the Name field shows the data source name with the prefix `ALE DS` followed by the name of the Import set table name. The internal name of the Import set table is also displayed.

6.  In the Transform map step, you can modify the default **Transform map name** and click **Continue**.

    The transform map is created and displayed in the Transform Map tab in the Related List. Click the **Name** link to navigate to the transform map and view the following:

    -   Source table: This is the Import set table which contains the staging data.
    -   Target table: The table to which the staging data will be moved.
    -   Field maps: Shows the mapping between the fields in the source and target tables.
    The Data validation assist list view with the different types of validations is displayed.

7.  Click **New** \(optional step\) to create a new field level or record level validation or navigate back to the Import Builder page.

8.  In the Playbook activity step, navigate to the UI Views tab in the Related List.

    Note the two list views that have been created. These lists appear in the Data Import step of the account onboarding playbook.

9.  Click **Continue** and navigate to the Activity Definition tab in the Related List.

    Note that a new activity definition has been created and the Import Builder process is now complete.


## What to do next

You can now add this newly created activity definition in the Process Automation Designer and create a new task for the account onboarding playbook by following the instructions in [Add the data import task](../concept/account-lifecycle-add-data-import.md)

.

