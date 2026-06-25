---
title: Creating and managing Playbooks
description: Learn how to create and configure a playbook in Workflow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/creating-managing-playbooks.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Creating and managing Playbooks

Learn how to create and configure a playbook in Workflow Studio.

You can view your list of Playbooks by navigating **Process Automation** &gt; **Workflow Studio** &gt; **Playbooks**. Opening a playbook allows you to edit it. If there are no playbooks in the list, you can create a new one by clicking **New** and selecting **Playbook**. For more information on creating a playbook, see [create a process definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-process-definition.md).

## Playbook properties

After you create a playbook, access its properties by opening it, and selecting **Properties** in the **More actions** menu in the upper right corner of the header. In the **Additional properties** modal, you can edit the following information:

<table id="table_ezy_jn4_rlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Name of the playbook to display in Workflow Studio and in a Playbook Experience.

</td></tr><tr><td>

Description

</td><td>

Description of what your playbook does.

</td></tr><tr><td>

Conditions

</td><td>

Conditions that must be met to run your playbook.

</td></tr><tr><td>

Run my trigger

</td><td>

Option that defines how many times your trigger can run for your playbook. Choices include:-   **Once**: Triggers the playbook once for the life of the triggering input record.
-   **Only if not currently running**: Triggers the playbook for every unique change if a process execution is not currently running.
-   **For every update**: Triggers the playbook every time the input record is updated, regardless of whether there has already been or there currently are any running process executions.

</td></tr><tr><td>

Run on extended

</td><td>

Option to trigger your playbook when record operations occur on tables that extend the input table. For example, if your selected table is the Task \[task\] table and you select this option, your playbook triggers when a Problem \[problem\] record is created or updated. For more information, see [Table extension and classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/table-extension-and-classes.md).

</td></tr></tbody>
</table>**Note:** After you create a playbook, you can't change the trigger's input table or trigger type.

## Design considerations

Refer to these design considerations when working with playbooks:

-   **Avoid duplicating business logic used in Workflow Studio, Workflow, and business rules**

    Replace separate business logic such as business rules, flows, and workflows with a consolidated playbook. Make sure that you deactivate any external business logic you replace to avoid duplication of effort.

-   **Ignore records added or updated by import and update sets**

    Record triggers ignore records added or updated by applying an update set or importing an XML file. These operations apply to the entire application or table rather than an individual record.


-   **[Create a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-process-definition.md)**  
Create a playbook to set up an automated business process. Use Playbook builder in Workflow Studio to add stages, activities, triggers, and runtime permissions, then activate the playbook to make it available to agents and fulfillers.
-   **[Test a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/test-process.md)**  
Verify that your playbook works as expected by running the playbook with test trigger data. Identify and resolve all errors before activating your playbook.
-   **[Enabling playbook restart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/restart.md)**  
Learn how playbook restart during runtime works and how restart rules control the behavior of stages and activities during a restarted run.
-   **[Duplicate a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/duplicate-process.md)**  
Make a copy of an existing playbook with the same trigger, stages, activities, and experience configurations as the original. Edit the duplicated playbook to quickly create a working variation.
-   **[Playbook summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-summarization.md)**  
Use AI-generated overviews of a playbook's stages, activities, triggers, and inputs to understand its purpose and flow without going into the details of what is being done at activity and stage level.
-   **[Add translations for Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/add-translations-playbooks.md)**  
Make Playbooks available in multiple languages during runtime, to support worldwide business processes.

**Parent Topic:**[Building Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/building-a-process.md)

**Related topics**  


[Designing Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-experience-admins.md)

[Running Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-agents-and-fulfillers.md)

