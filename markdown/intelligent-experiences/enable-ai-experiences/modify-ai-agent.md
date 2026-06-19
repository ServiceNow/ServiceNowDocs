---
title: Modify an AI agent
description: Modify an AI agent in AI Agent Studio to suit your changing business needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/enable-ai-experiences/modify-ai-agent.html
release: zurich
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2025-11-18"
reading_time_minutes: 3
breadcrumb: [Create an AI agent, Now Assist AI agents, Enable AI experiences]
---

# Modify an AI agent

Modify an AI agent in AI Agent Studio to suit your changing business needs.

## Before you begin

Role required: sns\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage** &gt; **AI agents**

2.  Select the AI agent that you want to modify.

3.  Modify the fields of the different sections of the Guided Setup, making changes to the fields for your requirements.

    The guided setup is the same as the one for creating an AI agent:

    -   [Define the AI agent's specialty](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/define-specialty.md).
    -   [Define the AI agent security controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/define-sec-controls-aia.md).
    -   [\(Optional\) Add a trigger to automatically invoke your AI agent if a specified event occurs.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/add-trigger-aia.md).
    -   [Determine whether you want to use the Now Assist in Virtual Agent chat assistants and/or as UI action, set the processing messages, and activate your AI agent.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/channels-access-aia.md).
    **Note:** Some fields aren't editable if the agent is associated with a Now Assist application. If you want to make more modifications, [duplicate the agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/clone-aia-usecase.md) and make changes to the duplicate.

    -   For the **List of steps** field in the **Define specialty** step, you can create multiple versions of the same AI agent without losing previous versions. Creating versions enables you to test different instructions to evaluate performance. See [Version control for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/version-control.md) for more information.
    -   For more guidance on creating effective instructions, see the [general guidelines for creating AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/gg-creating-aia.md).
    -   For the access control lists \(ACLs\), you can edit the security fields and define who can access the AI agent and edit the entity to run the AI agent as a dynamic user or an AI user. For more information, see [Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/aia-security-implementation.md).
    You can navigate through the steps of the Guided Setup with the **Continue** and **Back** buttons.

4.  Navigate to the last step and select **Test** to save your changes and begin testing your modified agent.


## Result

Your agent is modified and ready to test.

## What to do next

You can [test an execution of your AI agent manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/test-ai-agent.md) or [test the user access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/test-aia-access.md). Once you've determined that the AI agent has the basic functionality you expect, you can [evaluate the AI agent using automated tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/execute-aia-eval.md).

