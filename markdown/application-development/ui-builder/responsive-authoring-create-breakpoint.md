---
title: Create a breakpoint for responsive authoring
description: Learn how to create custom breakpoints for responsive authoring to control the look and feel of a page at different form factors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/responsive-authoring-create-breakpoint.html
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Responsive authoring, Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create a breakpoint for responsive authoring

Learn how to create custom breakpoints for responsive authoring to control the look and feel of a page at different form factors.

## Before you begin

Role required: ui\_builder\_admin

## About this task

UI Builder currently offers three default form factors:

-   Desktop \(1281 pixels and larger\)
-   Tablet \(1280 pixels and smaller\)
-   Mobile \(500 pixels and smaller\)

Add up to three additional breakpoints. For example, there's a default form factor of 500 pixels and smaller for mobile devices, but you may need a breakpoint of 360 pixels.

**Note:** Custom breakpoints represent a range. If you create a breakpoint at 800 pixels, all changes apply to devices with a width at and lower than the new size. For example, a page opened on a screen 750 pixels wide uses the 800 pixel settings \(properties and styles\) unless there's another custom breakpoint at 750 pixels.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create &gt; Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Open an existing page created from scratch with responsive authoring or create a page from scratch with responsive authoring.

    For more information about how to create a page, see [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/create-page.md).

4.  Select the menu icon next to the three form factor icons.

    \[Omitted image "responsive-author-icon-more.png"\] Alt text: UI builder editor view with black arrow pointing to form factor menu icon.

5.  Select **+ Add breakpoint**.

    \[Omitted image "responsive-author-add-breakpoint.png"\] Alt text: Responsive authoring menu icon selected with black arrow pointing to add breakpoint option.

6.  Type in a width \(in pixels\) and select **Add**.

    \[Omitted image "responsive-author-new-breakpoint-size.png"\] Alt text: Custom breakpoint window.

    The new breakpoint is saved and appears as a form factor icon.

    \[Omitted image "responsive-author-new-breakpoint-icon.png"\] Alt text: New form factor icon is displayed.

    As you build the page, select any of the form factor icons to view and edit the page at that size.

7.  To edit or delete a custom breakpoint, select the menu icon, point to the breakpoint name, and select the edit or delete icon.

    \[Omitted image "responsive-author-edit-delete-breakpoint.png"\] Alt text: Responsive authoring menu icon expanded with black arrow pointing to edit and delete icons for a custom breakpoint.

    **Note:** The default form factors \(desktop, tablet, and mobile\) can't be edited or removed.


**Parent Topic:**[Responsive authoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/responsive-authoring.md)

