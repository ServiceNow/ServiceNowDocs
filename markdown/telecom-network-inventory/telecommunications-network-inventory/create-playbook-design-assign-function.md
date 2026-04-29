---
title: Create a playbook for the Design and Assign function
description: Create a playbook for the Design and Assign function in the Workflow Studio. You can use the playbook to design and assign a network service in the Telecommunications Network Inventory application.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure Design and Assign function, Configure, Telecommunications Network Inventory]
---

# Create a playbook for the Design and Assign function

Create a playbook for the Design and Assign function in the Workflow Studio. You can use the playbook to design and assign a network service in the Telecommunications Network Inventory application.

## Before you begin

-   [Create a Change Model](create-change-model-design-assign-playbook.md).
-   [Create record producers.](create-record-producer-design-assign-playbook.md)
-   [Add input variables to the record producer](create-variables-record-producer-design-assign-playbook.md).
-   [Add variable set to the record producer](add-variable-set-record-producer-design-assign-playbook.md).
-   [Create subflows](create-subflow-design-assign-playbook.md).
-   [Create request definitions](create-request-definition-design-assign-function.md).

You create and configure the playbook in the Workflow Studio to fulfill a service request from the customer. Following are the configuration steps.

1.  Create a playbook.
2.  Add a stage.
3.  Set up the trigger.
4.  Add and configure activities.
5.  Activate the playbook.

Role required: admin, playbook.admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio** &gt; **Playbooks**.

2.  Select **New** and then select **Playbook** from the option list.

3.  Fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |Playbook name|Enter a unique, user-facing name for your playbook. This name appears to agents and fulfillers during runtime of your playbook.|
    |Description|Optionally, enter some descriptive details about your playbook.|
    |Application|Choose an application scope that you want your playbook to run in. You can select **Network Inventory Advanced**.|

    The builder displays in **Diagram view** by default, but you can select **Board view** to switch views.

4.  Add and configure your trigger.

    To learn more, see [Add and configure a trigger in a playbook](https://www.servicenow.com/docs/access?context=add-configure-trigger&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

    1.  Select the more options icon \(![More Options Icon](../../tmt-order-mgt/image/more-options.png) and select **Properties**.

    2.  On the **Schedule** tab, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Define your own conditions for when your process runs|Select the trigger type from the list. You can select **Record Create**.|
        |Table|Select a table to trigger your playbook to run. For Design and Assign function, select **Change Request**. When you create a change request, the playbook gets triggered.|
        |Trigger condition|The conditions that cause your playbook to run. Select your Change model as Trigger condition.|
        |Run my trigger|Select an option to run your trigger. You can select **Once** so that only one playbook process instance is created for design and assign.|

    3.  Select **Done**.

5.  Select **Add Stage** to add a stage.

    You must add only one stage for the Design and Assign function. To learn more about the playbook stage, see [Add and configure a stage in a playbook](https://www.servicenow.com/docs/access?context=add-configure-stage&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

6.  Add and configure the activity.

    1.  Select **Add activity**.

    2.  Select the activity that you want to add in the playbook.

        You can select an existing activity that is associated with the Network Inventory Advanced application and update them according to your requirement. You can also create and add new activity. To learn more about creating an activity, see [Add and configure an activity in a playbook](https://www.servicenow.com/docs/access?context=add-configure-activity&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

<table id="table_kvj_1zg_sdc"><thead><tr><th>

Activity

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Auto Create Change Task

</td><td>

This activity is used to invoke a record producer to create change task record and then display the change task form view. This activity does the following.-   Automatically creates change task​.

-   Invokes the associated record producer​.

-   Creates change task record with record producer variables​.

-   Displays change task form view​ in the activity card.

</td></tr><tr><td>

Display Form

</td><td>

This activity displays the form view according to the selected table and view​.

</td></tr><tr><td>

Review and submit design assign

</td><td>

This activity is used to review and submit a design and assign request. It automatically creates a change task​.

</td></tr></tbody>
</table>        You can also create an activity. To learn more, see [Add and configure an activity in a playbook](https://www.servicenow.com/docs/access?context=add-configure-activity&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

        Your new activity appears in the stage, and the Activity properties panel appears.

    3.  On the **Details** tab, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Label|Enter a unique, user-facing name for your activity. This name appears to agents and fulfillers during runtime of your playbook.|
        |Description|Optionally, enter some descriptive details about your activity.|

    4.  Open the **Automation** tab.

        Automation, Inputs, and Outputs sections appear.

    5.  Select **Show additional options** to view all fields.

    6.  Under the Inputs section, define the values of the activity's inputs.

        Configure inputs with a hard-coded value, or by selecting the data pill picker icon \(![Data Pill Picker Icon](../image/data-pill-picker-icon-01.png)\) to use data from previous activities or the playbook trigger.

    7.  Open the **UI Layout** tab and fill in the fields.

        Depending on the UI Layout associated with the activity, different sections and fields appear on this tab. These sections and fields let you set up the activity data that renders during the runtime Playbook Experience.

    8.  Select **Save and close**.

7.  Keep adding activities according to your design requirement.

8.  After you have added all appropriate activities to your playbook, select **Activate** in the header.

    Activating your playbook publishes it so that it runs when triggered.


## Result

When your playbook's trigger conditions are met, your playbook runs.

## What to do next

Update the system property to add the playbook in the Design and Assign home page. To learn more, see [Update system property to configure the Design and Assign home page](update-system-property-configure-design-assign-home-page.md).

**Parent Topic:**[Configuring Design and Assign function for your network services](../concept/configure-playbooks-design-assign-function.md)

**Related topics**  


[Configuring Design and Assign function for your network services](../concept/configure-playbooks-design-assign-function.md)

[Configure a Design and Assign function example](../concept/configure-design-assign-playbook-use-case.md)

