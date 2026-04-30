---
title: Generate Scope 3 carbon calculations
description: Use the carbon calculations agentic workflow to create a calculated metric definition \(CMD\) for Scope 3 carbon emissions. The workflow employs AI agents and integrated tools to guide methodology selection, map metrics, and simplify sustainability reporting with accuracy and efficiency.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-21"
reading_time_minutes: 2
breadcrumb: [Use agentic workflows Now Assist for Operational Sustainability, Now Assist for Operational Sustainability, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Generate Scope 3 carbon calculations

Use the carbon calculations agentic workflow to create a calculated metric definition \(CMD\) for Scope 3 carbon emissions. The workflow employs AI agents and integrated tools to guide methodology selection, map metrics, and simplify sustainability reporting with accuracy and efficiency.

## Before you begin

The following prerequisites must be met to use this feature:

-   Operational Sustainability Workspace and Now Assist for Operational Sustainability plugin \(sn\_esg\_gen\_ai\) must be installed.
-   Carbon calculations agentic workflow must be activated. For more information, refer to [Activate the carbon calculations agentic workflow](activate-carbon-calculations-agentic-workflow.md).

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Role required: sn\_esg\_gen\_ai.cmd\_agent\_user

## Procedure

1.  Navigate to **All** &gt; **ESG** &gt; **ESG Workspace**.

2.  Select the Now Assist \(![Now Assist panel icon.](../images/nap-icon.png)\) icon.

    A conversational assistant opens in the Now Assist panel.

3.  Provide a prompt to create a CMD.

    Some prompt examples are as follows:

    -   Create a calculated metric definition for scope 3 emission for business travel.
    -   Create a calculated metric definition for Scope 3 emissions for waste generated in operations.
    -   Create a calculated metric definition for Scope 3 emissions for end-of-life treatment of sold products.
4.  Respond to the questions from the AI agent. ![Now Assist panel displaying the conversational chat](../images/Now-assist-panel.png)

    The document and visual insights AI agent detects the category and retrieves calculation methods for category 6 from the guidance document.

5.  Select the calculation method that you want to use for Scope 3 Category by entering the option number.

    The formula expands based on your input, and the AI agent uses semantic matching to find metric definitions \(MDs\) and emission factors \(EFs\). For example, transportation types for business travel.

6.  Review the suggestions and select the correct options to refine your formula.

    If the presented MDs and EFs are correct, choose the corresponding option numbers. If none of the options fit, refine your input or skip the component to exclude it from the formula. For business travel, selecting air and train adds those transport components to the formula.

7.  After all selections, the agent refines the formula with the chosen metric definitions and emission factors.

8.  The agent creates a CMD, shares the link, and sets the state to inactive.


## What to do next

-   After the CMD is created, update its frequency before changing the formula. The frequency should be set based on the frequencies of the underlying metric definitions used in the CMD.
-   Activate the CMD. For more information, refer to [Create a calculated metric definition](../../metrics/task/create-composite-metric-definition.md).

**Parent Topic:**[Use agentic AI in Now Assist for Operational Sustainability](../concept/use-agentic-ai-in-now-assist-for-esg-management.md)

