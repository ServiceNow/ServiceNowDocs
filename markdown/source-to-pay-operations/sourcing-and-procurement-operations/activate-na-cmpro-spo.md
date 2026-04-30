---
title: Enable Now Assist in Contract Management
description: Install the Now Assist in Contract Management plugin \(sn\_cm\_gen\_ai\) and activate the generative AI skills to use Now Assist skills in Contract Management.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-03-18"
reading_time_minutes: 1
breadcrumb: [Using Now Assist for Contract Management in Sourcing and Procurement Operations, Sourcing and Procurement Operations integration with Contract Management Pro, Integrating Sourcing and Procurement Operations with other applications, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Enable Now Assist in Contract Management

Install the Now Assist in Contract Management plugin \(sn\_cm\_gen\_ai\) and activate the generative AI skills to use Now Assist skills in Contract Management.

## About this task

Use the Now Assist console to enable Now Assist in Contract Management. This console contains everything that you need to install the plugin and activate the generative AI skills. For additional information, see [Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

The following skills are available for Contract Management in the Now Assist Admin console.

-   Contract metadata extraction
-   Contract analysis

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_admin

## Procedure

1.  Install the Now Assist in Contract Management plugin \(sn\_cm\_gen\_ai\).

    -   For information about the plugin installation process, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
    -   For information about the plugin dependencies and plugin activation order, see [Application information](https://www.servicenow.com/docs/access?context=cncore-support-info-na&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US#cmpro-na-app-info).
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

3.  Navigate to **Employee** &gt; **CM Pro**.

4.  On the tile for your skill, select **Activate skill**.

    ![Now Assist skills available for Contract Management Pro.](../image/cmpro-NA-skills.png "Now Assist skills for Contract Management Pro")

5.  In the skill guided setup, configure the use cases and other mappings for the skill.

    For more information on configuring contract metadata extraction, see [Configuring contract metadata extraction](https://www.servicenow.com/docs/access?context=cncore-conf-metadata-extraction&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

    For more information on configuring contract analysis, see [Configuring contract analysis](https://www.servicenow.com/docs/access?context=cmpro-conf-contract-analysis&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

6.  In the Review and activate page, select **Activate**.


**Parent Topic:**[Using Now Assist for Contract Management in Sourcing and Procurement Operations](../concept/use-now-assist-cmpro-spo.md)

**Related topics**  


[Start a metadata extraction for a contract from Source-to-Pay Workspace](extract-metadata-spo.md)

[Analyze a contract document from Source-to-Pay Workspace](analyze-contract-spo.md)

