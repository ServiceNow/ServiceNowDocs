---
title: Create a playbook
description: Create a playbook to set up an automated business process. Use Playbook builder in Workflow Studio to add stages, activities, triggers, and runtime permissions, then activate the playbook to make it available to agents and fulfillers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/create-process-definition.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 4
breadcrumb: [Creating and managing Playbooks, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Create a playbook

Create a playbook to set up an automated business process. Use Playbook builder in Workflow Studio to add stages, activities, triggers, and runtime permissions, then activate the playbook to make it available to agents and fulfillers.

## Before you begin

-   Activate the Playbook application for your instance. See [Activate Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/activate-process-automation-designer.md).
-   Familiarize yourself with the tables and relationships that your application uses for the playbook that you want to create.
-   Familiarize yourself with any features that your business uses to automate operations on the ServiceNow AI Platform, such as [flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/exploring-flows.md), [subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/exploring-subflows.md), and [actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/exploring-actions.md).
-   Role required: admin, playbook.admin, or playbook.write.

## About this task

Use this procedure to build a new playbook from scratch. You can create a playbook with no trigger, a single trigger, or multiple triggers. If you change a playbook after activating it, the system saves your changes but deactivates the playbook. You must activate the playbook again to publish any new changes.

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio** &gt; **Playbooks**.

    The Workflow Studio landing page opens with the Playbooks list displayed by default.

2.  In the upper-right corner, under **New**, select **Playbook**.

3.  Fill in the following fields.

    |Field|Description|
    |-----|-----------|
    |**Playbook name**|Unique, user-facing name for the playbook. Appears to agents and fulfillers at runtime.|
    |**Application**|Application scope for the playbook. Select **Global** to run the playbook in any application scope.|
    |**Description**|Descriptive details about the playbook.|

4.  Select **Build playbook**.

    The builder displays in **Diagram view** by default, but you can select **Board view** to switch between views anytime as you build your playbook.

    \[Omitted image "board-view.png"\] Alt text: Diagram and Board view toggle

5.  Select the **Start** node.

    The Playbook properties side panel opens.

6.  Under the **Details** tab, fill in the fields.

    You can also update the Playbook name and Description.

<table id="table_lhw_frm_njc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Limit playbook executions for each parent record to**

</td><td>

Maximum number of times the playbook can run for a single parent record.

</td></tr><tr><td>

**Execution type**

</td><td>

Type of playbook to create.-   **Record driven:** Playbook tied to a record. Triggered on demand or automatically based on record operations. Data from the playbook is stored on that record.
-   **Standalone:** Single-session playbook that does not store data to a record. Must be manually triggered or called from another playbook.


</td></tr><tr><td>

**Parent table**

</td><td>

Table that provides trigger records and other playbook inputs. Required for Knowledge and Email activities.

</td></tr><tr><td>

**Allow this playbook to be restarted during runtime**

</td><td>

When selected, runtime users can restart the entire playbook during a run.

</td></tr></tbody>
</table>7.  Under the **Inputs** tab, add inputs for a playbook to launch with.

    Inputs defined here are accessible throughout the playbook via dot-walking and dot notation, for example `inputs.inputName`, and can be used in activity fields, conditions, and UI elements.

    **Tip:** To trigger a playbook with API inputs instead of trigger records, use the `triggerPlaybook(String scopedName, GlideRecord parentRecord)` API to trigger a playbook. For more information about the API, search `triggerplaybook` on the ServiceNow Developer Site: [Playbook Experience APIs](https://developer.servicenow.com/dev.do#!/reference/api/zurich/server/sn_playbook-namespace/PlaybookExperienceScopedAPI).

8.  Under the **Runtime permissions** tab, configure permissions for users, user groups, user criteria, and roles.

9.  Configure a trigger for the playbook.

    You can create a playbook with no trigger, a single trigger, or multiple triggers. For more information, see [Add and configure a trigger in a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/add-configure-trigger.md).

10. Add activities, stages, decision nodes, and parallel branches as required to automate your process.

    Continue adding stages and activities until your playbook reflects the full business process. For more information, see [Stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/process-automation-designer-lanes-activities.md).

11. Add a variant to your playbook.

    You can use one playbook in multiple use cases by using variants. For more information, see [Playbook variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-variants.md).

12. After adding all stages and activities, test the playbook.

13. After testing the playbook, select **Activate** in the header.

    The playbook is published and runs when its trigger conditions are met.


## Result

When the trigger conditions of the playbook are met, the system creates a Process Execution record and renders user-facing configurations for Playbook Experience. For an example of how to digitize a manual business process, see [Create a sample playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/design-automated-process.md).

## What to do next

Set up the Playbook Experience for your agents and fulfillers.

**Parent Topic:**[Creating and managing Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/creating-managing-playbooks.md)

