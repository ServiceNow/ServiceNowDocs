---
title: Modify an agentic workflow
description: Make changes to existing agentic workflows in AI Agent Studio to adjust them to suit your business needs.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-11-18"
reading_time_minutes: 3
breadcrumb: [Create an agentic workflow, Now Assist AI agents, Enable AI experiences]
---

# Modify an agentic workflow

Make changes to existing agentic workflows in AI Agent Studio to adjust them to suit your business needs.

## Before you begin

Role required: sns\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **Agentic workflows** and open the agentic workflows list on your AI Agent Studio.

2.  Select the agentic workflow that you want to modify.

3.  Modify the fields in the different sections of the guided setup, making changes to the fields for your own requirements.

    The guided setup is the same as the one for creating an agentic workflow:

    -   [Define the AI agent's specialty](define-key-requirements.md).
    -   [Define the AI agent security controls](define-sec-controls-aw.md).
    -   [\(Optional\) Add a trigger to automatically invoke your AI agent if a specified event occurs.](add-trigger-aw.md).
    -   [Determine the channels to invoke your agentic workflow.](channels-access-aw.md).
    **Note:** Some fields aren't editable if the agent is associated with a Now Assist application. If you want to make more modifications, [duplicate the agentic workflow](clone-aia-usecase.md) and make changes to the duplicate.

    -   For the **List of steps** field, you can create multiple versions of the same agentic workflow without losing previous versions. Creating versions enables you to test different instructions to evaluate performance. See [Version control for AI agents and agentic workflows](../concept/version-control.md) for more information.
    -   For the access control lists \(ACLs\), you can edit the security fields and define who can access the agentic workflow and edit the entity to run the agentic workflow as a dynamic user or an AI user. For more information, see [Implement access control in Now Assist AI agents](../concept/aia-security-implementation.md).
    -   For more guidance on creating effective instructions, see the [general guidelines for creating AI agents and agentic workflows](../concept/gg-creating-aia.md).
    You can navigate through the steps of the Guided Setup with the **Continue** and **Back** buttons.

4.  Navigate to the last step and select **Save and test** to save your changes and begin testing your modified agentic workflow.


## Result

Your agentic workflow is modified and ready to test.

## What to do next

You can [test an execution of your agentic workflow manually](test-aia-use-case.md) or [test the user access](test-aw-access.md). Once you've determined that the agentic workflow has the basic functionality you expect, you can [evaluate it using automated tests](execute-aia-eval.md).

