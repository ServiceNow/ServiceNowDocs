---
title: Duplicate Playbooks
description: Make a copy of an existing playbook with the same trigger, stages, activities, and experience configurations as the original. Edit the duplicated playbook to quickly create a working variation.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Playbooks in Workflow Studio, Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Duplicate Playbooks

Make a copy of an existing playbook with the same trigger, stages, activities, and experience configurations as the original. Edit the duplicated playbook to quickly create a working variation.

## Before you begin

-   [Activate playbooks](../concept/activate-process-automation-designer.md#) for your appropriate application.
-   Familiarize yourself with the tables and relationships that your application uses for the playbook that you want to create.
-   Make sure to familiarize yourself with any features that your business uses to automate operations on the ServiceNow AI Platform, such as [flows](../../workflow-studio/concept/exploring-flows.md), [subflows](../../workflow-studio/reference/exploring-subflows.md), and [actions](../../workflow-studio/concept/exploring-actions.md).
-   Learn how to [get started with ServiceNow® Process Automation](../concept/getting-started-process-automation.md).
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

<table id="choicetable_ndc_pgy_5lb"><tbody><tr><td id="d146086e217">

**Label**

</td><td>

Enter a unique, user-facing name for your playbook. This name appears during playbook runtime.

</td></tr><tr><td id="d146086e232">

**Application**

</td><td>

Choose an application scope that you want your playbook to run in. Selecting **Global** lets your playbook run in any application scope. For more information, see [Application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

</td></tr><tr><td id="d146086e254">

**Description**

</td><td>

Optionally, enter some descriptive details about your playbook.

</td></tr><tr><td id="d146086e266">

**Trigger type**

</td><td>

Specify what causes your trigger to fire.

</td></tr><tr><td id="d146086e275">

**Table**

</td><td>

The table with the record operations that you want to trigger your playbook. This field cannot be edited.

</td></tr></tbody>
</table>6.  Edit the playbook stages and activities to fit the new playbook.

7.  Select **Save**.


**Parent Topic:**[Playbooks in Workflow Studio](../concept/process-definitions.md)

**Related topics**  


[Create a playbook](create-process-definition.md)

[Playbook variants](../concept/playbook-variants.md)

[Test a playbook](test-process.md)

[Restart](../concept/restart.md)

[Add translations for playbooks](add-translations-playbooks.md)

