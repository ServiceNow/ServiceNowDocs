---
title: Verify skill activation and configurations
description: Verify that the skills are activated, configurations are complete, and role masking defined for conversational search.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-11-13"
reading_time_minutes: 1
breadcrumb: [Configure conversational search, Configure, Now Assist in CM Pro, Contract Management Pro, Employee Service Management]
---

# Verify skill activation and configurations

Verify that the skills are activated, configurations are complete, and role masking defined for conversational search.

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_config, sn\_cm\_core.contract\_config

## Procedure

1.  Verify the **TextToResult** is active.

    1.  Navigate to **All** &gt; **Admin Center** &gt; **Now Assist Admin**.

    2.  Navigate to **Platform** &gt; **Other**.

    3.  Search for `TextToResult`.

    4.  Verify that the skill is active.

        ![Verify TextToResult Platform skill is active](../image/cmpro-na-texttoresult-skill.png "TextToResult Platform skill")

2.  Verify the conversational search skills are active.

    1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

    2.  Navigate to **Other**.

    3.  Verify **Contracts query enhancer** and **Search contract with contextual input** are active.

        ![Skill activation for conversational search](../image/cmpro-na-converse-skill.png "Skill activation for conversational search")

3.  Verify the Now Assist panel is selected in the agentic workflow.

    1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

    2.  Search for `Conversational Contract Search and Insights` and open it.

    3.  Select **Select channels and status**.

    4.  Verify **Engage via the Now Assist panel** is enabled.

        ![Enable conversation search for Now Assist panel](../image/cmpro-na-nap-enable.png "Enable conversational search for Now Assist panel")

4.  Set the data access permissions for the agentic workflow- `Conversational Contract Search`.

    For more information, see [Configuring user access and data permissions for agentic workflows](../concept/cmpro-conf-users-agentic-wf.md).

5.  Set the data access permissions for the Agent- `Search contracts AI`.

    For more information, see [Configuring user access and data permissions for AI agents](../concept/cmpro-conf-users-ai-agents.md).

6.  Set the data access permissions for the Now Assist skills- `Contracts query enhancer` and `Search contract with contextual input`.

    For more information, see [Configure data permissions for Now Assist skills](cmpro-conf-roles-skills.md)


