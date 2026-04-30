---
title: Flow action numbering
description: The action outline displays a whole number besides each action and flow logic block in a flow. You can update flows containing legacy action numbering from within Workflow Studio.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring flows, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Flow action numbering

The action outline displays a whole number besides each action and flow logic block in a flow. You can update flows containing legacy action numbering from within Workflow Studio.

## Current action numbering

The current number sequence increments each item in the action outline by a whole value of one. For example, if a flow logic block is step 2 in the action outline, then the actions within the flow logic block are steps 3, 4, and 5. Inline scripts reference the whole number value of actions and flow logic.

## Legacy action numbering

The legacy number sequence increments each item within a flow logic block by a decimal value of 0.1. For example, if a flow logic block is step 2 in the action outline, then the actions within the flow logic block are steps 2.1, 2.2, and 2.3. Inline scripts reference the decimal values of actions and flow logic.

**Important:** Inline scripts produce an error when they refer to actions using legacy action numbering. Update all inline script references to the use the new action numbering.

## Automatic action numbering updates

Workflow Studio automatically updates the action numbering of all flows during upgrade. Whenever you open a flow that contains inline scripts, Workflow Studio checks the script for references to legacy action numbering. If the script contains legacy references, it displays a prompt to update the action numbering.

![Confirmation prompt to Allow Flow Designer to update action numbering in your scripts?](../images/update-script-action-numbers-confirmation.png "Prompt to automatically update action numbers in inline scripts")

The system attempts to match the actions referred to by the legacy action numbering to actions with the new numbering. Review the inline script changes to ensure that your inline scripts refer to the correct actions.

**Note:** If an upgraded flow does not have the correct numbering, move the actions and flow logic to the correct sequence.

**Parent Topic:**[Exploring flows](../../workflow-studio/concept/exploring-flows.md)

