---
title: Set up or update preferred currency options
description: Set up or update the preferred currency options for your cloud cost and usage data to gain reporting flexibility. These currency options become available for Cloud Cost Management users to choose from.
locale: en-US
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-01-12"
reading_time_minutes: 1
breadcrumb: [Use, Cloud Cost Management, IT Asset Management]
---

# Set up or update preferred currency options

Set up or update the preferred currency options for your cloud cost and usage data to gain reporting flexibility. These currency options become available for Cloud Cost Management users to choose from.

## Before you begin

Role required: insights\_admin

## About this task

Setting up currency options enables Cloud Cost Management users to choose from the list of available currencies. Costs are calculated using the exchange rates specified by cloud service providers. These exchange rates are automatically applied to ensure cost reporting accuracy across regions.

**Note:** If you haven't set up the preferred currency options earlier, all the billing and usage data is displayed in the default currency.

## Procedure

1.  Navigate to **Workspaces** &gt; **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **Multi-currency setup**.

2.  Select a currency code from the **Currency Option 1** drop-down list

    ![Multi-currency setup in the Cloud Cost Management Workspace](../image/multicurrency-setup.png "Multi-currency setup")

3.  Select the **Active** check box for **Currency Option 1** to activate the currency.

    The **Status** field is currently set to **Not mapped**.

4.  Select **Save**.

    The **Status** field changes to **Awaiting processing**. After the processing starts, the **Status** field changes to **In progress** and a message is displayed on the screen that shows the progress in percent. The **Save** button remains unavailable until the status changes to **Ready**.

5.  Repeat step 2, 3, and 4 to select additional currency options and activate them.

    At any given time, you can see a total of five active currencies that includes one reference currency plus four additional currencies.


## Result

After the **Status** field changes to Ready, the selected currencies become available for selection in the **Currency preference** list on the Operations view.

**Parent Topic:**[Using Cloud Cost Management](../concept/using-cloud-insights.md)

