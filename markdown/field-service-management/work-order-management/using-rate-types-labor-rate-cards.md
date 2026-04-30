---
title: Using rate types and labor rate cards
description: Use rate types and labor rate cards to define different cost rates for different activities recorded by field service agents.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage work order tasks, Prepare work orders, Use, Field Service Management]
---

# Using rate types and labor rate cards

Use rate types and labor rate cards to define different cost rates for different activities recorded by field service agents.

## Rate types

When multiple rate types are enabled for Field Service Management, agents can select active rate types when creating time worked entries. Active rate types can be selected in the **Rate Type** field on:

-   Time worked records
-   Time cards
-   Labor rate cards
-   The Worker Portal

The **Standard** rate type is the default value for the **Rate Type** field.

The time recording feature provides the following rate types:

-   FSM Billable Overtime
-   FSM Billable Standard

System administrators can create additional rate types by navigating to **Time Sheets** &gt; **Administration** &gt; **Rate Types** and clicking **New**.

## Labor rate cards

The time recording feature provides the following labor rate cards:

-   FSM Rate Card Task Work \(Billable\)
-   FSM Rate Card Task Work OT \(Billable\)
-   FSM Rate Card \(Default\)

System administrators can create additional labor rate cards using rate types. Navigate to **Cost** &gt; **Costs** &gt; **Labor Rate Cards** and click **New**.

## Enable multiple rate types

To enable multiple rate types for Field Service Management:

1.  Navigate to **Time Sheets** &gt; **Administration** &gt; **Time Sheet Policies**.
2.  Click the desired time sheet policy. By default, the system uses the **Default time sheet policy**.
3.  Enable the **Allow multiple rate types** field.
4.  Select a **Default rate type**. The default value for this field is the **Standard** rate type.
5.  Enable the **Auto create time card on planned task update** field.
6.  Enable the **Auto fill time card with time worked entries** field.
7.  Click **Update**.

