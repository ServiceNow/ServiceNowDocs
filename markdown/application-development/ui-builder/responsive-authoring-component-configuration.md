---
title: Configuring components for responsive authoring
description: When creating pages with responsive authoring for different form factors, learn how adjusting some component configuration options can make pages look and work better at smaller sizes.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Responsive authoring, Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Configuring components for responsive authoring

When creating pages with responsive authoring for different form factors, learn how adjusting some component configuration options can make pages look and work better at smaller sizes.

## Before you begin

Role required: ui\_builder\_admin

## About this task

A method of increasing page usability is to tailor the look and feel of components using different configurations across breakpoints. There are countless ways to use component configuration. In this procedure, edit several configuration options for the List component to make it more suitable for smaller form factors.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create &gt; Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Create a page from scratch with responsive authoring.

    For more information about how to create a page, see [Create a page in UI Builder](create-page.md).

4.  At the top, check that the desktop form factor icon is selected.

    ![Black arrow pointing to desktop form factor icon at the top of a UI Builder page in editor view.](../image/responsive-author-icon-desktop.png)

5.  On the stage, select **+ Add content**.

6.  On the **Layouts** tab, select **Single column**.

7.  Add the list component by selecting the **+** icon in the center of the new column.

8.  On the **Components** tab, find and select the **List** component.

9.  In the configuration panel, select **None - Configure the component manually**.

10. View the page at the desktop form factor.

11. Select the mobile form factor icon.

12. Select **List 1** in the content tree.

13. In the configuration panel, on the **Configure** tab, find the **Number of displayed columns** field and enter `1`.

    Only the **Number** column is displayed. The horizontal scroll bar was removed.

14. In the configuration panel, on the **Configure** tab, scroll down to make the following changes in the **Header** section:

    1.  Change the **Size** to **Small**.

    2.  Select the **Hide last refresh information** option.

    3.  Select the **Hide list actions** option.

        ![Header section of the configuration panel's configure tab.](../image/responsive-author-config2.png)

        As you made each change, the stage updated automatically. The header is a smaller size, the refresh time was removed, and the list actions icon was removed.

    4.  Select **Save**.

15. On the stage, scroll to the bottom of the mobile view.

16. In the configuration panel, on the **Configure** tab, scroll down and make the following changes in the **Pagination** section \(if necessary, select **Pagination** to expand the field\):

    1.  Select the **Hide range** option.

    2.  Select the **Hide row count** option.

    3.  Select the **Hide rows per page selector**.

    4.  Select **Save**.

    The range, row count, and rows per page selector were removed. \(The row count is still available at the top of the mobile screen\).

    In the configuration panel, the options and fields you edited are marked with the mobile cascade icon.

17. Select the mobile cascade icon next to any option or field to confirm that the value is for the mobile form factor.

    ![Configuration panel with configure tab displayed and black arrow pointing to value is specific message.](../image/responsive-author-config3.png)

18. Select the tablet and the desktop form factor icons at the top to confirm that no changes were made to the larger form factors.


**Parent Topic:**[Responsive authoring](../concept/responsive-authoring.md)

