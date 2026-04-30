---
title: Specify that a table is a fulfillment table
description: You configure a table as a fulfillment table to enable the system to prevent updates by users who are not subscribed to the app. For ServiceNow Store apps, you configure a table as a fulfillment table to enforce that fulfillment usage complies with your subscription use policy.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Fulfillment tables, Anatomy of an application, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Specify that a table is a fulfillment table

You configure a table as a fulfillment table to enable the system to prevent updates by users who are not subscribed to the app. For ServiceNow Store apps, you configure a table as a fulfillment table to enforce that fulfillment usage complies with your subscription use policy.

## Before you begin

Role required: usage\_admin, admin

## Procedure

1.  While working on a table, open the **Table Subscription Configuration** related list.

2.  Select **Fulfillment table**.

3.  Specify how the system determines ownership of records in the table so that both end users who own a record and subscribed fulfiller users can update the record: Specify the **Ownership condition**.

    For example, set the filter as **\[opened\_by\]\[is\]\[currentUser\] OR \[caller\_id\]\[is\]\[currentUser\]**.


