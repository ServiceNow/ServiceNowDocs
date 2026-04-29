---
title: Add price ramps on a quote line item
description: Add price ramps to quote line items to define incremental price changes for recurring product offerings.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Quote Management, Configure, price, quote apps, Use, Sales and Order Management]
---

# Add price ramps on a quote line item

Add price ramps to quote line items to define incremental price changes for recurring product offerings.

## Before you begin

Configurable product offerings eligible for price ramps must have the **Enable ramps** option turned on and the **Price method** set to recurring.

Role required: Sales\_agent

## About this task

Adding a price ramp to a quote line. 

Use price ramps to specify how the price of a configurable product offering in a quote increases over different time segments, yearly, quarterly, or with a custom ramp structure.

-   When you create ramps for a parent offering, the same ramps are created automatically for each child product offering in the product bundle.
-   If price ramps haven't been created for the parent product offering, you can create ramps for child product offerings. However, if you want to create price ramps for the parent offering later, remove the ramps for all its child offerings, and then create the ramps for the parent offering.
-   After price ramps are created on a quote line item, they are visible on order line items for viewing only. Ramps can be created and modified only in quotes.
-   After price ramps are created, you can make manual pricing adjustments to a ramp segment.

    **Note:** Price ramps aren't supported for quotes with sales agreements.


## Procedure

1.  Navigate to **Workspaces** &gt; **CSM Configurable Workspace**.

2.  Select the List icon.

3.  Navigate to **Quotes** &gt; **All**.

4.  Select a quote.

5.  In the **Line Items** tab, select the **Select row** check box for the quote line and select **Ramps**.

    The Price ramps dialog displays the default settings for the ramp.

6.  On the Price ramps form, fill in the fields.

    Default values are set for the **Term,** **Ramp type,** and **Segments**. You can change them as needed.

    |Field|Description|
    |-----|-----------|
    |**Start date**|Date that the quote starts.|
    |**End date**|Date that the quote ends.|
    |**Term \(months\)**|Number of months for the ramps. The maximum term is 60 months. You can enter a two-digit decimal value, for example 36.25. After entering the term, the **End date** is updated automatically.|
    |**Ramp type**|Option that indicates whether the ramp is Yearly, Quarterly, or Custom. Custom ramp types allows agents to define ramp segments with flexible durations. When custom is selected, agents can manually add and manage ramp segments.|
    |**Segments**|Number of segments in the ramp. The default number of segments is 1. If you change the **Term** value, the number of segments is updated automatically based on the **Ramp Type**.|
    |**Annual % increase**|The percentage increase to be applied on a yearly basis.|

7.  Select **Create**.

    The price ramps are created based on the ramp settings. The Price ramp details section shows each ramp segment created and associated pricing values:**Unit list price**, **Net price**, and **Cumulative net price** for the ramp segment.

8.  To change the ramp settings, change the **Term**, **Ramp**, or **Amount % Increase** values as needed, then select **Update**.

    For example, you can change the **Ramp type** from yearly to quarterly or percentage increase. The updated price ramp details section.

9.  To make manual price adjustments to a ramp segment, do the following:

    -   Select the check box for the segment to be adjusted.
    -   Select the type of adjustment to be made.
10. If you are amending a quote, modify ramp segments in the price ramps details section as needed.

    -   To split a segment into two shorter segments within the original term, select the check box for the segment and select **Split segment**. The system automatically divides the segment and assigns the correct effective dates for each resulting segment. If the segment is currently active, the first segment ends on the current date and the second segment begins the following day. If the segment is a future segment, it is divided into two equal segments.
    -   To remove a split segment, select the check box for the segment and select **Remove segment**. The split segments are re-merged and the ramp returns to its previous state.
    **Note:** Only segments created by splitting can be removed. Original ramp segments cannot be removed.


**Parent Topic:**[Using Quote Management](../concept/quote-mgmt-using.md)

