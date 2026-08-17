---
title: Multi-Instance Setup
description: The Multi-Instance Setup enables a prod \(manager\) instance to manage multiple sub-prod \(managed\) instances and facilitate communication for AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-control-tower/multi-instance-management.html
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, generative AI]
breadcrumb: [Configurations, AI Control Tower dashboard, Explore, AI Control Tower \(legacy\), Enable AI experiences]
---

# Multi-Instance Setup

The Multi-Instance Setup enables a prod \(manager\) instance to manage multiple sub-prod \(managed\) instances and facilitate communication for AI Control Tower.

## Instance Management Hierarchy overview

The Multi-Instance Framework uses a hierarchical structure to organize how instances manage and communicate with each other. This hierarchy helps you configure the appropriate manager instance for your environment.

## Instance Roles and Capabilities

Prod Instance

A prod instance can manage both other prod instances and sub-prod instances. This makes it suitable for centralized governance across your organization.

Sub-Prod Instance

A sub-prod instance can manage other sub-prod instances but can't manage prod instances. sub-prod instances are typically used for specific teams, environments, or business units.

## Configure Multi-Instance Framework with Multiple Prod and Sub-Prod Instances

Scenario: You have two prod instances and 6–8 sub-prod instances, and you want to configure the Multi-Instance Framework to manage and synchronize assets across all instances.

The Multi-Instance Framework enables a prod instance to manage multiple sub-prod instances and facilitate communication for centralized asset governance. Depending on your organizational needs, you can configure Multi-Instance Framework in two ways

-   Centralized Configuration- Use when your organization prefers centralized governance and a streamlined review process.
-   Distributed Configuration- Use when your organization has distinct business units or teams that require independent asset governance within a shared environment.

## Centralized Configuration

Use this configuration if you want a single access move to review and manage data from all instances.

1.  Designate one prod instance as the manager instance.
2.  Configure all other instances \(the second prod instance and all sub-prod instances\) to send synchronization requests to the manager instance.

The prod instance controls asset states, rules, and policies for all connected instances.

## Distributed Configuration

Use this configuration if you want to organize instances into separate management groups.

1.  Designate the first prod instance to manage a group of sub-prod instances \(for example, 2–3 sub-prod instances\).
2.  Designate the second prod instance to manage another group of sub-prod instances \(for example, 4–5 sub-prod instances\).
3.  Configure each sub-prod instance to send synchronization requests to its assigned prod instance.

## After configuration

After configuring the Multi-Instance Framework, enable AI Asset data transfer on the prod instance from the AI Control Tower user interface.

When you configure AI Asset data transfer, the remaining values are automatically configured. No additional setup is required.

**Note:** For information about configuring Multi-instance management for AI Control Tower, see [Configure Multi-instance management for AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/ai-control-tower/configure-multi-instance-management-for-aict.md).

## AI asset Synchronization

The Multi-Instance Framework synchronizes assets from sub-prod instances to the manager instance, enabling faster review processes.

The framework also synchronizes rules from the prod instance to all sub-prod instances.

**Note:** Starting with the May 2026 release, confirm that both the prod and sub-prod instances are running the same AI Control Tower core version \(6.2.4\), which is the minimum supported version.

Upgrade the prod instance to version 6.2.4 when you upgrade a sub-prod instance to confirm the Multi-Instance Framework functions correctly.

-   **AI inventory information**

    You can include the sub-prod instances to synchronize with the prod instance. This synchronization enables AI inventory information to flow between the instances.

    When configured, the scheduled job synchronizes AI systems, AI models, prompts, and datasets across instances. Staring with the September \(2025\) release, the job also synchronizes AI agents.

    **Note:** State of the assets while configuring Multi-Instance management.

    The production AI inventory displays the actual state of your assets like models, datasets, and skills from a production perspective. However, assets that are active in a sub-prod instance environment remain classified as under development from the sub-prod instance perspective because they are still in testing and not yet live.

    Due to this distinction, asset states remain separate across environments and don't synchronize. An asset's state transitions to deployed only when the asset and its related records are activated in the production system.

    In summary, the state indicates the asset's complete lifecycle progression, not its status within any single environment.

-   **Data sharing preference**

    Enable the data sharing preference to apply the production settings to all sub-prod instances. By default, this preference is turned off.

-   **Data overflow processing and bursting preference**

    Enable data overflow processing and bursting preferences to apply the production settings to all sub-prod instances. By default, these preferences are turned off.


**Note:** All the preferences mentioned earlier for a sub-prod instance are available in read-only mode, when Multi-Instance is configured and enabled.

For information on Data, see [Data sharing, Data overflow processing, and Security &amp; privacy in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/ai-control-tower/data.md)

For more information on trust concepts and trust configuration management, see [Cross-instance application trust configuration](https://www.servicenow.com/docs/r/platform-administration/grant-access-v2.html).

