---
title: MID server consumer
description: Use guided setup to step through the initial configuration of LES for MID server consumer.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Log Export Service \(LES\), Platform Security]
---

# MID server consumer

Use guided setup to step through the initial configuration of LES for MID server consumer.

## Guided setup home page

The home page for guided setup contains an overview of configuration types for your guided setup. You can select your guided setup type and select **Continue** to open the guided setup steps and begin configuration.

![LES guided setup for MID Server comsumer](../image/les-mid-server-setup.png)

All three setups on this page, Quick Start/Best Experience/Custom provide the same tasks and functionality. A dedicated MID Server is required to continuously stream logs from your instance to your log analytic system. The MID Server needs a one-time setup to establish a secure connection to the Hermes Messaging Service. Even if you have marked a task as completed, you can go back and uncheck it back to in-progress. To do so, first click on the **Edit** box on the upper right corner for the category. Then click on the **Edit** box for the task you want to uncheck. The **Mark as complete** box will be no longer marked.

## Guided setup categories page

The categories page contains an overview and descriptions of the categories and associated tasks. You can click either the drop down arrow to view information about the category or click **Start** to open the guided setup steps and begin configuration.

![MID Server comsumer options](../image/les-mid-server-categories.png)

Complete the tasks under each category by following the setup instructions.

-   **[Guided setup for MID Server consumers](../task/les-guided-setup-mid-server.md)**  
Implement the following steps for a complete guided setup for MID Server consumers.
-   **[Multi-consumer support using unique mid servers](les-multi-consumer.md)**  
You can now precisely manage log consumption with a new multi-consumer system, enabling dedicated consumers and MID servers for each specific log stream.

**Parent Topic:**[Configuring Log Export Service \(LES\)](les-configure.md)

**Related topics**  


[Kafka consumer](les-kafka-consumer.md)

[Set up a secure connection to the Hermes Messaging Service for LES](../task/les-hermes-cert.md)

