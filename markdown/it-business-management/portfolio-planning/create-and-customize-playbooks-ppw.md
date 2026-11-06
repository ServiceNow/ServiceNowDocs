---
title: Customize and create playbooks
description: Configure a playbook to match your organization's demand process. Customize the default demand workflow playbook or create one to define the stages and activities that guide demand records through your workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/portfolio-planning/create-and-customize-playbooks-ppw.html
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-11-03"
reading_time_minutes: 7
breadcrumb: [Playbooks in Next Experience for Demand Management, Manage demands, Use, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Customize and create playbooks

Configure a playbook to match your organization's demand process. Customize the default demand workflow playbook or create one to define the stages and activities that guide demand records through your workflow.

## Before you begin

Role required: admin, playbook.admin, or pd\_author

## About this task

Next Experience for Demand Management includes one predefined playbook, Demand workflow. This playbook is active by default and is ready to use without any additional configuration. When the AI Control Tower Core plugin is installed, the playbook includes the AI checkpoint stage. For the stages and activities in the playbook, see [Demand workflow playbook stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/demand-default-playbook-stages-activities-ppw.md).

Customize the playbook when your demand processes differ from the default, for example when you use custom demand states, roles, or fields. The default playbook runs when a demand is created and has no additional conditions. It applies to every new demand, including records in tables that extend the Demand \[dmn\_demand\] table. Duplicate the Demand workflow playbook to customize it to preserve the default playbook as a base that you can refer to at any point.

The demand-specific behavior of the playbook, such as the related lists and the **Mark Complete**, **Save**, and **Skip** actions, comes from the demand playbook experience. Keep your customizations in this experience to use the custom activities built for demands. For more information, see [Demand playbook experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/playbooks-in-demand-workspace-ppw.md).

This overview task covers the configuration of a demand process-specific playbook. For detailed information about creating or customizing playbooks, see [Configuring Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/setting-up-process-automation-designer.md). For a complete example of a custom demand playbook, see [Creation example for a demand playbook for IT governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/example-it-investment-governance-playbook-ppw.md).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**, and then select the **Playbooks** tab.

    The predefined Demand workflow playbook is listed on this tab.

2.  Open the playbook that you want to work with.

    -   To customize the default playbook, duplicate the Demand workflow playbook.
        1.  Select the More actions menu icon \[Omitted image "more-options-icon.png"\] Alt text:.

            \[Omitted image "demand-duplicate-playbook.png"\] Alt text: Duplicate the default playbook and customize the copy.

        2.  Modify the name of the playbook. By default, it is named as Duplicate of Demand workflow.

            The **Application** and **Parent table** fields are auto-populated from the default playbook. These are editable but for demands, the application must be `Portfolio Planning` and the parent table must be `Demand`.

        3.  Add a description for the playbook.
        4.  Select **Duplicate**.
    -   To create a playbook, select **New** &gt; **Playbook**. For next steps, see [Create and configure playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/setting-up-process-automation-designer.md).

        **Note:** If you want to use agentic playbooks, see [Agentic playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/agentic-playbooks-landing.md).

        \[Omitted image "demand-new-playbook.png"\] Alt text: The New drop-down list contains the option to create a playbook.

3.  Configure the trigger.

    1.  Select the **Triggers** icon in the left sidebar.

    2.  Select **Add trigger** or the existing trigger.

    Each demand can map to more than one playbook, based on the trigger. You can create multiple playbooks with different trigger conditions. For detailed steps, see [Triggers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/process-automation-designer-triggers.md).

    -   To run the playbook only for some demands, add conditions to the trigger. For example, to run the playbook only for new demands in the Draft state, add the condition `State is Draft` to a record creation type trigger.
    -   To run the playbook when a demand is updated instead of created, select **When record is updated** or **When record is created or updated** as the trigger type.
    -   To apply the playbook to tables that extend the Demand \[dmn\_demand\] table, select the **Run this trigger on extended tables** check box to apply the trigger to extended tables.
4.  Add or change stages.

    In **Board view**, select **Add Stage**, or select **Add Step** &gt; **Add Stage** to add a stage after an existing one. Set the **Start rule** to **When playbook starts** or **After specific stages**. A stage appears to users only if at least one of its activities is available for the demand. For detailed steps, see [Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/process-automation-designer-lanes-activities.md).

    \[Omitted image "demand-playbook-create-stage.png"\] Alt text: Add menu that has the option to create a stage to add activities.

5.  Add or change the activities in each stage.

    In a stage, select **Add activity** and search for the activity definition, such as Record Form, New Record Form, Instruction, Update Record, or Ask For Ad Hoc Approval. Configure the activity on its tabs:

    -   **Details**: Enter the label and description, and set the **Start rule** to **When stage starts** or **After specific activities**. To run the activity only when a condition is met, select **Show additional options** and add a run condition. For example, run an activity that moves the demand to Approved only if an earlier approval activity returns approved. If the condition is not met, the activity is skipped.
    -   **Automation**: Set the inputs of the activity. To assign the activity, select **Show additional options** and set **Assigned To** or **Assignment Group**. Use the data pill picker to assign the activity to a field on the demand, for example **Parent Record** &gt; **Demand** &gt; **Demand manager**, or enter a specific user or group.
    -   **UI Layout**: Set the associated table and record, the form fields to display, and the tagline that users see on the activity. For automated activities, enter a tagline such as `Automated state change` so that users don't see the default activity name.
    For a record form activity, select the table and the record, and then select the fields to display from the table's form layout. To include a related list in the activity, use the `Demand Related List` custom activity definition. To include a plugin check in any activity, use the `Check if plugin is active` custom action. To run an activity only after another activity is complete, set the activity to start after that specific activity. For detailed steps, see [Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/process-automation-designer-lanes-activities.md).

    For example, to capture a compliance review in the Define demand alignment stage, add a record form activity. Select the custom compliance fields from the Demand \[dmn\_demand\] table. Set the activity to start after the Define strategic alignment activity.

6.  Define what happens to each activity when the playbook is restarted.

    -   **Run always**: Always run this activity, including first runs.
    -   **Skip on restart**: Skip this activity when the run is due to a restart.
    -   **Skip on first run**: Skip this activity during the first run.
    \[Omitted image "demand-playbook-restart.png"\] Alt text: The restart options for an activity.

    The setting on an activity takes precedence over the setting on its stage. For detailed steps, see [Add and configure an activity in a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/add-configure-activity.md).

7.  Configure the automated state changes.

    To move the demand to the next state automatically, add an Update Record activity at the end of the stage that sets the **State** field of the demand. An Update Record activity on its own changes the state without checking any conditions. To check the same conditions as a manual state change, create a custom demand state transition checker activity before the Update Record activity. The Demand workflow playbook uses this approach.

    If you use custom demand states or roles, modify the `DemandPlaybookUtils` script include. For more information, see [Transition checker to move a demand to the next state automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/playbooks-in-demand-workspace-ppw.md).

8.  If you override activities or actions, add the overrides to the Demand playbook experience.

    Overrides that you add to another experience aren't available when the playbook runs in Next Experience for Demand Management. For more information, see [Designing Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-experience-admins.md).

9.  Select **Test** to test your playbook on the selected demand record and select `Demand playbook experience` as the Playbook preview.

    If you test with a different experience, the demand-specific lists and actions don't appear.

10. Select **Activate** to make the playbook live.

    The status changes from Inactive to Active, and new demands that match the trigger start the playbook. After you change an active playbook, select **Activate** again to publish the change. Demands already in progress keep the version of the playbook that they started with.


## Result

The playbook runs for demands that match its trigger. Users see it on the **Playbook** tab of the demand. For more information, see [Use playbook for a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/use-playbooks-in-ppw.md).

**Related topics**  


[Building Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/building-a-process.md)

[Designing Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-experience-admins.md)

[Playbooks in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/playbooks-in-demand-workspace-ppw.md)

[Use playbook for a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/use-playbooks-in-ppw.md)

[Demand workflow playbook stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/demand-default-playbook-stages-activities-ppw.md)

[Creation example for a demand playbook for IT governance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/example-it-investment-governance-playbook-ppw.md)

