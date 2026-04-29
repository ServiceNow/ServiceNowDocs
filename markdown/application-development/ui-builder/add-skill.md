---
title: Add Now Assist skills to your page
description: Add skills to enhance your UI Builder page with Now Assist's generative AI capabilities.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, Now Assist Skill Kit, UI Builder]
breadcrumb: [Dynamically expose data in UI Builder pages \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add Now Assist skills to your page

Add skills to enhance your UI Builder page with Now Assist's generative AI capabilities.

## Before you begin

Role required: ui\_builder\_admin

**Note:** Skills must be enabled and activated before they can be added to a page. For more information, see:

-   [Configure skill deployment settings](https://www.servicenow.com/docs/access?context=configure-skill-settings&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US): Enable the skill to make it available for selection
-   [Activate a skill](https://www.servicenow.com/docs/access?context=activate-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US): Activate the skill so it can be selected

## About this task

You can add Now Assist skills to your page, component, or controller. To trigger a skill, you must create an event to execute the skill while passing the appropriate payload. After configuring the required inputs, the skill is ready to use.

In this example, you will:

1.  Add a skill to the page
2.  Add an input component to capture user text
3.  Configure an event for the input component to pass the entered text to the skill and execute it
4.  Add a text component to show the skill's output

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Create or open a page.

4.  Hover over **Now Assist skills** in the **Data and scripts** section and select the **+** to the right.

5.  Select a skill and select **Add**.

    The following skills are available by default:

    -   **Generate Content**
    -   **Sentiment Analysis**
    -   **Summarize**
    For this example, select **Generate Content**.

    **Tip:** Select **Hide inactive** to remove inactive skills from view.

    ![UI Builder editor with the Select a Now Assist skill dialog open.](../image/add-skill-select.png)

    **Note:** Skills that are enabled in Now Assist Skill Kit but not activated in Now Assist Admin appear in the list, but aren't selectable. For more information, see [Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) and [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

6.  Select the **X** in the upper right to close the **Edit Generate Content** dialog.

7.  Select **+ Add content** in the content tree and add a component from the toolbox.

    In this example, add an **Input** component.

8.  Add the **Execute** event handler to the component that you added in the previous step.

    1.  Select the **Events** tab in the configuration panel.

    2.  Select **Add handler** under **Text entered**.

    3.  Select **Execute** under **Generate Content \(1\)** and select **Continue**.

    4.  Hover over **topic** and select the bind data icon ![](../image/uib-dynamic-data-binding-button.png) to configure the input for the skill.

    5.  Double-click the **fieldValue** pill to select it as the input source and select **Apply**.

        The **fieldValue** property captures what the user types in the input field. By using this property as the input to the skill, you set the skill to trigger whenever the user enters text.

        ![UI Builder editor with the Bind data to topic dialog open, showing the fieldValue output selected and added to the upper section.](../image/add-skill-input.png)

    6.  Select **Add**.

9.  Add and configure a second component to display the output for the skill.

    1.  In the content tree, hover over **Input 1**, select the **Configure** \(three vertical dots\) icon, then select **Add after**.

    2.  Add a **Stylized text** component.

    3.  Select **Cancel** to close the preset window.

    4.  Change the **HTML tag** property to **Paragraph** \(for better readability in this example\).

    5.  Hover over the **Text** field in the configuration panel and select the bind data icon ![](../image/uib-dynamic-data-binding-button.png).

    6.  Select **Data resource** on the left.

    7.  Navigate through the pills by selecting **Generate Content**, then **result**, then double-clicking **response** to complete the selection.

    8.  Select **Apply**.

    ![UI Builder editor with the Bind data to Text dialog open, showing the Data resource > Generate Content > result > response output added to the upper section.](../image/add-skill-response.png)

10. Select **Save**.

11. Select **Preview** to test the skill.

    ![UI Builder page preview showing a functional input component using the Generate Content skill.](../image/add-skill-result.png)


## Result

When you view the page and type in the input field, your text input triggers the **Generate Content** skill to execute and return content on the topic in the input field.

**Parent Topic:**[Dynamically expose data in UI Builder pages \(advanced feature\)](../concept/data-resources.md)

