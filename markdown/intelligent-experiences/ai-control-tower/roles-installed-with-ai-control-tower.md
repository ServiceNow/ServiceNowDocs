---
title: AI Control Tower roles
description: Certain roles are installed along with the installation of the AI Control Tower.
locale: en-US
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, Gen AI, Generative AI, AI Governance, Now LLM, large language model]
breadcrumb: [Reference, AI Control Tower, Enable AI experiences]
---

# AI Control Tower roles

Certain roles are installed along with the installation of the AI Control Tower.

<table id="table_a4d_hpy_yfc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

AI steward\[sn\_ai\_governance\_ai\_steward\]

</td><td>

**Note:** The organization decides on assigning the AI steward role. By adding the users to the AI stewards group, allows user to have additional permissions related to playbook.

 The AI steward is responsible for:

 -   Configuring AI Control Tower
-   Adoption of AI governance practices.
-   Adoption of managing AI Control Tower and linking the AI asset Inventory.
-   Execution of AI Control Tower initiatives.
-   Understand the AI assets and AI Control Tower policies.
-   Creating AI assets.
-   Completing the AI asset lifecycle.
-   Collaboration of cross-functional teams within the organization to confirm that the organization policies are adhered.
-   Creating AI Control Tower Approval Playbook for Now Assist approvals.
-   Configure third-party LLMs and SLMs.
-   Configure Multi-instance management.
-   Add and edit a value template.
-   Learning to use the access map
-   Approve or reject an approval request.

 For AI discovery:

 -   Activate or deactivate hyperscaler connections.
-   Select the hyperscaler connections to discover agents and usage on-demand.

 For AI Gateway:

 -   Add an MCP server via AI Agent Studio.
-   Set up MCP client connections.

</td><td>

-   sn\_nowassist\_admin.user
-   sn\_ai\_governance.workspace\_admin
-   sn\_aia.admin
-   aig\_admin
-   sn\_mcp\_client.admin

</td></tr><tr><td>

AI Control Tower Workspace user \[sn\_ai\_governance\_workspace\_user\]

</td><td>

The AI Control Tower Workspace user is responsible for:

 -   Own and manage the AI assets.
-   Access the AI Control Tower home page.
-   Exclusive access to the AI portfolio tab.

</td><td>

None

</td></tr><tr><td>

AI asset owner/Product owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

</td><td>

The AI asset owner/Product owner is responsible for:

 -   Ensure that AI assets are represented accurately and kept up to date.
-   Manage AI assets like AI systems, AI models, datasets, and prompts through their asset lifecycle from intake to retirement.
-   Access My overview, Value, and Adoption tabs.
-   Creating an AI asset from the AI Control Tower home page using **Create AI Asset icon**.
-   Marking the deploy phase of the AI asset lifecycle task complete. If the AI asset gets deployed, then the state of the task doesn’t change anything automatically in the asset table or the asset governance details record.

</td><td>

None

</td></tr></tbody>
</table>