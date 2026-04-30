---
title: Monitoring Workflow Data Fabric capability usage with Subscription Management
description: You can monitor Workflow Data Fabric capability usage and the relative token use rate of each capability with Subscription Management.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-06-09"
reading_time_minutes: 1
keywords: [token ratio]
breadcrumb: [Viewing product subscription details, Explore, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Monitoring Workflow Data Fabric capability usage with Subscription Management

You can monitor Workflow Data Fabric capability usage and the relative token use rate of each capability with Subscription Management.

## Overview of monitoring Workflow Data Fabric capability usage

Workflow Data Fabric subscriptions include tokens that can be used for Workflow Data Fabric capabilities. Using a capability expends a number of tokens determined by the terms of your Workflow Data Fabric license.

You can track token usage over time from the **Allocation summary** of a Workflow Data Fabric subscription details page.

## Workflow Data Fabric token ratios

The **Token ratio** tab of the subscription details page shows the number of tokens expended each time a capability is used. Each row in the tab represents a capability. The **Column names** and **Column values** columns show how each capability is tracked.

The following table shows definitions of the entries in the **Column names** column.

|Column name entry|definition|
|-----------------|----------|
|capability\_id|A unique identifier for each Workflow Data Fabric capability.|
|exchange\_value|The number of tokens expended when the associated capability is used.|

The **Column values** column has two comma-separated entries per row. The first entry corresponds to the capabilitiy\_id, while the second entry corresponds to the exchange\_value.

## Workflow Data Fabric token ratio tab

Match the entries under **Column names** to the entries under **Column values** to determine how many tokens are expended per Workflow Data Fabric capability.

![Token ratio tab showingColumn names and Column values columns. All rows under Column names display "capability_id, exchange_value." Refer to the following example for more detail](../image/sub-mgt-wdf-token-ratio.png)

The first row under **Column values** displays "API\_ACCESS, 8." Because the entries under **Column values** correspond to capability\_id and exchange\_value from **Column names**, the capability\_id is "API\_ACCESS" and the exchange\_value is "8." In other words, a Workflow Data Fabric capability that requires API access expends eight tokens.

