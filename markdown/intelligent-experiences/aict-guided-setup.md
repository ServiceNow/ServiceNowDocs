---
title: Guided setup
description: Configure AI Control Tower in a logical sequence and track your progress from a single summary page, instead of navigating separate Settings pages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-guided-setup.html
release: australia
topic_type: concept
last_updated: "2026-07-27"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, AI Control Tower, Enable AI experiences]
---

# Guided setup

Configure AI Control Tower in a logical sequence and track your progress from a single summary page, instead of navigating separate Settings pages.

## Key benefits

-   Track setup progress across all four configuration areas from a single summary page, so you know what's done and what's left.
-   Move between setup items in any order and complete them as your organization is ready, since each item's status is tracked independently rather than in a fixed sequence.
-   Start from default configuration where it's provided, and confirm or adjust it to fit your organization instead of configuring every item from scratch.
-   Review every configuration change made during setup, including the update set that captured it and who made it, from the Configuration activity list on the summary page.

## Setup areas

Guided setup organizes configuration into four areas. [Guided setup areas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-guided-setup-modules.md) lists every setup item within each area and the topic to reference for more detail.

-   **Users and roles.** Assign users to the AI Stewards, AI Product Owners, and AI Risk and Compliance Managers groups.
-   **AI asset inventory.** Bring ServiceNow and external AI assets into your inventory, and decide which assets to manage.
-   **Value and cost configuration.** Configure the templates and cost inputs used to calculate the value your AI assets deliver.
-   **ServiceNow AI settings.** Configure data sharing, deployment approval, and AI model provider settings that apply across your instance.
-   **Connectors.** Connectors integrate with AI Control Tower to create AI connections with to discover AI agents from external AI platforms such as AWS, Azure, Copilot, Snowflake, Google Cloud Platform \(GCP\) Vertex AI and so on for centralized governance.

    **Note:** The Connectors page is available only when the com.sn\_ai\_disc and sn\_sgc\_central plugins are installed.

-   AI Enterprise Foundation installs all the plugins so this guided page will also be visible.

## Required roles

The AI Steward \[sn\_ai\_governance.ai\_steward\] and sn\_ia\_config.ia\_user roles are required to access guided setup. For information about opening guided setup, see [Access guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-access-guided-setup.md).

-   **[Access guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-access-guided-setup.md)**  
Open guided setup from the AI Control Tower Home page to configure AI Control Tower in a logical sequence and track your progress toward a complete setup.
-   **[Guided setup areas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-guided-setup-modules.md)**  
Area-by-area listing of the setup items in guided setup, with cross-references to the topic each item relates to.

**Parent Topic:**[Configuring AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring.md)

