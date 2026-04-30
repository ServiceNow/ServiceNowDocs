---
title: Adjusting component visibility in responsive authoring
description: When creating pages with responsive authoring for different form factors, learn how to show or hide components by completing steps to hide an image at mobile size.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Responsive authoring, Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Adjusting component visibility in responsive authoring

When creating pages with responsive authoring for different form factors, learn how to show or hide components by completing steps to hide an image at mobile size.

## Before you begin

Role required: ui\_builder\_admin

## About this task

A method of increasing page usability is to hide components or show a different component across breakpoints. There are countless ways to use component visibility, but a few examples include:

-   Use multiple button components horizontally across the top of a page for desktop and tablet size, but at mobile size, hide the buttons and show the dropdown component.
-   Use a smaller button size for mobile size, but check that the buttons are large enough for users to press with a thumb. Consider changing the placement of buttons for mobile as well.
-   Use images in desktop and tablet pages, but hide images, especially larger ones, in mobile.

In this procedure, show buttons across the top for the desktop and tablet form factors, but hide the buttons and use the dropdown component for mobile.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create &gt; Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Create a page from scratch with responsive authoring.

    For more information about how to create a page, see [Create a page in UI Builder](create-page.md).

4.  At the top, check that the desktop form factor icon is selected.

    ![Black arrow pointing to desktop form factor icon at the top of a UI Builder page in editor view.](../image/responsive-author-icon-desktop.png)

5.  Add a column layout by selecting **+ Add content** under **Body** in the content tree.

6.  On the **Layouts** tab, select **Single column**.

7.  Add the first button component.

    1.  Select the **+** icon in the center of the new column on the stage.

    2.  On the **Components** tab, find and select the **Button** component.

    3.  In the configuration panel, select **None - Configure the component manually**.

    4.  In the configuration panel, on the **Configure** tab, replace the default text in the **Label** field by entering `Tasks`.

        ![Button component configure tab with black arrow pointing to label field.](../image/responsive-author-vis3.png)

    5.  Select **Save**.

8.  Add two more buttons by repeating step 7 twice and in 7d name the buttons `Incidents` and `Changes`.

    **Note:** To add the buttons, point to **Button 1** in the content tree, select the menu icon, and then select **Add after**.

9.  Check that the content tree and page are accurate.

10. Add some space around each button.

    1.  In the content tree, select **Button 1**.

    2.  In the configuration panel, select the **Styles** tab.

    3.  In **Spacing**, select **Margin**.

    4.  In the menu, select **XS** \(extra small\).

        ![Configuration panel with black arrows pointing to margin option and extra small size option.](../image/responsive-author-vis6.png)

    5.  Select **Save**.

11. Add space around the other two buttons by repeating step 10 for each.

12. Change the buttons from the vertical direction to the horizontal direction.

    1.  Select **Column 1** in the content tree.

    2.  On the configuration panel, in **Direction**, select the row icon.

        ![Configuration panel for column 1 with black arrow pointing to row icon for direction option.](../image/responsive-author-layout7.png)

    3.  Select **Save**.

    The page looks good at desktop width.

13. Select the tablet form factor icon.

    ![Black arrow pointing to tablet form factor icon at the top of a UI Builder page in editor view.](../image/responsive-author-icon-tablet.png)

    The spacing and position of the buttons also looks good at tablet width.

14. Select the mobile responsive authoring icon.

    ![Black arrow pointing to mobile form factor icon at the top of a UI Builder page in editor view.](../image/responsive-author-icon-mobile.png)

    The buttons use almost all the horizontal space at the smaller size.

15. Add the dropdown component.

    1.  Select the desktop form factor at the top of the stage.

    2.  Point to **Button 3** in the content tree, select the menu icon, and then select **Add after**.

    3.  On the **Components** tab, find and select the **Dropdown** component.

    4.  In the configuration panel, select **None - Configure the component manually**.

    5.  In the configuration panel, on the **Configure** tab, remove the default text in **Placeholder text** and select **menu-outline** in **Icon**.

        ![Dropdown component configure options.](../image/responsive-author-layout11.png)

    6.  Select **Save**.

16. Hide the dropdown component at the desktop and tablet form factors.

    1.  In the content tree, select **Dropdown 1**.

    2.  In the configuration panel, on the **Configure** tab, select **Component visibility** to show the options.

    3.  Select **Hide component**.

    4.  Select **Save**.

17. At the mobile form factor, hide the button components.

    1.  Select the mobile form factor icon at the top of the stage.

    2.  In the content tree, select **Button 1**.

    3.  In the configuration panel, on the **Configure** tab, select **Hide component**.

    4.  Repeat steps b-c for **Button 2** and **Button 3**.

    5.  Select **Save**.

    Two locations show that the button components are hidden at mobile size. First, in the configuration panel, next to the **Hide component** option, select the mobile icon. A message is displayed to confirm that the value \(hide component selected\) is for the mobile size.

    ![Configuration panel with configure tab displayed and black arrow pointing to message.](../image/responsive-author-vis-message.png)

    Second, in the content tree, the three button components are displayed with the hidden ![Hidden icon](../image/responsive-author-hidden-icon.png) icon.

18. At the mobile form factor, show the dropdown component.

    1.  In the content tree, select **Dropdown 1**.

    2.  In the configuration panel, on the **Configure** tab, select **Hide component** to clear the field.

    3.  Select **Save**.

19. Select **Preview**.

    The mobile form factor is displayed with the menu icon. If you select the arrow, the default options are displayed \(List item 1, List item 2, and so on\). You would configure the dropdown component to display **Tasks**, **Incidents**, and **Changes** just like the horizontal buttons available at the tablet and desktop form factors.

20. Select the desktop and tablet form factor icons at the top.

    The desktop and tablet form factors only show the horizontal buttons, not the menu icon.

21. Close the preview overlay by selecting the **X**.


**Parent Topic:**[Responsive authoring](../concept/responsive-authoring.md)

