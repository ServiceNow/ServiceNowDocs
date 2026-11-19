---
title: Adjust layout for responsive authoring
description: When creating pages with responsive authoring for different form factors, learn how to adjust the layout to improve the look and feel of the page at smaller sizes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/ui-builder/responsive-authoring-adjust-layout.html
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Responsive authoring, Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Adjust layout for responsive authoring

When creating pages with responsive authoring for different form factors, learn how to adjust the layout to improve the look and feel of the page at smaller sizes.

## Before you begin

Role required: ui\_builder\_admin

## About this task

A method of increasing page usability is to tailor components by adjusting the layout across breakpoints. There are numerous options for adjusting the layout. In this procedure, adjust the layout of the tabs component for the mobile form factor.

Most column layout options on the property pane can be edited for different form factors. However, the following options have global values across form factors:

-   Number of columns
-   **Stack columns below \(pixels\)** option
-   All options under **Accessibility**

\[Omitted image "responsive-author-column-layout.png"\] Alt text: Column layout properties pane with black arrows pointing to the options that cannot be set by form factor.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create &gt; Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Create a page from scratch with responsive authoring.

    For more information about how to create a page, see [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/create-page.md).

4.  At the top, check that the desktop form factor icon is selected.

    \[Omitted image "responsive-author-icon-desktop.png"\] Alt text: Black arrow pointing to desktop form factor icon at the top of a UI Builder page in editor view.

5.  On the stage, select **+ Add content**.

6.  On the **Layouts** tab, select **Single column**.

7.  Add the tabs component.

    1.  Select the **+** icon in the center of the column on the stage.

    2.  On the **Components** tab, find and select the **Tabs** component.

    3.  Select **Save**.

8.  In the configuration panel, on the **Configure** tab, edit the name of the first tab by selecting the edit icon.

    \[Omitted image "responsive-author-layout1.png"\] Alt text: Configure tab with black arrow pointing to tab edit icon.

9.  In **Tab label**, enter `Tab 1`.

10. In **Tab ID**, enter `tab_1`

11. Select **Save**.

12. Add a second tab.

    1.  On the **Configure** tab, select **+ Add** next to **Tabs**.

    2.  Select **Start from an empty container** and then select **Next**.

    3.  In **Tab label**, enter `Tab 2`.

    4.  Check that **Tab ID** has been automatically filled in with **tab\_2**.

        \[Omitted image "responsive-author-layout2.png"\] Alt text: Configuration panel with configure tab displayed and black arrow pointing to the label field.

    5.  Select **Create**.

13. Add a third tab by repeating step 12 and in 12c name the tab `Tab 3`.

14. Check that your content tree and page are accurate.

15. Select the tablet form factor icon.

    \[Omitted image "responsive-author-icon-tablet.png"\] Alt text: Black arrow pointing to tablet form factor icon at the top of a UI Builder page in editor view.

    The spacing and position of the tabs looks good at tablet width.

16. Select the mobile form factor icon.

    \[Omitted image "responsive-author-icon-mobile.png"\] Alt text: Black arrow pointing to mobile form factor icon at the top of a UI Builder page in editor view.

    The tabs take more space at the smaller size.

17. Change the layout of the tabs just for the mobile size.

    1.  In the content tree, select **Column 1** under **Column layout 1**.

    2.  On the configuration panel, in **Direction**, select the row icon.

        \[Omitted image "responsive-author-layout7.png"\] Alt text: Configuration panel for column 1 with black arrow pointing to row icon for direction option.

    3.  Select **Save**.

    The stage updates automatically showing that tab 1 is visible and that there's a new dropdown menu.

18. Select **Preview**.

19. Select **More**.

    The other two tabs are available.

20. Select the desktop and tablet form factor icons to see that the More drop-down doesn't appear.

21. Select the **X** to close the **Preview** overlay.


**Parent Topic:**[Responsive authoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/responsive-authoring.md)

