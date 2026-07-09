---
title: Enable Now Assist in Contract Management
description: Install the Now Assist in Contract Management plugin \(sn\_cm\_gen\_ai\) and activate the generative AI skills to use Now Assist skills in Contract Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/activate-na-cmpro-spo.html
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

Use the Now Assist console to enable Now Assist in Contract Management. This console contains everything that you need to install the plugin and activate the generative AI skills. For additional information, see [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/configuring-now-assist.md).

The following skills are available for Contract Management in the Now Assist Admin console.

-   Contract metadata extraction
-   Contract analysis

## Before you begin

Role required: sn\_cm\_gen\_ai.ai\_contract\_admin

## Procedure

1.  Install the Now Assist in Contract Management plugin \(sn\_cm\_gen\_ai\).

    -   For information about the plugin installation process, see [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
    -   For information about the plugin dependencies and plugin activation order, see [Application information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/cncore-support-info-na.md#cmpro-na-app-info).
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

3.  Navigate to **Employee** &gt; **CM Pro**.

4.  On the tile for your skill, select **Activate skill**.

    \[Omitted image "cmpro-NA-skills.png"\] Alt text: Now Assist skills available for Contract Management Pro.

5.  In the skill guided setup, configure the use cases and other mappings for the skill.

    For more information on configuring contract metadata extraction, see [Configuring contract metadata extraction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/cncore-conf-metadata-extraction.md).

    For more information on configuring contract analysis, see [Configuring contract analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/cmpro-conf-contract-analysis.md).

6.  In the Review and activate page, select **Activate**.


**Parent Topic:**[Using Now Assist for Contract Management in Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/sourcing-and-procurement-operations/use-now-assist-cmpro-spo.md)

**Related topics**  


[Start a metadata extraction for a contract from Source-to-Pay Workspace]()

[Analyze a contract document from Source-to-Pay Workspace]()

