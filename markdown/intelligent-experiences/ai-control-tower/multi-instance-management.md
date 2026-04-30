---
title: Multi-instance Setup
description: The multi-instance setup enables a prod \(manager\) instance to control, manage, and communicate with multiple sub-prod \(managed\) instances for AI Control Tower.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Now Assist, generative AI]
breadcrumb: [Configurations, AI Control Tower dashboard, Exploring AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Multi-instance Setup

The multi-instance setup enables a prod \(manager\) instance to control, manage, and communicate with multiple sub-prod \(managed\) instances for AI Control Tower.

## AI asset Synchronization

Multi-instance setup uses the multi-instance framework, which helps the user to synchronize assets from sub-prod instances to prod instances for a faster review process.

Multi-instance setup synchronizes rules for the sub-prod instances from the prod instance.

**Note:** Starting with the February 2026 release, ensure that both the prod and sub-prod instances are running the same AI Control Tower version \(5.1.1\), which is the minimum supported version.

If there’s any upgrade to version 5.1.1 in a sub-prod, then it’s advisable to upgrade the prod instance from 5.1.1 to ensure Multi-instance framework functions correctly.

-   **AI inventory information**

    You can include the sub-prod instances that you want to synchronize with the prod instance. This synchronizes AI inventory information between the instances.

    When configured, the scheduled job starts syncing AI systems, AI models, prompts, and datasets. From the September \(2025\) release, the job has been enhanced to include syncing AI agents as well.

    **Note:** State of the assets while configuring Multi-instance management.

    The AI inventory in production reflects the true state of your assets like models, datasets, or skills from a production standpoint. Even if a model or dataset is active in a sub prod \(lower\) environment, it's still considered as under development from a prod perspective, since it's being tested and not yet live.

    For this reason, you don’t synchronize asset states across environments. An asset’s state changes to **deployed** only when the asset and its related records are activated in the production system.

    In summary, the state represents the overall lifecycle of the asset, not its local status in a specific environment.

-   **Data sharing preference**

    You have the option to enable the data sharing preference, when it is enabled the preferences of the data sharing from the production will be applied to all sub-prod instances. By default, the data sharing preference is turned off.

-   **Data overflow processing and bursting preference**

    You have the option to enable the data overflow processing and bursting preferences, when it is enabled the preferences of the data overflow and bursting from the production will be applied to all sub-prod instances. By default, data overflow processing and bursting is turned off.


**Note:** All the preferences mentioned earlier for a sub-prod instance are available in read-only mode, when Multi-instance is configured and enabled.

For information about configuring Multi-instance management for AI Control Tower, see [Configure Multi-instance management for AI Control Tower](../task/configure-multi-instance-management-for-aict.md)

For information about Data section, see [Explore Data](data.md)

