---
title: Adjust styles for responsive authoring
description: When creating pages with responsive authoring for different form factors, learn how to change style options to increase the usability of the page at smaller sizes.
locale: en-US
release: yokohama
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Responsive authoring, Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Adjust styles for responsive authoring

When creating pages with responsive authoring for different form factors, learn how to change style options to increase the usability of the page at smaller sizes.

## Before you begin

Role required: ui\_builder\_admin

## About this task

A method of increasing page usability is to tailor components using different styles across breakpoints. There are numerous options for editing styles. In this procedure, edit the margin around the stylized text component and reduce the text size so it uses less space on smaller form factors.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create &gt; Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Create a page from scratch with responsive authoring.

    For more information about how to create a page, see [Create a page in UI Builder](create-page.md).

4.  At the top, check that the desktop responsive authoring icon is selected.

    ![Black arrow pointing to desktop form factor icon at the top of a UI Builder page in editor view.](../image/responsive-author-icon-desktop.png)

5.  On the stage, select **+ Add content**.

6.  On the **Layouts** tab, select **Single column**.

7.  Add the stylized text component.

    1.  Select the **+** icon in the center of the column on the stage.

    2.  On the **Components** tab, find and select the **Stylized text** component.

    3.  In the configuration panel, select **None - Configure the component manually**.

    4.  In the configuration panel, on the **Configure** tab, double-click \(or use the keyboard shortcut\) in the **Text** field to select the default text.

    5.  Replace the default text by entering `Critical Operations Workspace Admin Center`.

        ![Configuration panel for stylized text component with black arrow pointing to text field.](../image/responsive-author-styles1.png)

    6.  Select **Save**.

8.  Add some space around the stylized text component and center it.

    1.  In the content tree, select **Stylized text 1**.

    2.  On the configuration panel, select the **Styles** tab.

    3.  In **Spacing**, select **Margin**.

    4.  Select **Large** in the list.

        ![Configuration panel for stylized text component with black arrow pointing to margin option and large size option.](../image/responsive-author-styles2.png)

    5.  In **Alignment**, select the center icon.

        ![Configuration panel for stylized text component with black arrow pointing to center icon for alignment field.](../image/responsive-author-styles3.png)

    6.  Select **Save**.

    The stage updates automatically, showing the additional white space around the stylized text component and centering it.

9.  Select the tablet form factor icon.

    ![Black arrow pointing to tablet form factor icon at the top of a UI Builder page in editor view.](../image/responsive-author-icon-tablet.png)

    The spacing and heading size of the stylized text component looks good at tablet size.

10. Select the mobile form factor icon.

    ![Black arrow pointing to mobile form factor icon at the top of a UI Builder page in editor view.](../image/responsive-author-icon-mobile.png)

    The stylized text component uses a great deal of vertical space at the smaller size.

    ![Page displayed at the mobile form factor with large margin around stylized text component and H1 heading size.](../image/responsive-author-styles4.png)

11. Remove the extra margin space and make the heading smaller just for the mobile form factor.

    1.  In the content tree, select **Stylized text 1**.

    2.  On the configuration panel, select the **Styles** tab.

    3.  In **Spacing**, select **Margin**.

    4.  Select **0** in the list.

    5.  Select the **Configure** tab.

    6.  In **HTML tab**, select **H3**.

    7.  Select **Save**.

    The stage updates automatically showing that the stylized text component uses less space.

    ![Page displayed at the mobile form factor with zero margin around stylized text component and reduced heading size.](../image/responsive-author-styles5.png)

12. Select the tablet and the desktop form factor icons at the top to confirm that no changes were made to the larger form factors.


**Parent Topic:**[Responsive authoring](../concept/responsive-authoring.md)

