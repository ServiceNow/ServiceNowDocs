---
title: Conversational actions
description: Run a Workflow Studio action from a Now Assist conversation. Create and configure the conversational skill from Workflow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/build-workflows/workflow-studio/conversational-actions.html
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Exploring actions, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Conversational actions

Run a Workflow Studio action from a Now Assist conversation. Create and configure the conversational skill from Workflow Studio.

Workflow Studio offers a selection of preconfigured actions that are available to run from Conversational Interfaces.

## Activating the subflows and actions skill

To activate the subflows and actions skill, see [Turn on the subflows and actions skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/turn-on-the-subflows-and-actions-skill.md).

## User role access

Give personnel an appropriate role to access conversational subflows. See [User roles for conversational subflows and actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/user-roles-for-conversational-subflows-and-actions.md).

## Making an action conversation compatible

To make an action conversation compatible, you must perform the following steps.

-   Turn on the subflows and actions skill. See [Turn on the subflows and actions skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/turn-on-the-subflows-and-actions-skill.md).
-   Give personnel an appropriate role to access conversational actions. See [User roles for conversational subflows and actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/user-roles-for-conversational-subflows-and-actions.md).
-   Choose action inputs that are compatible with Conversational Interfaces. See [Supported input data types for conversational subflows and actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/supported-input-data-types-for-conversational-subflows-and-actions.md).
-   Add tooltip hint text to all action inputs.
-   Publish the action.

## Conversational settings

You can use the conversational settings menu to manage conversational subflows and actions from Workflow Studio. Options include:

-   Toggle off or on the option to make an action or subflow conversational.
-   See the subflow or action skill name.
-   Select one or more assistants that can discover the action or subflow skill.
-   Select one or more roles users must have to access the action or subflow skill.
-   Set the advanced option to make the action or subflow skill discoverable.
-   Set the advanced option to include the action or subflow skill in the list of topics.

\[Omitted image "example-conversational-settings.png"\] Alt text: Conversational settings for the preconfigured action called Create Checklist from Template

When you set these options in Workflow Studio, the system also sets the corresponding options in Virtual Agent Designer.

## Supported conversational subflows and actions input data types

Conversational subflows and actions support a limited number of input data types. To be compatible with conversational interfaces, an action or a subflow must only include inputs that use supported data types.

|ServiceNow AI Platform data type name|Workflow Studio data type label|
|-------------------------------------|-------------------------------|
|array.string|Array of Strings|
|boolean|True/False|
|calendar|Calendar Date/Time|
|choice|Choice|
|date|Date|
|datetime|Date/Time|
|document\_id|Document ID|
|date\_time|Date/Time|
|due\_date|Due Date|
|email|Email|
|glide\_date|Date|
|glide\_time|Time|
|glide\_date\_time|Date/Time|
|GUID|Sys ID \(GUID\)|
|html|HTML|
|integer|Integer|
|long|Long|
|longint|Long Integer String|
|reference|Reference|
|schedule\_date\_time|Schedule Date/Time|
|string|String|
|string\_full\_utf8|String \(Full UTF-8\)|
|table\_name|Table Name|

-   **[Available conversational actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/available-conversational-actions.md)**  
Workflow Studio provides a set of actions that are preconfigured to be compatible with and callable by conversational interfaces such as Now Assist.
-   **[Check for conversational compatible actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/check-for-conversational-compatible-actions.md)**  
Run a compatibility check on new or all actions to determine if they are conversational compatible. Review the inputs of an action to determine if their data types are compatible.
-   **[Configure action conversational settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/configure-action-conversation-settings.md)**  
Configure conversation settings to make an action available to conversational interfaces.

**Parent Topic:**[Exploring actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/exploring-actions.md)

**Related topics**  


[Conversational subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/conversational-subflows.md)

