---
title: Autocompleting Record Form activity
description: Display a form during runtime to collect input values for your playbook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/autocompleting-user-form.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Non-Interactive activities, Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# Autocompleting Record Form activity

Display a form during runtime to collect input values for your playbook.

## Roles and availability

This activity is available as a common activity. Users with the admin, playbook.admin, or pd\_author can add this activity to a playbook.

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/dot-walking-examples.md).

<table id="table_yv5_b5w_bcc"><thead><tr><th>

Input

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

Start Rule

</td><td>

Choice

</td><td>

Under **Schedule** &gt; **Start Rule**, select a start rule for when the activity should start running:-   **When stage starts**: The activity starts running as soon as its stage starts running.
-   **After specific activities**: The activity starts running after specified activities have finished running. You can select one more activities from the available activities. By default, the previous activity is selected.

</td></tr><tr><td>

Display order

</td><td>

Choice

</td><td>

Option to select the order in which you want to display the activity to end users at run time. From the **Playbook display order** list, select the display order for the activity.

</td></tr><tr><td>

Start with delay

</td><td>

True/False

</td><td>

Option to wait for a duration of time before running an activity or stage. When enabled, this input displays the [Start with delay input properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/start-with-delay-properties.md).**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Run condition

</td><td>

Condition Builder

</td><td>

Conditions that must be met to run an activity or stage. You can use data from prior activities to build conditions.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Restart rules

</td><td>

Choice

</td><td>

The restart rule defines how the activity runs when the playbook is restarted. Options are:-   **Skip on restart**: The stage or activity runs only during the initial run. It does not run when the playbook is restarted. Use this rule when you don't want new tasks or records to be created during a restarted run. This is important if the original execution and its resulting record are still relevant.
-   **Run always**: The activity runs during the initial run and in any restarted run.
-   **Skip on first run**: The activity runs only during a restarted run. It never runs during the initial run.

</td></tr></tbody>
</table>|Input|Type|Description|
|-----|----|-----------|
|Table|Table Name|Table containing the record to update.|
|Record|Reference|Use dot walking to select the record to update.|
|Assignment group|List|From the list of assignment groups, select the group responsible for handling the record.|
|Assigned to|List|From the list of available users, select the person responsible for handling the record.|

## AI Agents

You can add AI agents to this activity and configure the agents to perform tasks within this activity. To learn about how to configure AI agents for the activity, see [Configuring Agentic Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/configure-agentic-playbooks.md).

