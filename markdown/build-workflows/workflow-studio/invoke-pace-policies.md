---
title: Invoke PaCE activity
description: Enable the Policy as Code Engine \(PaCE\) activity in Playbooks to develop playbook processes.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Interactive activities, Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# Invoke PaCE activity

Enable the Policy as Code Engine \(PaCE\) activity in Playbooks to develop playbook processes.

## Roles and availability

These activities are available as part of the application that is automatically bundled with PaCE. Users with the admin, pd\_admin, pd\_author, or pd\_content\_author can add these activities to a playbook.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see Dot-walking examples.

<table id="table_qmc_knm_sbc"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

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

Information to display about activity usage or outcome.

</td></tr><tr><td>

Run condition

</td><td>

Condition Builder

</td><td>

Conditions that must be met to run an activity. You can use data from prior activities to build conditions.

</td></tr><tr><td>

When to start

</td><td>

Choice

</td><td>

Select a start rule for when your activity should start running:-   **Immediately**: Your activity starts running as soon as its stage starts running. Your stage starts running when your playbook is triggered.
-   **Before previous**: Your activity starts before specified activities have finished running.
-   **After previous**: Your activity starts running after specified activities have finished running.

</td></tr><tr><td>

Start with delay

</td><td>

True/False

</td><td>

Option to wait for a duration of time before running an activity or stage. When enabled, this input displays the [Start with delay input properties](start-with-delay-properties.md).

</td></tr><tr><td>

Service

</td><td>

String

</td><td>

The calling service that is invoking the PaCE API.

</td></tr><tr><td>

Category

</td><td>

String

</td><td>

The category type.

</td></tr><tr><td>

Policy tag

</td><td>

String

</td><td>

Tag name of the policy.

</td></tr><tr><td>

Document Ids

</td><td>

Array.Object

</td><td>

Name of document IDs.

</td></tr><tr><td>

Data

</td><td>

JSON

</td><td>

The policy-specific data that includes all possible caller inputs.

</td></tr><tr><td>

Options

</td><td>

Object

</td><td>

Options of the policy.

</td></tr></tbody>
</table>## Outputs

The outputs are configurable in Flow Designer and are set by the Automation plan.

|Label|Type|
|-----|----|
|Root execution id|Sys ID \(GUID\)|
|Don't Treat as Error|True/False|
|Response|JSON|
|Action Status|String|

