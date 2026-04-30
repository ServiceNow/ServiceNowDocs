---
title: Software Spend Detection Overview dashboard
description: View all software spend from uploaded financial data in the Software Spend Detection Overview dashboard.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Software Spend Detection, Software Asset Management, IT Asset Management]
---

# Software Spend Detection Overview dashboard

View all software spend from uploaded financial data in the Software Spend Detection Overview dashboard.

Access the Software Spend Detection dashboard by navigating to **Software Spend Detection** &gt; **Overview**.

Expand a publisher in the left menu bar to see their products. Select a publisher or product to show only those transactions. Select **Edit date range** to filter transactions by date. By default, the dashboard shows all transactions from within the past year. Move your cursor over the Software Spend Over Time graph to view exact spend amounts. You can also view transactions grouped by cost center, department, or location using the tabs at the bottom of the dashboard.

Sharing the dashboard's URL displays your currently selected publisher, product, and date range. To view the applied filters, the URL recipients must already be logged in to their ServiceNow instance.

**Note:** Transactions that aren't labeled with a software publisher aren't included in the dashboard. You can manually update these transactions with a publisher to add them to the dashboard. For more information, see [Manually update transactions](../task/manually-update-transactions.md).

![Software Spend Detection dashboard for all publishers and their spend data](../image/spend-detection-dashboard.png)

|Indicator|Description|
|---------|-----------|
|Total Publishers|Total number of publishers. This includes publishers automatically detected from imported financial transactions and publishers manually added to transactions.|
|Unmanaged Publishers|Number of publishers that have unmanaged products.|
|Total Products|Total number of products. This includes products automatically detected from imported financial transactions and products manually added to transactions.|
|Unmanaged Products|Number of products that don't have a software model.|
|Total Detected Spend|Total amount spent on software. This value is equal to Accounts Payable Spend plus Expense Spend.|
|Unmanaged Spend|Total spend for transactions where the publisher and product are identified but there's no software model for the product. You can create software models and entitlements to start tracking those products and turn unmanaged spend into managed spend.|
|Accounts Payable Spend|Total spend for transactions where the type is Accounts Payable. These transactions are from an accounting or procurement system.|
|Expense Spend|Total spend for transactions where the type is Expense. These transactions are from an employee expense system or credit card feed.|
|Software Spend Over Time|Amount spent on software each month.|

**Parent Topic:**[Software Spend Detection](software-spend-detection.md)

