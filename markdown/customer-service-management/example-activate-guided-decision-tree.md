---
title: Activate the Troubleshoot credit card transaction failure decision tree
description: Validate and activate the completed decision tree so you can use it in playbooks in case records or as recommendations in Recommended Actions.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Example configuration of a decision tree, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Activate the Troubleshoot credit card transaction failure decision tree

Validate and activate the completed decision tree so you can use it in playbooks in case records or as recommendations in Recommended Actions.

## Before you begin

Role required: admin, sn\_gd\_core.decision\_tree\_author

## About this task

When you activate the completed decision tree, Decision Tree Builder checks for errors such as missing information, invalid input mappings due to changes in prior node inputs, or missing guidance inputs. After all the errors are resolved, you can validate and activate the decision tree.

If you make changes to an activated decision tree, remember to activate the decision tree again to display the updated decision tree in a workspace.

## Procedure

1.  In Decision Tree Builder, select **Activate**.

    -   If there are errors in your decision tree, error icons and alert messages are displayed. You must resolve the errors before you can activate the decision tree. For more information, see [Validation error notifications in Decision Tree Builder](../concept/validation-errors-builder.md).
    -   If there are no errors, a confirmation dialog box displays.
2.  In the confirmation dialog box, select **Activate now**.

    A success message with instructions on the next action to take is displayed.


## Result

-   The status of the decision tree is changed from **Not Active** to **Active**.
-   The **Activate** button is disabled.

## What to do next

-   Configure recommended actions to use the activated decision tree as a recommendation. The recommendations appear as cards in the contextual side panel of a workspace. For more information, see [Add Guided Decisions to Recommended Actions](add-guided-decisions-to-recommended-actions.md).
-   Configure Playbooks to use the activated decision tree as part of a playbook in a record tab. For more information, see [Add Guided Decisions to playbooks](add-guided-decision-playbook.md).

