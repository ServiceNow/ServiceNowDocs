---
title: Conversational actions
description: Run a Workflow Studio action from a Now Assist conversation. Create and configure the conversational skill from Workflow Studio.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2024-11-18"
reading_time_minutes: 3
breadcrumb: [Exploring actions, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Conversational actions

Run a Workflow Studio action from a Now Assist conversation. Create and configure the conversational skill from Workflow Studio.

Workflow Studio offers a selection of preconfigured actions that are available to run from Conversational Interfaces.

## Conversational requirements

Currently, you can't make an action conversational. You can only modify the conversational settings of preconfigured conversational actions. When editing a preconfigured conversational action, you must follow these guidelines to keep the action conversational.

-   All action inputs are compatible with Conversational Interfaces.
-   All action inputs have tooltip text.
-   The action is active and published.
-   You have an appropriate role to access conversational actions.
-   You activate the subflows and actions skill.

## Activating the subflows and actions skill

To activate the subflows and actions skill, see [Turn on the subflows and actions skill](https://www.servicenow.com/docs/access?context=turn-on-the-subflows-and-actions-skill&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## User role access

Personnel with the following user roles can access conversational actions.

|Role|Description|Contains roles|Groups with this role|Special considerations|
|----|-----------|--------------|---------------------|----------------------|
|Virtual Agent administrator \[virtual\_agent\_admin\]|Provides read and write access to all Virtual Agent tables, conversational experiences, and Now Assist admin operations|action\_designer,flow\_designer|None|Avoid granting an admin role when more specialized roles are available.|
|Workflow Conversational Admin \[sn\_conv\_fa.conv\_fa\_admin\]|Provides read access to flows, subflows, and actions. Provides read and write access to conversational experience settings.|sn\_conv\_fa.conv\_fa\_designer, fd\_read\_actions, fd\_read\_flows|None|Avoid granting an admin role when more specialized roles are available.|
|Flow/Action Designer Conversational Workflow \[sn\_conv\_fa.conv\_fa\_designer\]|Provides read and write access to conversational experience settings.|None|None|This is a specialized role with limited access.|
|Action Designer \[action\_designer\]|Provides read and write access to Workflow Studio actions.|sn\_conv\_fa.conv\_fa\_designer|None|This is a specialized role with limited access.|
|Flow Designer \[flow\_designer\]|Provides read and write access to Workflow Studio flows and subflows.|sn\_conv\_fa.conv\_fa\_designer|None|This is a specialized role with limited access.|

## Conversational settings

You can use the conversational settings menu to manage conversational subflows and actions from Workflow Studio. Options include:

-   Toggle off or on the option to make an action or subflow conversational.
-   See the subflow or action skill name.
-   Select one or more assistants that can discover the action or subflow skill.
-   Select one or more roles users must have to access the action or subflow skill.
-   Set the advanced option to make the action or subflow skill discoverable.
-   Set the advanced option to include the action or subflow skill in the list of topics.

![Conversational settings for the preconfigured action called Create Checklist from Template](../images/example-conversational-settings.png "Example conversational settings")

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

-   **[Available conversational actions](../reference/available-conversational-actions.md)**  
Workflow Studio provides a set of actions that are preconfigured to be compatible with and callable by conversational interfaces such as Now Assist.

**Parent Topic:**[Exploring actions](../../workflow-studio/concept/exploring-actions.md)

