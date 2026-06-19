---
title: Change a flow or action's default title
description: Change the default title for a flow, subflow, or action by adding styled and dynamic text.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/manage-natural-language-title.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a flow, Build flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Change a flow or action's default title

Change the default title for a flow, subflow, or action by adding styled and dynamic text.

## Before you begin

Role required: admin, flow\_designer, or action\_designer

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  On the Workflow Studio landing page, click **New** and then select **Flow**, **Subflow**, or **Action** from the list.

3.  In the Workflow Studio main header, click the more actions icon \(\[Omitted image "MoreActionsIcon.png"\] Alt text: More Actions icon\).

4.  Click **Change default title**.

5.  On the Change default title screen, enter a title.

    1.  Use any combination of the following options to create a styled title:

        |Text style|Example input for new title|Example output in Workflow Studio environment|
        |----------|---------------------------|---------------------------------------------|
        |Bold|A \*bold\* title|\[Omitted image "natural-title-bold.png"\] Alt text: Title with bold text|
        |Italic|An \_italic\_ title|\[Omitted image "natural-title-italic.png"\] Alt text: Title with italic text|
        |Underline|An ~underlined~ title|\[Omitted image "natural-title-underline.png"\] Alt text: Title with underlined text|
        |Strikethough|A ~~strikethrough~~ title|\[Omitted image "natural-title-strikethrough.png"\] Alt text: Title with strikethrough text|
        |Title \(bold and colored\)|A \#titled\# title|\[Omitted image "natural-title-title.png"\] Alt text: Title with titled text bold and colored|

    2.  Add dynamically generated text for your title from an input, output, action, or action step by clicking the data pill picker \(\[Omitted image "data\_pill\_picker.png"\] Alt text: Data pill picker\) and selecting the input, output, action, or action step that you want to include in your title.

        **Note:** The value that is associated with the **Label** field for an input or output appears in the title.

6.  Click **Submit**.


## Result

When you change your action or subflow's default title, the new title appears in the Workflow Studio environment.

**Parent Topic:**[Create a flow in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-flow.md)

