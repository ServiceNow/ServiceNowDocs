---
title: Add a viewport component to your page
description: Add a viewport component to your page and create a subpage to create separate content on the page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/ui-builder/work-with-viewport-components.html
release: zurich
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Extend your UI experience with viewport components, Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add a viewport component to your page

Add a viewport component to your page and create a subpage to create separate content on the page.

## Before you begin

Role required: ui\_builder\_admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Open the editor for the page variant that you want to add the viewport to.

    If you haven't created a page for your experience, follow the steps to [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/create-page.md).

4.  Select **+ Add content** in the content tree.

5.  Select a **Single column** layout.

6.  Next, select the **+** icon in the column to open the toolbox.

7.  Enter `viewport` in the search box.

8.  Select **Viewport**.

    \[Omitted image "viewport-component-add.png"\] Alt text: Viewport component selected in the toolbox.

9.  Select the viewport component in the content tree.

10. Select **+ Add** in the configuration panel.

    \[Omitted image "viewport-component-edit-content.png"\] Alt text: Arrow pointing to the +Add button on the configure tab to add page collections.

11. Select a [page collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/ui-builder-glossary.md) from the list or create a collection by selecting **+ Create collection**.

    For more information on creating your own page collection, see [Create a page collection across multiple UI pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/create-page-collection.md).

    \[Omitted image "page-collection-list.png"\] Alt text: Page collection selection screen with option to create a collection.

12. Select **Add**.

    The page collection displays in the **Page collections** section of the configuration panel. Only one page of the page collection displays in the staging area.

13. Select **Save**.

14. Locate the viewport ID and route.

    You can see the ID and route in the Config panel as shown in the following figure.

    \[Omitted image "viewport-component-id-route.png"\] Alt text: Arrow pointing to the viewport component id on the configure tab.

15. Add a component to your page to open the viewport you just added, such as a button component.

    For more information, see [Add and configure components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/add-components.md).

16. Select the **Events** tab in the configuration panel.

17. Select **+ Add event handler** to view the viewport.

    \[Omitted image "modal-button-event.png"\] Alt text: Arrow pointing to the add event handler option on the configure tab for the button component.

18. From **Page-level event handlers**, select **UXF Macroponent Viewport Load Requested**.

    \[Omitted image "viewport-component-add-event.png"\] Alt text: UXF Macroponent Viewport Load Requested event handler selected.

19. In the **viewportElementID** element, replace the `null` value with the viewport ID that you located in a previous step.

    In this example, it is, `"viewport_1"`.

20. Select **Add**.

    \[Omitted image "viewport-component-id-route-added.png"\] Alt text: UXF Macroponent Viewport Load Requested event handler script with viewport element id.

21. Select **Save**.

22. View and test your page by selecting \[Omitted image "preview-button.png"\] Alt text: Preview button that opens the page variant..


**Parent Topic:**[Extend your UI experience with viewport components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/viewports-overview.md)

