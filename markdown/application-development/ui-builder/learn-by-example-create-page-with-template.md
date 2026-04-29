---
title: Create a record page using a template
description: After you've created your demo experience, you can create a record page from a template. A record page shows data from a table.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Learn UI Builder by example, Learning UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create a record page using a template

After you've created your demo experience, you can create a record page from a template. A record page shows data from a table.

## Before you begin

Role required: ui\_builder\_admin

## Procedure

1.  Open the main page for your demo experience.

    ![Demo Experience.](../image/demo-experience.png "Demo Experience")

2.  From the main page for your experience, select the plus \(**+**\) sign next to **Pages**.

    ![Create new page or variant](../image/create-new-or-variant.png "Create a new page or variant")

3.  Select **Create a new page** to create a page that resides at a different URL.

4.  On the **First, select a template** screen, locate the **Standard record** template and hover over **Use template**.

    **Note:** Optionally, you could select **Learn more** to read about the template before selecting it.

    ![Page details for the standard record template.](../image/page-details-standard-record.png "Page details")

5.  In the **Name** field of the Page details screen, type `Task record page`, and select **Continue**.

6.  Select a URL page type in the **Type** drop-down list. UI Builder automatically assigns a page type based on the template you select, but you can change this value if needed.

7.  Select **Looks good** on the next screen.

8.  On the **Tell us about your variant** screen, enter a condition to determine when the page is visible.

    1.  In the **Parameter** field, select **table**.

    2.  In the **Operator** field, select **is**.

    3.  In the **Value** field, enter `task`.

    ![Parameter field with dropdown options 'table' and 'sysId', along with Operator and Value fields.](../image/demo-experience-declare-conditions.png "Condition fields")

    This page is visible to users accessing a record from the Task table.

9.  Select **Create**.

    The visual editor opens. Here, you can begin editing your new page.

    **Note:** The new page includes LOTS of layout, preconfigured components, data, and modals. Additionally, it includes test values you can modify for your own particular use cases. Using templates can be a significant time-saver when creating new pages.

10. You can select the area above the Page content pane to view information about test values included in the template.

    ![Edit test values included in the template.](../image/edit-test-values.png "Edit test values included in the template")


## What to do next

Select the **Next topic** link to learn how to define audiences who can view your pages in UI Builder.

-   **[Create a button that opens a modal](learn-by-example-button-modal.md)**  
After you've created your demo experience and added a blank page, you can edit the page variant as needed. For the sake of this demo, you can create a button and a modal, and configure the button to open the modal.

**Parent Topic:**[Learn UI Builder by example](../concept/learning-uib-by-example.md)

**Related topics**  


[Create a demo experience to explore UI Builder](learn-by-example-create-experience.md)

[Create a blank page](learn-by-example-create-blank-page.md)

[Define an audience for your variant](learn-by-example-define-audience.md)

[Define conditions for your variant](learn-by-example-define-conditions.md)

[Customize forms within a form component](learn-by-example-edit-form-component.md)

