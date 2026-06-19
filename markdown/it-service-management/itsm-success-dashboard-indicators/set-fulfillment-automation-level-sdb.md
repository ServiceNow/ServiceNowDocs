---
title: Set fulfillment automation level of catalog item for the Success Dashboard indicators
description: Set the fulfillment automation level of catalog items from manual to fully-automate to reduce manual effort and accelerate the turn around time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/itsm-success-dashboard-indicators/set-fulfillment-automation-level-sdb.html
release: zurich
product: ITSM Success Dashboard Indicators
classification: itsm-success-dashboard-indicators
topic_type: task
last_updated: "2026-04-17"
reading_time_minutes: 1
breadcrumb: [ITSM Success Dashboard Admin console, Configure, ITSM Success Dashboard indicators, IT Service Management]
---

# Set fulfillment automation level of catalog item for the Success Dashboard indicators

Set the fulfillment automation level of catalog items from manual to fully-automate to reduce manual effort and accelerate the turn around time.

## Before you begin

Role required: admin or catalog\_admin

The Fulfillment automation level field does not change based on how ServiceNow processes or routes the catalog item. The value you select is used by the ITSM Success Dashboard to categorize the item in the Catalog item fulfillment automation level distribution indicator.

## Procedure

1.  Navigate to **All** &gt; **Success Dashboard** &gt; **Getting Started**.

2.  Select **Success Dashboard** tab.

3.  In the **Catalog item fulfillment level** card, select **Configure**

4.  In the Catalog Item form, set the **Fulfillment automation level.**

    The available options are:

    -   Unspecified: Catalog item is not specified.
    -   Manual: Catalog item is set to manual.
    -   Semi-automated: Catalog item is semi-automated.
    -   Fully automated: Catalog item is completely automated.
5.  Select **Update**.

    For any catalog item, if the **Fulfillment automation level** field is set to **Fully automated**, then on the **Success Dashboard,**in the **Catalog item fulfillment level** card, the **% Fully automated catalog items** value increments.

6.  To view the fulfillment automation level distribution for all catalog items:

    1.  Go to **All** &gt; **Success Dashboard** &gt; **Getting Started** &gt; ******Catalog item fulfillment level** card **Configure**
    2.  In the **Catalog Item fulfillment level** page, you can view the **Fulfillment automation level distribution** as a pie chart.
    \[Omitted image "fulfillment-automation-level-distribution.png"\] Alt text: Fulfillment automation level distribution pie chart


**Parent Topic:**[ITSM Success Dashboard Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/itsm-success-dashboard-indicators/admin-console-sd.md)

