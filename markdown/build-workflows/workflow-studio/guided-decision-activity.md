---
title: Guided Decision activity
description: Choose a decision tree from your Guided Decisions framework to step agents through how to proceed with a task.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Interactive activities, Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# Guided Decision activity

Choose a decision tree from your Guided Decisions framework to step agents through how to proceed with a task.

## Roles and availability

This activity is available with a subscription to App Engine or Customer Service Management \(CSM\). For more information on how to enable this activity for use in Playbooks, see [Activate Playbooks for Customer Service Management \(CSM\)](../task/activate-process-automation-designer-for-csm.md).

## Inputs

Open the activity properties panel and configure your activity to add values for the following inputs. If the input value varies, use the pill-picker to show where to get the value. To learn more about the pill-picker, see [Dot-walking examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/dot-walking-examples.md).

<table id="table_ajt_sr3_plb"><thead><tr><th>

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

Run condition

</td><td>

Condition Builder

</td><td>

Conditions that must be met to run an activity or stage. You can use data from prior activities to build conditions.**Note:** Select **Show additional options** to see this field.

</td></tr><tr><td>

Start Rule

</td><td>

Choice

</td><td>

Under **Schedule** &gt; **Start Rule**, select a start rule for when your stage should start running:-   **When process starts**: Your stage starts running as soon as the playbook starts.
-   **After specific stages**: Your stage starts running after specified stage\(s\) have finished running.

Under Schedule &gt; Start Rule, select a start rule for when your activity should start running:-   **When stage starts**: Your activity starts running as soon as its stage starts running. Your stage starts running when your playbook is triggered.
-   **After specific activities**: Your activity starts running after specified activities have finished running.

</td></tr><tr><td>

Start with delay

</td><td>

True/False

</td><td>

Option to wait for a duration of time before running an activity or stage. When enabled, this input displays the [Start with delay input properties](start-with-delay-properties.md).**Note:** Select **Show additional options** to see this field.

</td></tr></tbody>
</table>## Advanced inputs

After configuring the required inputs for your activity, you can also choose to configure additional inputs. In the side panel, select **Show additional options** to display these advanced inputs. For more information, see [Activity experience](../concept/activity-definitions.md#activity-experience).

|Input|Type|Description|
|-----|----|-----------|
|Decision Tree|Reference|The Decision Tree \[ga\_decision\_tree\] record whose decision inputs and guidance you want to show to agents in the Workspace playbook. For more information on how to set up the Guided Decisions framework, see [Configuring Guided Decisions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/setting-up-guided-decisions.md).|
|Task|Reference|The triggering Case \[sn\_customerservice\_case\] record.|

## Outputs

There are no outputs for this activity.

