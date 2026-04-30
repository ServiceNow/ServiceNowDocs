---
title: Configure AI Control Tower
description: Configuring the AI Control Tower workspace.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Now Assist, Gen AI, Generative AI, AI Governance, Now LLM, large language model]
breadcrumb: [Configuring AI Control Tower workflows, AI Control Tower, Enable AI experiences]
---

# Configure AI Control Tower

Configuring the AI Control Tower workspace.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\]

**Note:** The custom widget support hasn’t been included on the AI Control Tower overview for AI stewards.

## Procedure

1.  Navigate to the **Configurations** view in the AI Control Tower.

2.  Expand **Data** and select **Opt in** under **Data sharing**.

    To view the **Data** section, confirm that the generative AI Controller plugin is installed.

    The **Opt in** option is enabled by default.

    **Note:** Opting out of data sharing can only be enabled by your Account Executive or the Now Support team. The Opt-out is disabled by default and not toggle-able.

    For information on Data and Data sharing, see [Explore Data](data.md) and refer the FAQs section on the Data sharing page.

3.  Select **Controls** and activate the **Automatically trigger playbooks** option.

    The **Automatically trigger playbooks** option is inactive by default.

    Enabling the **Automatically trigger playbooks** and adding an AI asset to this environment automatically triggers approval requests.

    **Note:** When the Automatically trigger playbooks isn't enabled, the approval requests aren't generated automatically, however, the asset manager can initiate them manually.

    Verify to have the **Automatically trigger playbooks** option enabled in your production environment.

    For information on Controls available on the AI Control Tower, see [Controls](controls.md)


## Result

The AI Control Tower is configured.

