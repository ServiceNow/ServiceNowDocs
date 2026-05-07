---
title: Enhancing customer impact visibility for PSEW processes
description: Use the customer impact tab to reduce navigation time, and enhance tracking and management of PSEW processes. This visibility enables you to quickly assess business impact and take informed actions.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-03-27"
reading_time_minutes: 2
breadcrumb: [Proactive Service Experience Workflow, Explore, Product Support for Technology]
---

# Enhancing customer impact visibility for PSEW processes

Use the customer impact tab to reduce navigation time, and enhance tracking and management of PSEW processes. This visibility enables you to quickly assess business impact and take informed actions.

The customer impact tab is available in incident, change, and problem case records and is aligned with the diagnostic framework. This tab displays key metrics and insights across customer accounts, reactive cases, and install base items. It improves visibility and streamlines decision-making during PSEW processes.

You can create proactive cases after analyzing the impact and communicate with the customers or consumers.

![Customer impact tab showing affected contract value, products, install base, and reactive cases metrics with affected customers table](../image/customer-impact-tab.png "Example of customer impact tab")

## Access

You can access the customer impact tab as follows:

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.
2.  Open the incident, problem, or change record.
3.  Select the **Customer impact** tab.

## Indicators

The Customer impact tab provides the following indicators. Select the indicator to view the details.

|Indicator|Description|
|---------|-----------|
|Affected total contract value|Combined contract value of both impacted accounts and consumers, helping quantify the overall business impact.|
|Affected products|Number of products purchased by impacted customers. For example, multiple ServiceNow instances purchased by a single customer.|
|Affected install base|Total number of impacted install base within the customer environment.|
|Total reactive cases|Total number of reactive cases.|

## Affected customers

The Affected customers section provides a detailed view of impacted customer and consumer accounts. This section enables you to assess service impact, track engagement, and take proactive actions.

The Affected customers section contains the following tabs.

-   **Accounts tab**

    List of impacted customer accounts and their details.

-   **Consumers tab**

    List of impacted consumers and their details.


To learn more about the columns in each tab, see [Affected customers list columns](../reference/affected-customer-list-columns.md).

The Affected customers section uses interactive pills to quickly filter and view customer and consumer-level impact:

|Pill|Description|
|----|-----------|
|All|Lists the complete list of accounts.|
|Critical service impact|Lists accounts experiencing significant service disruption.|
|No proactive records|Lists accounts without any proactive case created.|
|No customer communication|Lists accounts that have not yet received any communication.|

To learn more about how to create proactive cases and resolve incidents, see [About identifying affected accounts with Proactive Service Experience Workflows in Incident Management](psew-identify-act-incident.md).

**Parent Topic:**[Proactive Service Experience Workflows architecture](architecture-assurance-workflows.md)

