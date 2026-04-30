---
title: Building actions
description: Workflow Studio is the default ServiceNow AI Platform process automation builder used to create actions. Workflow Studio replaces the Workflow Editor.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using Workflow Studio, Workflow Studio, Build workflows]
---

# Building actions

Workflow Studio is the default ServiceNow AI Platform process automation builder used to create actions. Workflow Studio replaces the Workflow Editor.

## Core actions

ServiceNow Core actions that come with your instance cannot be viewed or edited from the Workflow Studio interface. Some applications include spokes which include application-specific actions. Spoke actions are typically read-only but can be copied and customized.

## Custom actions

Unlike core actions where flow designers must manually configure flow logic, custom actions always use the same configuration when added to a flow. If your flow designers often use an action with the same configuration, you might create a reusable action.

## Action design environment

![Action Designer interface](../images/action-designer.png)

Create and edit actions by defining inputs and adding action steps. Test actions to verify if they complete successfully and review the runtime values they generate. Copy actions to use existing actions as templates. Publish actions to activate them, which makes them available to activated flows and to preserve their current action steps, variables, and sequence as a snapshot separate from further configuration changes.

## More Actions

Click the More actions icon \(![More actions icon](../images/MoreActionsIcon.png)\) to access additional options for the action.

-   **Copy action**

    Create a copy of the open action in an application you specify.

-   **Configurations**

    Enable or disable the **Show inline script toggle** option.

-   **Code Snippet**

    Generate a code snippet for the action.

-   **Manage security**

    Enable or disable the **Callable by Client API** option.

-   **Manage natural language title**

    Create or edit an action title with styled or dynamic text. For more information, see [Manage natural language titles](../task/manage-natural-language-title.md).


## Testing actions

After adding inputs and action steps, users with the action\_designer or admin role can test an action. To test an action, provide the required inputs. Action designers should always test actions on non-production instances containing relevant demonstration data because testing an action can make significant changes to records on your instance.

## Roles

To create custom actions, you must have the action\_designer or admin role.

## Action status

Every action has an Action Status data pill in the Data pane. This object data pill contains the current runtime details about the action. The Action Status object consists of a code and message.

-   **Action Status &gt; Code**

    Integer data pill containing the code returned by the first matching error condition or the last step run. You can return your own code when you create a custom error condition. See [Action error evaluation](action-error-evaluation.md).

-   **Action Status &gt; Message**

    String data pill containing the message produced by a matching error condition or the last step run. You can return your own message when you create a custom error condition. See [Action error evaluation](action-error-evaluation.md).


-   **[Getting started with actions](../task/getting-started-action.md)**  
Transform the Ask for Approval action into a reusable action that always requires manager approval.
-   **[Create an action in Workflow Studio](../task/create-action.md)**  
Create a reusable component to automate one or more steps of a process.
-   **[Configure action conversational settings](../task/configure-action-conversation-settings.md)**  
Configure conversation settings to make an action available to conversational interfaces.
-   **[Complex data](complex-data.md)**  
Use a graphical interface to work with collections of complex structured data. Help design users understand the organization of structured data, and add, remove, or configure its individual elements.

**Parent Topic:**[Using Workflow Studio](../../workflow-studio/reference/building-workflow-studio-components.md)

