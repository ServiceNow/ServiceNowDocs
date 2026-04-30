---
title: Using client state parameters in UI Builder
description: Create a simple counter by adding the stylized text component and two buttons to an experience page. Use a client state parameter to implement the functionality so that when the buttons are selected the count increases or decreases.
locale: en-US
release: xanadu
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Client state parameters, Dynamically expose data in UI Builder pages \(advanced feature\), Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Using client state parameters in UI Builder

Create a simple counter by adding the stylized text component and two buttons to an experience page. Use a client state parameter to implement the functionality so that when the buttons are selected the count increases or decreases.

## Before you begin

Role required: ui\_builder\_admin

Three minute video showing how to add a stylized text component and two button iconic components to create a simple counter application.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create &gt; Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  [Create a page in UI Builder](create-page.md) or open a page.

4.  Add a column layout by selecting **+ Add content** in the content tree under **Body**.

5.  On the **Layouts** tab, select **Two columns**.

6.  Add the first component by selecting **+ Add content** in the content tree under **Column 1**.

    ![Content tree with black arrow pointing to plus add component under column one.](../image/counter-app-add-component.png)

    1.  In **Search**, type `sty`.

    2.  Select the **Stylized text** component.

        ![Toolbox with black arrows pointing to search field and the stylized text component.](../image/counter-app-stylized-text-component.png)

    3.  In the configuration panel, select **None - Configure the component manually**.

        ![Configure panel with black arrow pointing to the none option.](../image/counter-app-none-config-manually.png)

7.  Add the second component by selecting **+ Add content** in the content tree under **Column 2**.

    1.  In **Search**, type `button`.

    2.  Select **Button Iconic**.

        ![Toolbox with black arrows pointing to search field and the button component.](../image/counter-app-button-iconic-component.png)

    3.  In the configuration panel, select **None - Configure the component manually**.

    4.  In **Icon**, select **Square Arrow Up Fill**.

        ![Configure panel with black arrows pointing to icon field, search bar, and square arrow up fill icon.](../image/counter-app-button-icon1.png)

8.  Add the third component by pointing to **Button iconic 1** in the content tree, selecting the **Menu** icon, and selecting **Add after**.

    ![Content tree to black arrows pointing to button icon 1 menu icon and the add after option in the pop up menu.](../image/counter-app-add-second-button.png)

    1.  In **Search**, type `button` as you did in the previous step.

    2.  Select **Button Iconic** as you did in the previous step.

    3.  In the configuration panel, select **None - Configure the component manually** as you did in the previous step.

    4.  In **Icon**, select a different icon this time, the one named **Square Arrow Down Fill**.

        ![Configure panel with black arrows pointing to icon field, search bar, and square arrow down fill icon.](../image/counter-app-button-icon2.png)

9.  Select **Save**.

    The stylized text component and the two button iconic components are saved and appear on the stage.

    ![The three components appear on the stage.](../image/counter-app-all-components-on-stage.png)

10. Add a client state parameter by going to **Data and scripts**, pointing to **Client state parameters**, and selecting the **Add new \(plus\)** icon.

    1.  Change the **Name** by entering `count`.

    2.  Change the **Type** to **Number**.

    3.  Set the **Initial value** by entering the number `0`.

    4.  Select the **X** to close the window.

        ![Client state parameter shown with name, type, and initial value fields underlined and black arrow pointing to close icon.](../image/counter-app-client-state-param.png)

11. Bind the stylized text component to the client state parameter.

    1.  Select the stylized text component on the stage.

    2.  In the configuration panel, point to the **Text** field and select the **Bind data or use scripts** icon.

        ![Configure panel with black arrows pointing to the text field and the bind data icon.](../image/counter-app-stylized-text-bind.png)

    3.  On the **Data types** tab, select **Client states**.

    4.  Double-click on the **count** pill.

    5.  Select **Apply**.

        ![Bind data pop up window with black arrows pointing to data types tab, client states option, count pill, and apply button.](../image/counter-app-stylized-text-bind2.png)

        The **Text** field changes to **count**.

12. Now configure the buttons to increase or decrease the number.

    1.  Select the top button on the stage.

    2.  In the configuration panel, select the **Events** tab.

    3.  Select **+ Add event handler**.

    4.  Under **Page-level event handlers**, select **Update client state parameter**.

    5.  In **Client State Parameter Name**, select **count**.

    6.  Point to the **New Value** field and select the **Bind data or use scripts** icon.

        ![Event handler pop up window with black arrows pointing to update client state parameter option, the client state parameter name field, and the new value bind data icon.](../image/counter-app-button1-configure1.png)

    7.  On the **Data types** tab, select **Client states**.

    8.  Double-click on the **count** pill.

    9.  Select the **Formulas** tab.

    10. In the list, select **Math**.

    11. Double-click on the **ADD** pill.

    12. In the **right** pill at the top, remove the text and enter `1`.

        ![Bind data to new value pop up window with black arrow pointing to second pill at top.](../image/counter-app-button1-configure2.png)

    13. Select **Apply**.

    14. Select **Add**.

13. Now configure the second button by following the same process that you used for the first button, but select the SUB pill instead of the ADD pill.

    1.  Select the bottom button on the stage.

    2.  In the configuration panel, select the **Events** tab.

    3.  Select **+ Add event handler**.

    4.  Under **Page-level event handlers**, select **Update client state parameter**.

    5.  In **Client State Parameter Name**, select **count**.

    6.  Point to the **New Value** field and select the **Bind data or use scripts** icon.

    7.  On the **Data types** tab, select **Client states**.

    8.  Double-click on the **count** pill.

    9.  Select the **Formulas** tab.

    10. In the list, select **Math**.

    11. Double-click on the **SUB** pill.

    12. In the **right** pill at the top, remove the text and type `1`.

    13. Select **Apply**.

    14. Select **Add**.

14. Test the counter by selecting **Preview**.

15. Select the up arrow button to increase the count and the down arrow button to decrease the count.

    ![Preview window with black arrows pointing to the up arrow button and the down arrow button.](../image/counter-app-preview.png)


## Result

You added a button component to increase the count by one and another button component to decrease the count by one. You added the stylized text component to show the count as it increased and decreased.

For detailed, technical information about the button component, see [Button Overview &amp; API](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/now-components/now-button/overview).

For detailed, technical information about the stylized text component, see [Stylized Text Overview](https://developer.servicenow.com/dev.do#!/reference/next-experience/washingtondc/now-components/now-stylized-text/overview).

**Parent Topic:**[Client state parameters](../concept/client-state-parameters.md)

