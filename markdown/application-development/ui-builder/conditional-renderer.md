---
title: Dynamically display content with conditional renderers
description: Use the conditional renderer component to display content or components based on specified conditions.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Dynamically display content with conditional renderers

Use the conditional renderer component to display content or components based on specified conditions.

## Before you begin

Role required: ui\_builder\_admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Create or open a page or page variant.

    For more information about how to create a page in UI Builder, see [Create a page in UI Builder](create-page.md).

4.  Select **+ Add content** in the content tree.

5.  Select **Components**.

6.  Select **Conditional renderer**.

7.  Select **+ Add condition**.

8.  Choose how you want to build the condition.

    |Type of condition|Description|
    |-----------------|-----------|
    |Empty Container|Create a condition by placing components in an empty container.|
    |Card|Create a condition by placing components in a card component.|
    |Single component|Add a condition directly to a component without using a container or card. This works well for showing a single component only when the condition is true.|

9.  Select a component from the list if you selected **Single component** in the previous step.

10. On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Component label|Label to identify the conditional content.|
    |Component ID|Unique identifier used when binding data.|
    |Description \(Optional\)|Description of the condition.|
    |Render content|Select when to render the content on the page.|
    |Condition|Use data or formulas to set the condition for rendering content. The field requires a true boolean value.|

11. Select **Apply**.

12. Add components to the container or card.

    For more information about adding components, see [Customize UI Builder pages using components](../concept/work-components.md).

13. Configure the components in the conditional renderer.

14. Select **Save**.


**Parent Topic:**[Customize UI Builder pages using components](../concept/work-components.md)

