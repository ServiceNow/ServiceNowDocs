---
title: Building triggers
description: A trigger contains the start conditions for your automation. You can create separate triggers for each flow or create a reusable saved trigger that you can use in multiple flows.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-06-19"
reading_time_minutes: 2
---

# Building triggers

A trigger contains the start conditions for your automation. You can create separate triggers for each flow or create a reusable saved trigger that you can use in multiple flows.

By creating a saved trigger, you enable the flow authors to use a predefined trigger rather than creating a new trigger definition for their flow. You can use the same trigger in multiple flows. Any changes made to the trigger are propagated to each flow that uses the trigger.

The following video demonstrates how you can use saved triggers in Workflow Studio.

Saved triggers in Workflow Studio 

## UI elements

The Workflow Studio home page displays a **Triggers** option in the list of available components and the list of new components.

![Screen to create a new trigger.](../images/trigger-create-new.png)

When you create a new trigger, you must enter the trigger properties on the **New Trigger** form.

<table id="table_p35_zpc_wfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Trigger name

</td><td>

Unique name to identify the trigger.

</td></tr><tr><td>

Trigger type

</td><td>

Type of trigger to start your flow.You can create a saved trigger for any of the following trigger types:

-   Record
-   Scheduled
-   External \(Webhooks\)

For more information about trigger types, see [Workflow Studio flow trigger types](../reference/flow-triggers.md).

</td></tr><tr><td>

Description

</td><td>

Description of the trigger.

</td></tr><tr><td>

Application

</td><td>

Application to create the trigger. The default is Global.The application scope determines which data your trigger can access and what data it can share.

</td></tr><tr><td>

Domain

</td><td>

Domain scope of the flow. For more information about domain separation, see [Domain separation explained](https://www.servicenow.com/docs/access?context=bp-what-is-domain-separation&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Accessible from

</td><td>

Specifies if the trigger data is accessible from all application scopes or one application only.

</td></tr><tr><td>

Protection

</td><td>

Option to make the trigger read-only.

</td></tr><tr><td>

Category

</td><td>

Category under which the trigger will be displayed.

</td></tr><tr><td>

Trigger annotation

</td><td>

Annotation for your trigger that the user can see before they select it.

</td></tr></tbody>
</table>After you specify the trigger properties and build the trigger, configure and publish the trigger to use in flows.

-   **[Create a saved record trigger](../task/create-saved-trigger.md)**  
Save a set of trigger definitions as a reusable trigger. Enable flow authors to select the saved trigger from some or all application flows. Specify whether flow authors can see the trigger details or add conditions to the trigger.
-   **[Create a saved scheduled trigger](../task/create-scheduled-trigger.md)**  
Create a scheduled trigger that starts your flow when you need. Schedule the trigger to start your flow on a specific date and time or repeatedly at scheduled intervals. Reuse the trigger in flows that need to run on the same schedule.
-   **[Create a saved external trigger](../task/create-saved-external-trigger.md)**  
Save a set of trigger definitions as a reusable trigger that responds to external events through webhooks. When an event occurs in the configured third-party application that meets the specified conditions, the trigger is activated.
-   **[Edit a saved trigger](../task/edit-saved-trigger.md)**  
Edit a saved trigger in Workflow Studio to update the trigger definitions or other options according to your business needs.
-   **[Detach a saved trigger from a flow](../task/detach-saved-trigger.md)**  
View a list of flows that are associated with a saved trigger, and detach it from any of the flows. Detach a saved trigger before you specify different start conditions for your flow or before you delete the trigger.
-   **[Delete a saved trigger](../task/delete-saved-trigger.md)**  
Delete a saved trigger that you no longer need.

**Parent Topic:**[Using Workflow Studio](../../workflow-studio/reference/building-workflow-studio-components.md)

