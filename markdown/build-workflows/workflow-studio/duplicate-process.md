---
title: Duplicate Playbooks
description: Make a copy of an existing playbook with the same trigger, stages, activities, and experience configurations as the original. Edit the duplicated playbook to quickly create a working variation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/build-workflows/workflow-studio/duplicate-process.html
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Playbooks in Workflow Studio, Building playbooks, Use, Workflow Studio, Build workflows]
---

# Duplicate Playbooks

Make a copy of an existing playbook with the same trigger, stages, activities, and experience configurations as the original. Edit the duplicated playbook to quickly create a working variation.

## Before you begin

-   [Activate playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/activate-process-automation-designer.md) for your appropriate application.
-   Familiarize yourself with the tables and relationships that your application uses for the playbook that you want to create.
-   Make sure to Familiarize yourself with any features that your business uses to automate operations on the ServiceNow AI Platform, such as [flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/exploring-flows.md), [subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/exploring-subflows.md), and [actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/exploring-actions.md).
-   Learn how to [get started with ServiceNow® Process Automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/getting-started-process-automation.md).
-   Role required: admin or playbook.admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio** &gt; **Playbooks**.

    The Playbooks builder appears.

2.  Select the playbook you want to duplicate.

3.  Check the box next to the playbook that you want to duplicate.

    Only one playbook can be duplicated at a time.

    The **Duplicate** button displays.

4.  Select **Duplicate**.

    The system makes a copy of the selected playbook and opens **Duplicate playbook** modal for the new playbook.

5.  Fill in the playbook properties.

<table id="choicetable_ndc_pgy_5lb"><tbody><tr><td id="d155468e217">

**Label**

</td><td>

Enter a unique, user-facing name for your playbook. This name appears during playbook runtime.

</td></tr><tr><td id="d155468e232">

**Application**

</td><td>

Choose an application scope that you want your playbook to run in. Selecting **Global** lets your playbook run in any application scope. For more information, see Application scope.

</td></tr><tr><td id="d155468e254">

**Description**

</td><td>

Optionally, enter some descriptive details about your playbook.

</td></tr><tr><td id="d155468e266">

**Trigger type**

</td><td>

Specify what causes your trigger to fire.

</td></tr><tr><td id="d155468e275">

**Table**

</td><td>

The table with the record operations that you want to trigger your playbook. This field cannot be edited.

</td></tr></tbody>
</table>6.  Edit the playbook stages and activities to fit the new playbook.

7.  Select **Save**.


**Parent Topic:**[Playbooks in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/build-workflows/workflow-studio/process-definitions.md)

**Related topics**  


[Create a playbook]()

[Playbook variants]()

[Test a playbook]()

[Enabling playbook restart]()

[Add translations for playbooks]()

[View all buttons without hover]()

