---
title: Activate the carbon calculations agentic workflow
description: Activate and configure the carbon calculation agentic workflow that uses AI agents and tools. It automates the creation of calculated metric definition \(CMD\) records and formulas for Scope 3 carbon emissions.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-11-18"
reading_time_minutes: 3
breadcrumb: [Configure, Now Assist for Operational Sustainability, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Activate the carbon calculations agentic workflow

Activate and configure the carbon calculation agentic workflow that uses AI agents and tools. It automates the creation of calculated metric definition \(CMD\) records and formulas for Scope 3 carbon emissions.

## Before you begin

Install the Now Assist for Operational Sustainability plugin \(sn\_esg\_gen\_ai\).

Attach the Calculation Guidance document to the relevant record in the Emission Calculation Guidelines table. For further details, refer to [Attaching calculation guidance document](attaching-calculation-guidance-document.md).

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

**Important:** This workflow is active by default. All fields are read-only except for the Triggers and Channels and status sections. To modify other fields, clone the workflow. Currently, you can't edit agent prompts or provide feedback for training.

If you have the user sn\_esg\_gen\_ai.cmd\_agent\_user role, you can get carbon calculations agentic workflow in the Now Assist panel.

This workflow uses an agentic approach to guide ESG teams through carbon calculations, promoting accurate Scope 3 emissions reporting. It uses AI agents and integrated tools to select methodologies, map metrics, and validate emission factors for transparency and compliance. The process requires user interaction and runs under helper agent roles with ACL-based security.

**Note:** You can add or remove AI agents from this workflow by making a copy and customizing it. For more information, about copying agentic workflows, see [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

If you have the sn\_generative\_ai.nsa\_admin role, you can perform the following actions on Now Assist agentic workflows:

-   [Duplicate an agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)
-   [Modify an agentic workflow](https://www.servicenow.com/docs/access?context=modify-aia-use-case&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)
-   [Delete an agentic workflow](https://www.servicenow.com/docs/access?context=delete-aia-use-case&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.

2.  In the Recent agentic workflows and AI agents activity section, select **Generate calculations for metrics**.

3.  Under the **Define key requirements**, find the Add AI agents that can perform these steps section and activate the calculation operand AI agent and the calculation creation AI agent.

4.  To activate the calculation operand AI agent, refer to [Activate calculation operand AI agent CMD](activate-calculation-operand-ai-agent-cmd.md).

5.  To activate the calculation creation AI agent, refer to [Activate calculation creation AI agent](activate-calculation-creation-ai-agent.md).

6.  On the Generate calculations for metrics page, test the agentic workflow.

    1.  Under the Define security controls section, review the details in the Define user access subsection and Define data access subsection, and select **Continue**.

    2.  Under the Add Triggers section, review the details and select **Continue**.

    3.  Under the Select a UI display section, set the display as active.

    4.  Select **Save and test**.

    5.  In the **Task** of the **Test Details**, enter the prompt.

    6.  Initiate the test by selecting **Continue to Test Chat Response**.


## What to do next

Use the **Testing** playground to [test your new agentic workflow](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) using example utterances.

Verify that the executive summary and recommendations are generated. If activation fails, check roles and skill configuration.

After you’ve confirmed the workflow is functioning as expected, you can select the Ask Now Assist action menu and enter your prompt.

If you haven't already set up the Now Assist panel, for more information see, [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

-   **[Activate calculation creation AI agent](activate-calculation-creation-ai-agent.md)**  
The calculation creation AI agent creates a calculated metric definition record using the formula passed in the input.
-   **[Activate calculation operand AI agent CMD](activate-calculation-operand-ai-agent-cmd.md)**  
The calculation operand AI agent CMD identifies and retrieves relevant metric definitions and emission factors from existing sources. It then replaces generic references in the input formula with precise metric definition and emission factor names.
-   **[Attaching calculation guidance document](attaching-calculation-guidance-document.md)**  
Attach the Calculation Guidance PDF to the designated emission calculation guidelines table record to enable the carbon calculations agentic workflow. The agent relies on this document to extract calculation methods, formulas, and category details for automated metric definition creation.

**Parent Topic:**[Configure Now Assist for Operational Sustainability](../concept/configure-now-assist-for-esg.md)

