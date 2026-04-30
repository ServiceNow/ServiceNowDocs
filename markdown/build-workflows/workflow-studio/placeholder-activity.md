---
title: Placeholder activity
description: Display an activity card in Playbooks to indicate what a future activity does.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Playbooks reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Placeholder activity

Display an activity card in Playbooks to indicate what a future activity does.

## Roles and availability

This activity is available as a common activity. Users with the admin, playbook.admin, or pd\_author can add this activity to a playbook.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://www.servicenow.com/docs/access?context=dot-walking-examples&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

<table id="table_ajt_sr3_plb"><thead><tr><th>

Input

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Edit

</td><td>

Choice

</td><td>

Activities that you can select to replace the placeholder.

</td></tr><tr><td>

Label

</td><td>

String

</td><td>

Title to display as activity and playbook card.

</td></tr><tr><td>

Description

</td><td>

String

</td><td>

Information to display about activity usage or outcome. You can use this input to describe the activity needed to replace this placeholder.

</td></tr><tr><td>

Run condition

</td><td>

Condition Builder

</td><td>

Conditions that must be met to run an activity or stage. You can use data from prior activities to build conditions.**Note:** **Show additional options** to see this field.

</td></tr><tr><td>

Start Rule

</td><td>

Choice

</td><td>

Under **Schedule** &gt; **Start Rule**, select a start rule for when your stage should start running:-   **When process starts**: Your stage starts running as soon as the playbook starts.
-   **After specific stages**: Your stage starts running after specified stage\(s\) have finished running.

Under Schedule &gt; Start Rule, select a start rule for when your activity should start running:-   **When stage starts**: Your activity starts running as soon as its stage starts running. Your stage starts running when your playbook is triggered.
-   **After specific activities**: Your activity starts running after specified activities have finished running.

</td></tr></tbody>
</table>## Outputs

This activity does not produce output.

## Design considerations

-   **Add placeholders activities to skip activity configuration**

    Playbooks designers can use placeholder activities to communicate the intent of an activity or playbook without having to do any configuration. Playbook designers can defer configuration to another time or delegate the configuration to another user who may better understand the playbook data model.

-   **Edit placeholder activities to replace them with other activities**

    Placeholder activities help playbook designers create playbook, but do not produce any output or advance a playbooks when run. Edit Placeholder activities when you are ready to replace them with another activity type and configure them.


**Parent Topic:**[Playbooks reference](process-automation-designer-reference.md)

