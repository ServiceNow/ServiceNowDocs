---
title: Create custom placement policies
description: Create a Knowledge Base article that defines custom placement policies for your data center racks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/create-custom-placement-policies.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 1
breadcrumb: [Data center infrastructure rack allocation, Using Design &amp; Assign Network, Use, Telecommunications Network Inventory]
---

# Create custom placement policies

Create a Knowledge Base article that defines custom placement policies for your data center racks.

## Before you begin

Role required: sn\_ni\_core.dc\_ops\_agent or sn\_ni\_core.inventory\_agent

## About this task

Custom placement policies let you define how data center infrastructure allocation places equipment in your data center or on specific racks. Policies are stored as Knowledge Base articles linked to your data center or individual racks.

Write these parameters in plain language in your Knowledge Base article. Data center infrastructure allocation interprets them automatically.

-   **maxFillPercent**: Maximum percentage of rack capacity to fill
-   **reserveRU**: Number of rack units to reserve
-   **balanceLoad**: Strategy for distributing equipment across racks
-   **preferBottomPlacement**: Placement preference \(bottom-up or top-down\)

Structure your article with:

-   A default section containing data center-wide values
-   An optional rack overrides section mapping individual racks to their custom values using each rack's unique system identifier \(sys\_id\)

## Procedure

1.  Navigate to **Knowledge** &gt; **Articles** &gt; **New**.

2.  Select **Knowledge**.

3.  Select **Standard**.

4.  Select **Next**.

5.  Enter a short description in the **Short description** field.

6.  Select **Save**.

7.  Open the knowledge article you created.

8.  Add the configuration item for your data center or rack.

    \[Omitted image "create-knowledge-article.png"\] Alt text: Knowledge article form with the configuration item field

9.  Enter the policy parameters in plain language in the article body.

10. Select **Update**.

11. Select **Publish**.


**Parent Topic:**[Data center infrastructure rack allocation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/data-center-infra-rack-allocation.md)

