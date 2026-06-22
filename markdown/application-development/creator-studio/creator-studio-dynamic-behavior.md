---
title: Make a form change based on responses in Creator Studio
description: Make a form update based on how users answer a question using dynamic behavior. For example, if a user says they want a T-shirt for an event they're attending, you can make a T-shirt size field required.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/creator-studio/creator-studio-dynamic-behavior.html
release: xanadu
product: Creator Studio
classification: creator-studio
topic_type: task
last_updated: "2024-09-26"
reading_time_minutes: 4
breadcrumb: [Working with forms in Creator Studio, Building apps with Creator Studio, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Make a form change based on responses in Creator Studio

Make a form update based on how users answer a question using dynamic behavior. For example, if a user says they want a T-shirt for an event they're attending, you can make a **T-shirt size** field required.

## Before you begin

You must name the form before you can add [dynamic behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-glossary.md) to it.

To add dynamic behavior to a form, you must be given permission to work on the app.

## Procedure

1.  Go to **All** &gt; **App Engine** &gt; **Creator Studio** to see all the apps on the Creator Studio home page.

2.  Open the application that contains the form you want to add dynamic behavior to.

3.  Select to **Preview** how different forms appear in various experiences, or select the **View** or **Edit** button to view or edit the application experience.

    Select different previewing options if you want to make sure that you've selected the correct application and see how it will appear in the following formats:

    -   **Portal** \(see a preview of how it'll appear on a desktop website\)
    -   **Now Mobile** \(see a preview of how it'll appear on a mobile phone or device\)
    -   **Virtual agent** \(see a representation of how it'll appear on a chatbot interface\)

        **Note:** Your organization should have the correct plugins installed to see how the form will appear in Virtual Agent. If you're interested, ask your admin and see [Catalog builder preview topic conversation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/servicenow-platform/service-catalog/catalog-builder-preview-topic.md) for more information on previewing forms and their catalog items in Virtual Agent.

    The **View** button displays forms that have been published and doesn't explicitly create a new draft form for development. The **Edit** button takes you to a development form, for example, a new draft version of a form that's already been published.

    \[Omitted image "crs-portal-preview.png"\] Alt text: Preview how your app will look

    You can also check out a representation of how the form submissions workspace will appear by selecting the **Submissions** preview, as well as the records your app generates for it \(by selecting the **Record** preview\).

4.  Check that you're editing the correct form in your app by selecting it from the **Request forms** tab.

    \[Omitted image "cs-request-forms-tab.png"\] Alt text: Selection from the Request forms tab

5.  Select the question that should be affected by how users answer one or more previous questions.

    For example, select the **T-shirt size** field to make it required if a user answers `Yes` to the **Do you want a T-shirt?** question.

6.  Select the **Behaviors** tab of the settings panel.

    \[Omitted image "crs-add-behavior-btn.png"\] Alt text: Add behavior button on the Question details panel

7.  Define the conditions that will make the form change in the Conditions section.

    1.  Select **Questions** in the **Field** field to specify that you're choosing questions from the form.

        The name of the form automatically appears in the **Item** field.

    2.  Choose the question whose answer triggers the dynamic behavior in the **Question** field.

        For example, select the **Do you want a T-shirt?** question.

    3.  Select the condition **Operator** to determine the status of the selected field that will trigger the dynamic behavior.

        For example, you could select **Is** as the operator for the **Do you want a T-shirt?** field.

        For more information, see [Condition builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-user-interface/configure-user-experiences/c_ConditionBuilder.md).

    4.  Enter or select the value for the user's response to the trigger question.

        For example, the value could be **Yes** if they want a T-shirt.

    5.  Specify another field and value to create a more complex set of triggering conditions by selecting the **or** button or the **and** button.

    6.  Build another set of conditions by selecting the **Add condition set** button and repeating steps a-e.

    \[Omitted image "crs-dynamic-panel-fields.png"\] Alt text: Dynamic behavior settings for T-shirt question

8.  Define how the form changes in response to the conditions that you defined in the Action section of the **Behaviors** panel.

    1.  Choose what the form does when the triggering conditions are met in the **Select an option** field.

        Depending on the conditions you created, the following actions may be available:

        -   **Make it visible**
        -   **Mark as required**
        -   **Make read-only**
        -   **Display a message**
        -   **Choose a value**
        You can add multiple actions, but you can add only one of each type of action for each set of dynamic behavior.

        \[Omitted image "crs-dynamic-actions.png"\] Alt text: Choose an action for the behavior

    2.  Choose what happens for each action that you select.

        For example, if you chose to **Display a message**, you can make it an **Info**, **Warning**, or **Error** message, and then you must enter the message that appears.

9.  Select **Save**.


## Result

The question appears with a dynamic icon \(\[Omitted image "crs-dynamic-indicator.png"\] Alt text:\) to indicate that it has dynamic behavior.

The dynamic behavior appears in a card on the **Behavior** tab of the settings panel. You can select the card at any time to view or edit its details, or select the **Add behavior** button to add another dynamic behavior.

**Parent Topic:**[Working with forms in Creator Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/creator-studio/creator-studio-work-with-forms.md)

