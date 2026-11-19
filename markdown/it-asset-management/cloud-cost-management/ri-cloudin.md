---
title: Commitments
description: The Commitments feature recommends resources that could decrease costs by the conversion of on-demand payment plans to reservation plans. These plans are also called committed-use discounts, committed-use savings plans, or reserved instance plans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/cloud-cost-management/ri-cloudin.html
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Cloud Cost Management, IT Asset Management]
---

# Commitments

The Commitments feature recommends resources that could decrease costs by the conversion of on-demand payment plans to reservation plans. These plans are also called committed-use discounts, committed-use savings plans, or reserved instance plans.

**Note:** Azure Managed Disk reserved instance to save over your on-demand costs is supported.

## How the Commitments feature works

1.  Each time billing and usage data updates, the system identifies resources recommended by your provider for reservation plans. These are resources projected to cost less under a reservation plan over their planned lifetime.
2.  The Commitments feature sorts the resources by estimated savings and displays the list on the **Commitments** page. You can view the list by navigating to **Cloud Cost Management Workspace** &gt; **Optimization** &gt; **Commitments**.

    For more information, see [Reduce resource cost with Commitments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/reserve-plan-using.md).

3.  The **Commitments** page has following tabs that you can use to sort the recommendations into categories.
    -   **New**: This tab lists the recommendations that haven't been reviewed. After reviewing a recommendation, you can select **Accept** or **Decline** as appropriate.
    -   **Accepted**: This tab lists the recommendations that have been accepted after a review. After the review, select a recommendation and then select **Accept**. The recommendation moves to the **Accepted** tab.
    -   **Declined**: This tab lists the recommendations that have been declined after a review. After the review, select a recommendation and then select **Decline**. The recommendation moves to the **Declined** tab.

