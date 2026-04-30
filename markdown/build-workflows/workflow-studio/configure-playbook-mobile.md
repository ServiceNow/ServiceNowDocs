---
title: Configure a playbook for ServiceNow mobile
description: Configuring a playbook for ServiceNow mobile is exactly the same as in a configurable workspace, but with an additional step for embedding the playbook.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Designing playbooks, Use, Workflow Studio, Build workflows]
---

# Configure a playbook for ServiceNow mobile

Configuring a playbook for ServiceNow® mobile is exactly the same as in a configurable workspace, but with an additional step for embedding the playbook.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Workspace Experience** &gt; **Actions &amp; Components** &gt; **Related Items** or **Contextual Side Panel**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_knn_mkn_1mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Action label

</td><td>

Label of the Related Item or Contextual Side panel tab.

</td></tr><tr><td>

Action name

</td><td>

Unique name for your item. This name can be overridden.

</td></tr><tr><td>

Implemented as

</td><td>

Select **UI Component**.

</td></tr><tr><td>

Specify UI component

</td><td>

UI component associated with the action. Enter `now-playbook-experience`.

</td></tr><tr><td>

Icon

</td><td>

Icon that is displayed in the Contextual side panel to differentiate from other components. **Note:** This field is available for the Contextual Side Panel only.

</td></tr><tr><td>

Application

</td><td>

Application for the action assignment.

</td></tr><tr><td>

Workspace

</td><td>

Option to limit a Related Item or Contextual Side Panel to a specific Workspace. For example, Agent Workspace or HR Workspace.

</td></tr><tr><td>

Table

</td><td>

Select the table you want to show the Related Item or Contextual Side Panel on.

</td></tr><tr><td>

View

</td><td>

Field to only display a Playbook when this Form View is selected on the parent record.

</td></tr><tr><td>

Active

</td><td>

Option to activate the action assignment.

</td></tr><tr><td>

Order

</td><td>

Integer that determines the precedence of this action in relation to matching actions with the same name. The lower the number, the more likely it is to be selected against other actions. The typical practice is to use numbers that are in the hundreds. For example, 100, 200, 300, or 400.

</td></tr><tr><td>

Tooltip

</td><td>

Message that's displayed when your mouse points to the Related Item tab or Contextual Side Panel icon.

</td></tr><tr><td>

Description

</td><td>

Description for the action assignment. This description is displayed in the Action Assignment list and provides context on the form.

</td></tr></tbody>
</table>4.  Click the **Advanced View** related link.

5.  Click the **Component Attributes** tab.

6.  On the form, fill in the fields.

<table id="table_w4t_vnn_1mb"><thead><tr><th>

Attribute name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

playbookExperienceId

</td><td>

Associated Playbook experience ID. Copy and paste the sys\_id of a Playbook Experience record.**Note:** If no Playbook experience ID is provided, the global Playbook experience is used by default.

</td></tr><tr><td>

parentSysId

</td><td>

Associated parent sys\_id. Enter`{{sysId}}` to automatically take the parentSysId of the record that you're viewing.

</td></tr><tr><td>

parentTable

</td><td>

Associated parent table. Enter `{{table}}` to automatically take the parentSysId of the record that you're viewing.

</td></tr><tr><td>

compactMode

</td><td>

Option to display a Playbook in compact mode. Typically set to true for Contextual Side Panel and false for Related Item.

</td></tr><tr><td>

recordGeneratorQuery

</td><td>

Not currently supported in Agent Workspace.

</td></tr><tr><td>

isNewParentRecord

</td><td>

Set to `{{isNewRecord}}`.

</td></tr></tbody>
</table>    **Note:** Select a different **UI Component** if the attributes are missing from your form. Change the **UI Component** back to **now-playbook-experience** and the attributes will appear.

7.  Select **Update**.

8.  Click the **Conditions** tab.

9.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Script Condition|Script condition for the action assignment. Enter `sn_playbook.PlaybookExperience.parentRecordContainsPlaybook(current)`. The script condition enables you to show a Playbook only when the record has triggered a process execution.|
    |Client Conditions|Choose conditions to limit collisions based on your use case.|
    |Record Conditions|Choose conditions to limit collisions based on your use case.|
    |Required Roles|Roles to limit Playbook access.|
    |Requires create access|Option to require create access.|
    |Requires read access|Option to require read access.|
    |Requires write access|Option to require write access.|
    |Requires delete access|Option to require delete access.|

10. Select **Update**.


## Result

The playbook is configured for ServiceNow® mobile.

## What to do next

Embed your playbook in ServiceNow® mobile. To learn more, see

-   **[Embed a playbook in ServiceNow mobile](embed-playbook-mobile.md)**  
Embed a playbook in ServiceNow® mobile by creating a screen in Mobile App Builder.

**Parent Topic:**[Designing playbooks](../concept/playbook-experience-admins.md)

