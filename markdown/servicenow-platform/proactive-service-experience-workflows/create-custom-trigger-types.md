---
title: Create custom trigger types
description: Create your own trigger type during the rule creation process that is specific to your organization for improved Proactive Triggers usage.
locale: en-US
release: xanadu
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Proactive Triggers, Proactive Triggers, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create custom trigger types

Create your own trigger type during the rule creation process that is specific to your organization for improved Proactive Triggers usage.

## Before you begin

Role required: sn\_pt.proactive\_admin or admin

## About this task

For a more advanced configuration, create your own custom trigger types. You can create custom trigger types through two different paths.

1.  Through the **View All** button next to the **Trigger types** field in **Conversational Interfaces** &gt; **Settings** &gt; **General** &gt; **Proactive triggers**.
2.  Through the rule creation process.

## Procedure

1.  Navigate to **Conversational Interfaces** &gt; **Settings** &gt; **General**, and then select **View All** next to the **Rules** field in Proactive Triggers.

2.  Select **New** to display the Proactive Rule form.

3.  Next to the **Trigger type** field, select the create new trigger type icon \(![Create new trigger type icon.](../../../reuse/itom/image/workspace-icon-add.png)\).

4.  On the form, fill in the fields.

<table id="table_vwz_xk5_cxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the custom trigger type.

</td></tr><tr><td>

ID

</td><td>

System-generated, read-only ID required for API calls. This ID is only displayed after you've submitted the new trigger type and you view the trigger record.

</td></tr><tr><td>

Description

</td><td>

Trigger type description.

</td></tr><tr><td>

Order

</td><td>

Trigger run order whenever two rules conflict in the same time frame. The lowest number is evaluated first when multiple triggers are running at the same time.

</td></tr><tr><td>

Active

</td><td>

Option to activate the trigger type so that it’s available as a trigger type when creating a rule.

</td></tr><tr><td>

Trigger table

</td><td>

The table referenced in the rule condition builder. Only one trigger type can exist for the same referenced table. For example, if you try to create a trigger type referencing the Knowledge \[kb\_knowledge\] table with a Web browsing source, an error appears when saving the trigger type. This error appears because the default Knowledge trigger already uses this same table and source.

</td></tr><tr><td>

Source

</td><td>

The trigger initiation is either **System API** or **Web browsing**. -   **System API**: Calls the Proactive Triggers API. For example, a business rule on the trigger table calls the API that initiates the trigger.

**Note:** Trigger types with the **System API** source only work for internal ServiceNow sites and not external sites.

-   **Web browsing**: Calls to a URL. The default active trigger types are associated with the web browsing source.


</td></tr><tr><td>

Applicable portal

</td><td>

The trigger type is only applicable to select pages on a particular portal.

</td></tr></tbody>
</table>

    ![Create Trigger Type form.](../image/pt-create-custom-trigger-type.png)

5.  Select **Submit**.

    The new, custom trigger type appears as the **Trigger Type** field value.


## What to do next

After creating the custom trigger type, the **Create new trigger type** button updates to the **Preview this record** button \(![Preview.](../image/workspace-icon-preview.png)\). Select **Preview this record** to preview the new trigger type that you created and view the system-generated ID. To make edits to this trigger type, select **Open Record** to manage the parameters of the custom trigger type.

Also, you can make edits to this new trigger type by selecting **View All** next to the **Trigger types** field in **Conversational Interfaces** &gt; **Settings** &gt; **General** &gt; **Proactive triggers**.

