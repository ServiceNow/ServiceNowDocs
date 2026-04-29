---
title: Generate Scope 3 carbon calculations
description: Use the AI-driven workflow to create calculated metric definitions \(CMD\) for Scope 3 carbon emissions. The workflow employs conversational agents and integrated tools to guide methodology selection, map metrics, and simplify sustainability reporting with accuracy and efficiency.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use agentic workflows in ESG, Now Assist, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Generate Scope 3 carbon calculations

Use the AI-driven workflow to create calculated metric definitions \(CMD\) for Scope 3 carbon emissions. The workflow employs conversational agents and integrated tools to guide methodology selection, map metrics, and simplify sustainability reporting with accuracy and efficiency.

## Before you begin

Make sure that the following prerequisites are met to use this feature:

-   Operational Sustainability Workspace and Now Assist for Operational Sustainability plugin \(sn\_esg\_gen\_ai\) must be installed.
-   Carbon calculations agentic workflow must be activated. For more information, refer to [Activate carbon calculations agentic workflow](activate-carbon-calculations-agentic-workflow.md).

Role required: sn\_esg\_gen\_ai.cmd\_agent\_user

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace**.

2.  Select the Now Assist \(![Now Assist panel icon.](../images/nap-icon.png)\) icon.

    A conversational assistant opens in the Now Assist panel.

3.  In the text column, provide a prompt for Now Assist to create a CMD.

    Some prompt example to be used in this context are as follows:

    -   Create a calculated metric definition for scope 3 emission for business travel.
    -   Create a calculated metric definition for Scope 3 emissions for waste generated in operations.
    -   Create a calculated metric definition for Scope 3 emissions for end-of-life treatment of sold products.
4.  Interact with the conversational AI agent by responding to its questions to create the CMD.

    The Document and visual insights Agent detects the category and retrieves calculation methods for category 6 from the guidance document.

5.  Select the calculation method that you want to use for Scope 3 Category by entering the option number.

    The formula expands based on user input, and the system uses semantic matching to find metric definitions \(MDs\) and emission factors \(EFs\). For example, transportation types for business travel.

6.  Review the suggestions and select the correct options to refine your formula.

    If the presented MDs and EFs are correct, choose the corresponding option numbers. If none of the options fit, refine your input or skip the component to exclude it from the formula. For business travel, selecting air and train adds those transport components to the formula.

7.  After all selections, the agent refines the formula with the chosen metric definitions and emission factors, making it instance-specific.

8.  The agent creates a Calculated Metric Definition \(CMD\), shares the link, and keeps it inactive for your review and activation.


## What to do next

-   After the Calculated Metric Definition \(CMD\) is created, update its frequency before changing the formula. The frequency should be set based on the frequencies of the underlying metric definitions used in the CMD.
-   Activate the CMD, for more information refer to, [Create a calculated metric definition](../../metrics/task/create-composite-metric-definition.md).

**Parent Topic:**[Use agentic AI in Now Assist for Operational Sustainability \(formerly ESG\)](../concept/use-agentic-ai-in-now-assist-for-esg-management.md)

