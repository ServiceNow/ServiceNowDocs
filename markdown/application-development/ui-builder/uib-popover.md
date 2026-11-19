---
title: Create popovers in UI Builder
description: Use popovers on a UI Builder page to overlay contextual information or functionality to help users complete tasks.Learn how to add a popover in UI Builder. A popover is a container that appears above a page when you click a component. For example, a popover might display contact information when selecting a persons name in a list.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/ui-builder/uib-popover.html
release: zurich
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create popovers in UI Builder

Use popovers on a UI Builder page to overlay contextual information or functionality to help users complete tasks.

A popover is a small window or dialog box that appears above a UI Builder page and contains additional information, options, or actions related to the content or task at hand. Add components to a popover in the same way you add modals to a page.

You can place popovers anywhere on a UI Builder page where you think additional information helps the users. Popovers are intended to provide small pieces of information or links to related content, so you should limit the amount of information or functionality within a popover because the popover only displays when a user is interacting with it.

You can make popovers visible or hidden with event mapping, such as triggering a popover to appear when selecting a button or pointing to a part of the page. For more information, see [Define map events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/event-mapping.md).

\[Omitted image "popover-demo.png"\] Alt text: Page with tool tip text link that has been selected to show an additional information popover.

**Parent Topic:**[Customize UI Builder pages using components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-components.md)

## Add popover to a UI Builder page

Learn how to add a popover in UI Builder. A popover is a container that appears above a page when you click a component. For example, a popover might display contact information when selecting a persons name in a list.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Now experience framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Open or create a page variant.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/create-page.md).

4.  Add a component to your page that you want to trigger a popover, such as a button component.

    See [Add and configure components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/add-components.md) for more information.

5.  Select the **Events** tab in the configuration panel.

6.  Select **+ Add event handler**.

    \[Omitted image "popover-add-event-handler.png"\] Alt text: Arrow pointing to the add event handler link for the button component.

7.  Select **Open Popover**.

8.  Select **Create a new popover**.

    \[Omitted image "popover-open-event.png"\] Alt text: Arrow pointing to the Create a new popover option.

9.  Select **Add**.

    The popover appears above the stage.

10. Add components to the popover by selecting the **+** icon.

    \[Omitted image "popover-add-content.png"\] Alt text: Arrow pointing to the + to add content.

11. When you finish configuring the popover, close it.

    Notice in the content tree that the popovers you create sit above the body of your page structure.

    \[Omitted image "popover-content-tree.png"\] Alt text: Arrow pointing to the custom popover in the content tree.

12. Click **Save**.

13. Select **Preview** in the UI Builder header.

14. Click on the button to test the popover.


