---
title: Conversational subflows
description: Run a Workflow Studio subflow from a Now Assist conversation. Create and configure the conversational skill from Workflow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/build-workflows/workflow-studio/conversational-subflows.html
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-02-13"
reading_time_minutes: 3
breadcrumb: [Exploring subflows, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Conversational subflows

Run a Workflow Studio subflow from a Now Assist conversation. Create and configure the conversational skill from Workflow Studio.

\[Omitted video\] Description: Run an action or subflow from a Now Assist conversation

Workflow Studio offers a selection of preconfigured subflows that are available to run from Conversational Interfaces.

## Activating the subflows and actions skill

To activate the subflows and actions skill, see [Turn on the subflows and actions skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/turn-on-the-subflows-and-actions-skill.md).

## User role access

Give personnel an appropriate role to access conversational subflows. See [User roles for conversational subflows and actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/user-roles-for-conversational-subflows-and-actions.md).

## Making a subflow conversation compatible

To make a subflow conversation compatible, you must perform the following steps.

-   Turn on the subflows and actions skill. See [Turn on the subflows and actions skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/turn-on-the-subflows-and-actions-skill.md).
-   Give personnel an appropriate role to access conversational subflows. See [User roles for conversational subflows and actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/user-roles-for-conversational-subflows-and-actions.md).
-   Choose subflow inputs that are compatible with Conversational Interfaces. See [Supported input data types for conversational subflows and actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/supported-input-data-types-for-conversational-subflows-and-actions.md).
-   Add tooltip hint text to all subflow inputs.
-   Publish the subflow.

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

-   **[Available conversational subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/available-conversational-subflows.md)**  
Workflow Studio provides a set of subflows that are preconfigured to be compatible with and callable by conversational interfaces such as Now Assist.
-   **[Check for conversational compatible subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/check-for-conversational-compatible-subflows.md)**  
Run a compatibility check on new or all subflows to determine if they are conversation compatible. Review the inputs of a subflow to determine if their data types are compatible.
-   **[Configure subflow conversational settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/configure-subflow-conversation-settings.md)**  
Configure conversation settings to make a subflow available to conversational interfaces.

**Parent Topic:**[Exploring subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/exploring-subflows.md)

**Related topics**  


[Conversational actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/build-workflows/workflow-studio/conversational-actions.md)

