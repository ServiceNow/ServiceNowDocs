---
title: CI relationships
description: To get reports that represent the total costs for a business service, there must be some association between the service and the CIs that make up the service. This is done with CI relationships.
locale: en-US
release: australia
product: Cost Management
classification: cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cost Management, Strategic Portfolio Management]
---

# CI relationships

To get reports that represent the total costs for a business service, there must be some association between the service and the CIs that make up the service. This is done with CI relationships.

## Before you begin

Role required: financial\_mgmt\_admin

## About this task

Use the demo data of the Cost Management plugin to understand how to check all expense lines related to a business service.

## Procedure

1.  Navigate to **All** &gt; **Cost** &gt; **Config** &gt; **Business Services**.

2.  Select **Retail**.

3.  View the business service map by selecting the dependency views icon \(![Dependency views.](../image/dependency-views.png)\).

    ![Retail business service map.](../image/CostDemoRetailBsm.jpg "Example business service map")

    This view shows that the dbaix901nyc server is a dependency of the Retail Adding Points, Retail POS, and Retail business services. So whenever the dbaix901nyc server incurs a cost, it would be represented at each of the business services.

    The dbaix901nyc server is a member of the Sun E20K Servers NY CI rate card, so the expenses can be verified from this CI rate card.

    To view them:

    1.  Navigate to **All** &gt; **Cost** &gt; **Costs** &gt; **CI Rate Cards**.
    2.  Select **Sun E20K Servers NY**.
    3.  Select the Expense Line related list.

        If this related list is not available, configure your form layout to display the Expense Line → Rate Card related list.

    4.  Filter the related list for **short description contains dbaix901nyc**.
    The server's expenses are now visible:

    ![Cost Demo Server Expense](../image/CostDemoServerexp.jpg "Example server expenses")

    This example contains one direct expense \(**inherited = false**\), and three inherited expenses that have been generated from other direct expenses. These inherited expenses are based on CI relationships, which allow for reporting at any business service level.

    For more information on expense aggregation, see [Enable relationship aggregation](t_EnableRelationshipAggregation.md).


**Parent Topic:**[Cost Management](../reference/r_CostManagement.md)

