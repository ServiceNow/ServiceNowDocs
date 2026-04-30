---
title: Add a viewport modal to your experience
description: Add a viewport within a modal in your experience.
locale: en-US
release: yokohama
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Extend your UI experience with viewport components, Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add a viewport modal to your experience

Add a viewport within a modal in your experience.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Use viewport modals to embed subpages or other experiences within a modal in your parent page or experience. Viewport modals can be opened via events or scripts. Viewport modals are limited to one subroute per viewport modal. You can create additional viewport modals for extra routes.

**Note:** Legacy viewport modals cannot be upgraded and must be recreated to take advantage of the new functionality.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information.

3.  Open or create a page.

    If you open an existing page, ensure you are in the same scope as the original page. If not, change the scope before you start editing the page. Application scoping protects applications by identifying and restricting access to application files and data. Administrators set the scope to specify what parts of an application are accessible to other applications. Application scope protects data and application files. See [Learn about security and roles](security-roles.md) for more information on application scope.

4.  Select **+ Add content** in the content tree.

5.  Select a **Single column** layout.

6.  Select **+** next to **Modals** in the content tree.

7.  Select **Viewport Modal** in the list.

    ![Pointer selecting the viewport modal in the modal list.](../image/viewport-modal-add.png "Viewport Modal")

    A viewport model appears above your page.

8.  Click **Save**.

9.  Select the viewport in the content tree.

    ![Arrow pointing at the viewport added in the previous step.](../image/viewport-modal-select.png)

10. Select **+ Add** next to **Page collections** in the configure tab.

    ![Arrow pointing to + Add in the Configure panel](../image/viewport-modal-edit-content.png)

11. Select a page collection or create a new one.

    For more information, see [Create a page collection across multiple UI pages](create-page-collection.md).

    ![Page collection selection screen with option to create a collection.](../image/page-collection-list.png)

12. Click **Add**.

13. Click **Save**.

14. Add a component that opens the viewport modal.

    The following example uses a button to open the viewport modal.

    ![Arrow pointing to a button component used to open a viewport modal.](../image/viewport-modal-button.png)

15. Select the **Events** tab.

16. Select **+ Add event handler**.

    ![Arrow pointing to + Add event handler in the events tab of a button component.](../image/button-add-event-handler.png)

17. Select **Open or close modal dialog**.

18. Enable **Open modal dialog**.

19. Select the viewport modal that you created in the **Modal** dropdown.

    ![Configure the event handler for your viewport modal.](../image/viewport-modal-open-dialog.png)

    The **Viewport ID** auto populates.

20. Select **Add**.

21. Select **Save**.

22. View and test your page by selecting ![Preview button that opens the page variant.](../image/preview-button.png).


**Parent Topic:**[Extend your UI experience with viewport components](../concept/viewports-overview.md)

