---
title: Enable integration for internal planning item
description: Enable the integration for an internal planning item type to view portfolio financials.
locale: en-US
release: xanadu
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-01-10"
reading_time_minutes: 1
breadcrumb: [Configure portfolio financials in Strategic Planning, Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Enable integration for internal planning item

Enable the integration for an internal planning item type to view portfolio financials.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Filter the name field to locate and open the **Table Map** \[sn\_align\_cmn\_int\_table\_map\] table.

3.  Select the **Show List** Related Link.

    If you are setting up your ServiceNow AI Platform for the first time, you need to create these mapping using the **New** button with the following mappings for Alignment table.

4.  Set the Active field to **true** for dmn\_demand, pm\_project, and rm\_epic.

    ![Integration for internal planning item.](../images/fin-integration-internal-planning-item.png)


