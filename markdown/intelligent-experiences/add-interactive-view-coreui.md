---
title: Add Interactive View Experience in the Core UI
description: Add the Interactive View Experience component to a page variant to display agentic AI processes on a record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-interactive-view-coreui.html
release: australia
topic_type: task
last_updated: "2026-07-15"
reading_time_minutes: 1
breadcrumb: [In-product agentic AI, Agentic workflows, AI assets, Enable AI experiences]
---

# Add Interactive View Experience in the Core UI

Add the Interactive View Experience component to a page variant to display agentic AI processes on a record.

## Before you begin

Ensure that the **com.glide.agentic\_processes\_view.enabled** property is enabled. See [Enable the in-product experience for agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-inproduct-aia.md) for instructions.

Role required: personalize\_form

## Procedure

1.  Navigate to the table where the Interactive View Experience should be displayed.

2.  Select the Additional Actions icon \[Omitted image "icon-docintel-additional-actions.png"\] icon to open the menu and select **View**.

3.  Select the view where the component should appear, or select **Default view** to display it by default.

4.  From the Additional Actions menu, select **Configure** &gt; **Form Layout**.

5.  Confirm the current view in **View Name**, or create a view from the **View name** dropdown.

6.  Choose whether this view should use the inline or sidebar experience.

    1.  For the inline experience, add **AI Activity Inline Experience** from Available to Selected, and position it directly above Contextual Search Results \(or at the end of the section if that formatter isn't present\).

    2.  For the sidebar experience, add **AI Activity Sidebar Experience** from Available to Selected.

        If you don't see either option in the **Available** tab, try selecting or creating a new section of the form.

        Placement in the list doesn't affect sidebar position. The sidebar always opens on the right side of the screen.

        If you add both the AI Activity Inline Experience and the AI Activity Sidebar Experience, the sidebar won't open. The AI Activity button will only redirect to the Inline Experience.

7.  Save, then switch to the modified view and interact with the AI Activity button \[Omitted image "ai-activity-button.png"\] to confirm the inline or sidebar experience renders correctly.

8.  Repeat for all tables and views where the Interactive View Experience should be enabled.


## Result

The Interactive View component is added to a record form on the view you have specified.

## What to do next

Verify whether the agentic process displays correctly by running an AI specialist, agentic workflow, or AI agent on a record of the table configured.

