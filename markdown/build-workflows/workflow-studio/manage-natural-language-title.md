---
title: Change a flow or action's default title
description: Change the default title for a flow, subflow, or action by adding styled and dynamic text.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a flow, Building flows, Use, Workflow Studio, Build workflows]
---

# Change a flow or action's default title

Change the default title for a flow, subflow, or action by adding styled and dynamic text.

## Before you begin

Role required: admin, flow\_designer, or action\_designer

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  On the Workflow Studio landing page, click **New** and then select **Flow**, **Subflow**, or **Action** from the list.

3.  In the Workflow Studio main header, click the more actions icon \(![More Actions icon](../images/MoreActionsIcon.png)\).

4.  Click **Change default title**.

5.  On the Change default title screen, enter a title.

    1.  Use any combination of the following options to create a styled title:

        |Text style|Example input for new title|Example output in Workflow Studio environment|
        |----------|---------------------------|---------------------------------------------|
        |Bold|A \*bold\* title|![Title with bold text](../images/natural-title-bold.png)|
        |Italic|An \_italic\_ title|![Title with italic text](../images/natural-title-italic.png)|
        |Underline|An ~underlined~ title|![Title with underlined text](../images/natural-title-underline.png)|
        |Strikethough|A ~~strikethrough~~ title|![Title with strikethrough text](../images/natural-title-strikethrough.png)|
        |Title \(bold and colored\)|A \#titled\# title|![Title with titled text bold and colored](../images/natural-title-title.png)|

    2.  Add dynamically generated text for your title from an input, output, action, or action step by clicking the data pill picker \(![Data pill picker](../images/data_pill_picker.png)\) and selecting the input, output, action, or action step that you want to include in your title.

        **Note:** The value that is associated with the **Label** field for an input or output appears in the title.

6.  Click **Submit**.


## Result

When you change your action or subflow's default title, the new title appears in the Workflow Studio environment.

**Parent Topic:**[Create a flow in Workflow Studio](create-flow.md)

