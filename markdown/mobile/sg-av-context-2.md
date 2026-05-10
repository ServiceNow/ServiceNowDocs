---
title: Create UI parameters for your Virtual Agent link
description: Create UI parameters to pass information from your record into Virtual Agent so that your users get the information they need for their issues.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure a contextual link to Virtual Agent, Action functions, Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create UI parameters for your Virtual Agent link

Create UI parameters to pass information from your record into Virtual Agent so that your users get the information they need for their issues.

## Before you begin

Role required: admin

## Procedure

1.  From the Mobile App Builder home screen, select the **Functions** category and then select **New**.

2.  In the **Action item** area of the form, select **New**.

3.  In the **Data parameters** area of the form, select **New**.

4.  In the **Name** field, enter the name of the data parameter.

    You can have multiple parameters with the same name, so choose a name that you can distinguish easily.

5.  From the **Type** list, select the type of the parameter.

    -   **Integer:** Uses a numbers-only keypad for input.
    -   **String:** Uses a full keyboard for input. Use the String type for list parameters, such as priority or state, or for reference fields, such as **Assigned to** or **Caller**.
    -   **Decimal:** Uses a numbers-only keypad for input.
    -   **Boolean:** Uses a true or false selection option.

        **Note:** Making a Boolean mandatory has no effect. Boolean fields are always considered to have a value. A selected check box has a value of true and an unselected check box has a value of false. Either of these values satisfies the requirement of a mandatory field.

    -   **DateTime:** Uses a calendar with an exact time selector.
    -   **Date:** Uses a calendar.
6.  Select **Save**.

7.  Navigate back to the action item using the menu.

    Confirm that the Data Parameter you created in Step 3 through 6 appears in the **Data parameters** section of the Action Item form.

8.  Select **Save**.

9.  Repeat steps 3 through 6 to create additional UI parameters for any other information that you want to pass to Virtual Agent.

    You can direct your mobile users to a specific Virtual Agent topic by creating a `search_text` UI parameter. You can create this parameter using the preceding steps, with the following changes:

    |Field|Description|
    |-----|-----------|
    |Name|Name of the UI parameter. For this example, enter `search_text`.|
    |Input Type|Location where the user will input data for the parameter. For this example, select **Constant**.|
    |Constant Value|Value that matches a keyword from one of your Virtual Agent conversations. When your users tap the chat button, they are directed to the matching topic.|


## What to do next

The UI parameters that you created are available to your Virtual Agent topics within the `vaContext` object. You can access these parameters in Virtual Agent Designer by entering `vaContext.` followed by the name of your UI parameter. For example, you can access the `incident_caller` UI parameter by entering `vaContext.incident_caller`. For more details on using context variables in Virtual Agent, see [Virtual Agent scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/virtual-agent-scripts.md).

**Parent Topic:**[Configure a contextual link to Virtual Agent](sg-av-context-action.md)

