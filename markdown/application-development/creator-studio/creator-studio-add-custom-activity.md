---
title: Make a custom activity available for playbooks in Creator Studio
description: You must add custom activities to the Creator Studio Activities table \[sn\_creatorstudio\_activity\] before users can add them to playbooks when building apps.
locale: en-US
release: yokohama
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Administering activities in Creator Studio, Administering Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Make a custom activity available for playbooks in Creator Studio

You must add custom activities to the Creator Studio Activities table \[sn\_creatorstudio\_activity\] before users can add them to playbooks when building apps.

## About this task

You may want to create custom activities for complex or company-specific workflows. For example:

-   The standard Request approval activity has a **Requester's manager** option, but you may need a **Department manager** instead.
-   You may need an approval or flow with more complex decision logic than is easily built in the Creator Studio automation. You could use Workflow Studio to build that flow, and then create a custom action that calls it.
-   You may want more notification types than the standard Email notification activity. You could create a flow that sends a notification to a MS Teams integration, and create an activity that calls that flow.

## Before you begin

The following steps must be completed before you can make a custom activity available in Creator Studio:

1.  **Create the flow, subflow, or action**: An admin or someone with the correct role must first create the flow, subflow, or action in Workflow Studio. For more information, see [General guidelines for Workflow Studio flows, subflows, and actions](https://www.servicenow.com/docs/access?context=design-considerations-consolidated&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).
2.  **Define the activity**: An admin then defines the activity by adding it to the Activity Definition table and assigning the flow/subflow/action to a playbook activity. This step is also when the admin specifies which inputs can be made available as fields in the activity settings in Creator Studio playbooks. For more information, see [Activity definitions](https://www.servicenow.com/docs/access?context=activity-definitions&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) and [Create an activity definition](https://www.servicenow.com/docs/access?context=create-activity-definition&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

    **Note:** If an activity definition already exists for the activity you want, you can skip this step.


Role required: admin or app\_engine\_admin

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **Request App Administration** &gt; **Creator Studio Activities**.

    All of the standard Creator Studio activities appear in the list, not just custom activities.

    The Creator Studio Activities table appears.

    ![Table showing all activities defined for Creator Studio playbooks](../image/crs-activities-table.png "Creator Studio Activities table")

2.  Create the basis of the new activity.

    1.  Select the **New** button.

    2.  On the record, fill in the fields.

<table id="table_tls_s13_xcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity

</td><td>

Search for and select the type of activity that will be the basis of your custom activity.For example, create a complex approval activity by selecting **Request Multi-Level Approval**.

**Note:** Once you choose an activity, you can select the information icon \(![](../../app-engine-studio/image/icon-information.png)\) to preview its Activity Definition record.

</td></tr><tr><td>

Order

</td><td>

Order that the activity appears in the Creator Studio activity picker list.For example, an activity with order number 400 appears before an activity with order number 500.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the custom activity, which appears in the activity picker.

</td></tr></tbody>
</table>        To see a list of all the available activities you can add:

        -   See [Workflow Studio actions](https://www.servicenow.com/docs/access?context=flow-actions&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) for all standard actions.
        -   See [Workflow Studio flow logic](https://www.servicenow.com/docs/access?context=flow-logic&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) for a list of all flows.
        -   See your list of all available subflows in Workflow Studio.
    3.  Confirm that the **Active** option is selected to make the activity appear in Creator Studio.

    4.  Select **Submit**.

3.  Specify which fields appear in the playbook activity's properties panel.

    **Note:** The fields that appear may have already been configured in the process of defining the activity. If so, follow these steps to verify that the available fields are correct.

    1.  Open the definition for the newly created activity by selecting it from the **Activity** column of the Creator Studio Activities table.

    2.  Confirm that the **Automation Plan** tab is selected.

    3.  Make the field appear for the activity’s properties in a Creator Studio by selecting **Always Show**.

        For example, set the **Assigned To** field to **Always Show** to users building a playbook in Creator Studio.

        ![Select Always Show to make a field appear](../image/crs-activity-inputs.png "Inputs for activities")

        For more information, see [Add dynamic inputs to an activity](https://www.servicenow.com/docs/access?context=add-dynamic-inputs-to-activity&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

    4.  Hide a field from the properties panel by setting it to **Show as additional property for admins only.**

    5.  Repeat these steps for every field that should be visible on the properties panel.

    6.  Save the record.

4.  Return to the Creator Studio Activities table.

5.  Review the Creator Studio Activity record by selecting is **Short Description** field.

6.  Confirm that the **Active** option is selected, and that everything else is correct.

7.  Save the record if you made any additional changes by selecting the **Update** button.


## Result

The new activity appears in the activity picker in Creator Studio.

![The activity we added appears at the end of the activity picker](../image/crs-activity-added.png "New activity appears in the activity picker")

**Parent Topic:**[Administering activities in Creator Studio](../concept/creator-studio-administering-activities.md)

