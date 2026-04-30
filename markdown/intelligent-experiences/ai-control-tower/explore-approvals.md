---
title: Explore Approvals
description: Explore the Approvals section on the Configurations page of AI Control Tower.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Controls, Configurations, AI Control Tower dashboard, Exploring AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Explore Approvals

Explore the **Approvals** section on the Configurations page of AI Control Tower.

The approvals page has two features to set up governance of your approvals for AI assets and workflows.

-   AI steward approval for AI assets- when the AI steward approval-required control is active, asset deployment is blocked until it receives an approval from the AI steward approves it. This control is inactive by default but can be activated for required approval before deploying an AI asset.
    1.  AI systems- Activating AI systems, all the AI skills and agents need approval by an AI steward before being deployed.
    2.  MCP servers- Activating MCP servers setting, AI Stewards can block unapproved MCP servers from being used in AI Agent Studio. The setting is deactivated by default and must be manually activated by the AI steward.

        When you attempt to add an unapproved server in Agent Studio, you’ll see an error message: 'Approval is needed to display tools', helping prevent any interaction with that server.

    3.  AI models- Activating this all AI models need approval by an AI steward before being deployed.
-   Automatically trigger playbooks- enabling automatically trigger playbooks control triggers approval requests for AI assets. When inactive, only the AI steward can initiate requests manually. The recommendation is to have this control activated in the production environment.

![Configurations screen.](../image/approvals-aict-config.png)

