---
title: Define the network function details
description: Create a network function record in the Telecommunications Network Inventory application. You can manage the network functions such as 5Physical Network Function \(PNF\), Virtual Network Function \(VNF\) and so on.Created topics for STRY55389656 - DOC1072742
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage your network functions, Define inventory records, Use, Telecommunications Network Inventory]
---

# Define the network function details

Create a network function record in the Telecommunications Network Inventory application. You can manage the network functions such as 5Physical Network Function \(PNF\), Virtual Network Function \(VNF\) and so on.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent, sn\_ni\_core.telco\_inventory\_catalog\_manager

## About this task

When you create a network function record, it creates a corresponding configuration item \(CI\) record in the Network Function \[cmdb\_ci\_network\_function\_application\] table. By default, 19 functions are included and each record is a function.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon.](../image/ni-workspace-list-icon.png)\), and then select **Inventory** &gt; **Network Function**.

3.  Select **New**

4.  On the form, fill in the fields.

    To see a description of the fields, see [Design &amp; Planning domain in the CSDM model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/design-domain.md).

5.  Select **Submit**.


**Parent Topic:**[Manage your network functions](../concept/services.md)

