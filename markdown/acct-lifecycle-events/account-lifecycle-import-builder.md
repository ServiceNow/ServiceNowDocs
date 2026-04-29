---
title: Configure the account onboarding data import task
description: Use the Import Builder to configure the account onboarding data import task.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data capture and validation, Set up playbook, Account onboarding, Configure, Customer Success Management]
---

# Configure the account onboarding data import task

Use the Import Builder to configure the account onboarding data import task.

## Before you begin

-   Role required: sn\_acct\_lc\_agent
-   One or more Playbooks roles. See [Playbooks roles](https://www.servicenow.com/docs/access?context=process-automation-designer-roles&version=australia&pubname=australia-build-workflows&ft:locale=en-US) for details.
-   Confirm that you're in the same application scope in which the target table is present.

## Procedure

1.  Navigate to **All** &gt; **Customer Success Management** &gt; **Data Validation Assist Support** &gt; **Import builder**.

2.  Select **New**.

3.  In the **Create template** tab, enter the name and select the **Target table** from the drop-down list.

4.  Select the Attachments icon, upload an Excel template, and select **Continue**.

    **Note:** The label names in the attached template must match the field names in the target table.

5.  In the Data source step, you can modify the default **Import set table name** and select **Continue**.

    The data source is created and is displayed in the Data Source tab in the related list. Select the **Name** link to view the data source. Note that the Name field shows the data source name with the prefix `Customer Success DS` followed by the name of the Import set table name. The internal name of the Import set table is also displayed.

6.  In the Transform map step, you can modify the default **Transform map name** and select **Continue**.

    The transform map is created and displayed in the Transform Map tab in the related list. Select the **Name** link to navigate to the transform map and view the following:

    -   Source table: This is the Import set table that contains the staging data.
    -   Target table: The table in which the staging data is stored.
    -   Field maps: Shows the mapping between the fields in the source and target tables.
    The Data validation assist list view with the different types of validations is displayed.

7.  Select **New** \(optional step\) to create a field level or record level validation or navigate back to the Import Builder page.

8.  In the Playbook activity step, navigate to the UI Views tab in the related list.

    Note the two list views that have been created. These lists appear in the Data Import step of the account onboarding playbook.

9.  Select **Continue** and navigate to the Activity Definition tab in the related list.

    Note that a new activity definition has been created and the Import Builder process is now complete.


## What to do next

Add this newly created activity definition in the Process Automation Designer and follow the instructions in [Add the data import task](../concept/account-lifecycle-add-data-import.md) section to create an onboarding playbook task.

.

**Parent Topic:**[Data capture and validation](../concept/account-lifecycle-use-playbook-data-capture.md)

