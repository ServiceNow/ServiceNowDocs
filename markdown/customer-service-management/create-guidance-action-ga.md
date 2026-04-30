---
title: Create a guidance action for a guidance
description: Configure the actions that agents can take to resolve cases or issues.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a guidance in the Core UI, Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Create a guidance action for a guidance

Configure the actions that agents can take to resolve cases or issues.

## Before you begin

Role required: sn\_gd\_guidance.guidance\_manager

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Guidances**.

2.  Select a guidance from the Guidances list.

3.  In the Guidance Actions form section, select **New**.

4.  On the Guidance Action form, fill in the fields.

<table id="table_fsp_ybn_25b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Guidance

</td><td>

The guidance that this action is associated with. This field is read only.

</td></tr><tr><td>

Action label

</td><td>

A name for this guidance action.

</td></tr><tr><td>

Call to Action Label

</td><td>

The label for the action button that appears on the recommendation card in the contextual side panel. For example, **Review and attach article** or **Propose Solution**.

</td></tr><tr><td>

Action Behavior

</td><td>

The selected behavior for the guidance action:-   **Single click**: The action is initiated and completed with one selection and the card moves to the **History** tab in the side panel. Useful for simple actions such as escalating a case.
-   **Open in Contextual Side Panel**: The action opens in a detailed view within the side panel. The agent can review the details in the side panel, such as reviewing the content of a knowledge base article.
-   **Open in Sub Tab**: The action opens in a separate tab.
You can configure the preview experience for all the action behavior types and configure the detail view for the actions that open in the sub tab or contextual side panel. For more information, see [Configure guidance detail experience](configure-guidance-preview-detail-experiences-ga.md).

 **Note:** Actions that open in the contextual side panel or in the subtab don’t move to the in-progress state. The action moves to the in-progress or completed state only when the agent selects the action button in the detail view.

</td></tr><tr><td>

Primary

</td><td>

Denotes the guidance action as a primary action. This field is enabled by default.

 A primary action highlights the action that the agent should take and makes that action available as a button on the recommendation card.

**Note:** A guidance can have only one primary guidance action.

 If this field is not selected, the guidance action is a secondary action available through the more actions menu on the recommendation card.

</td></tr><tr><td>

Application

</td><td>

The application that this guidance action is associated with. This field is read only.

</td></tr><tr><td>

Guidance Action Automation

</td><td>

The flow associated with this guidance action.

</td></tr><tr><td>

Order

</td><td>

The order of the action.

</td></tr><tr><td>

Completion Message

</td><td>

The message that appears at the top of the recommendation card when the guidance action is complete. For example, **KB article was shared**.

</td></tr></tbody>
</table>5.  Depending on the selected flow in the **Guidance Action Automation** field, you can configure flow inputs and guidance outputs.

    -   Configure flow inputs in the **Automation Flow Inputs** tab.
    -   Configure outputs in the **Guidance Outputs** tab.

        These fields can contain static text, dynamic content \(field values from guidance inputs\), or a combination of static text and dynamic content. To use dynamic content, select the Pill-picker icon \(![Pill-picker icon](../image/icon-pill-picker.png)\) next to the field and select a guidance input from the list.

6.  Select **Submit**.


## What to do next

Configure a guidance node and link the created guidance to this node to [provide actions to agents](configure-guidance-in-gdb.md).

