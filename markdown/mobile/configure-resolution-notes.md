---
title: Configure mobile resolution notes generation
description: Generate the resolution notes that summarize work orders for mobile.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Now Assist for Mobile, Now Assist for Mobile, Mobile Platform]
---

# Configure mobile resolution notes generation

Generate the resolution notes that summarize work orders for mobile.

## Before you begin

Role required: admin

Make sure that Now Assist is enabled in the instance. For more information, see [Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select the **Screens** category, and then choose the input form screen you wish to add resolution notes generation to, or select **New**.

    **Note:** The input form screen must have at least one **String** type input as this is where the summary text will be generated.

4.  [Create a parameter action](../task/param-screen-config-actions.md).

5.  [Create a mobile UI rule](../task/create-mobile-ui-rule.md) with the **onUserAction** trigger type.

    This action is what will show up on the keyboard when a user clicks into an input field.

    **Note:** Parameter actions will only support triggering record summarization and will only appear when the input field is empty.

6.  [Create a mobile UI rule action](../task/create-mobile-ui-rule-action.md) with the **Record Summarization** operation type.

7.  Add a delete action using the **ShowDeleteAll** input attribute.

    For more information, see [Input form screen attributes for inputs](../reference/parameter-screen-var-attr.md).

8.  Select **Save**.


**Parent Topic:**[Configuring Now Assist for Mobile](configuring-now-assist-mobile.md)

