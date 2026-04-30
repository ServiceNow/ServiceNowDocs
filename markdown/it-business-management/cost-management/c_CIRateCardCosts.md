---
title: CI rate card costs
description: CI rate card costs generate expense lines for configuration items on the associated rate cardYou can add a rate card cost to the CI rate card.You can remove a rate card cost on the CI Rate Card form.To prevent a cost from processing, clear the Active option. Use the option to make a rate card cost permanently inactive or to temporarily skip a cost from processing.Configuration item costs often change over time as facilities or vendor rates change.
locale: en-US
release: zurich
product: Cost Management
classification: cost-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [CI rate cards, Cost Management, Strategic Portfolio Management]
---

# CI rate card costs

CI rate card costs generate expense lines for configuration items on the associated rate card

Costs associated with rate cards are stored in the Rate Card Cost \(`fm_ci_rate_card_cost`\) table. Each cost is applied to every configuration item associated with the rate card when the costs are processed.

Expense Line is active by default.

**Parent Topic:**[CI rate cards](c_CIRateCards.md)

## Add a CI rate card cost

You can add a rate card cost to the CI rate card.

### Before you begin

Role required: financial\_mgmt\_admin

### Procedure

1.  Navigate to **All** &gt; **Cost** &gt; **Costs** &gt; **CI Rate Cards**.

2.  Select a rate card.

3.  In the **Rate Card Costs** related list, click **New**.

4.  Enter a **Start date**.

5.  Fill in the fields, as appropriate.

<table id="simpletable_hwl_l3q_3r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

\[Read-only\] The rate card cost identification number. Automatically assigned.

</td></tr><tr><td>

Rate card

</td><td>

The identification number of the rate card to which this rate card cost is associated.

</td></tr><tr><td>

Name

</td><td>

The rate card cost name.

</td></tr><tr><td>

Active

</td><td>

Check box that indicates whether to enable cost processing for this cost.

</td></tr><tr><td>

Short description

</td><td>

A brief description of the rate card cost. The description is used to identify the processed cost on an expense line record.

</td></tr><tr><td>

Start date

</td><td>

The date the cost should start being processed.

</td></tr><tr><td>

End date

</td><td>

The date the cost should stop being processed.

</td></tr><tr><td>

Interval

</td><td>

The frequency at which the rate card cost recurs.

</td></tr><tr><td>

Recurring

</td><td>

Check box that indicates whether the cost is a repeating cost. Also sets generated expense lines to show as recurring. If this check box is cleared, no further expenses are generated automatically.

</td></tr><tr><td>

Sales tax

</td><td>

Check box that indicates whether to apply sales tax to the cost.

</td></tr><tr><td>

Tax rate

</td><td>

The tax rate to apply to the cost.

</td></tr><tr><td>

Order

</td><td>

Used by task rate cards.

</td></tr><tr><td>

Last processed

</td><td>

\[Read-only\] The date and time this cost was last processed.

</td></tr><tr><td>

Next process

</td><td>

The next date on which new expenses will be processed based on the Process FM Costs scheduled job.

</td></tr><tr><td>

Base cost

</td><td>

The amount that must be paid before taxes.

</td></tr><tr><td>

Tax cost

</td><td>

Total cost of the tax.

</td></tr><tr><td>

Total cost

</td><td>

Total rate card cost, including taxes.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the rate card cost.

</td></tr></tbody>
</table>
## Remove a rate card cost

You can remove a rate card cost on the CI Rate Card form.

### Before you begin

Role required: financial\_mgmt\_admin

### Procedure

1.  Navigate to **All** &gt; **Cost** &gt; **Costs** &gt; **CI Rate Cards**.

2.  Select a rate card.

3.  In the **Rate Card Costs** related list, click a **Number**.

4.  Click **Delete**.


## Disable a rate card cost

To prevent a cost from processing, clear the Active option. Use the option to make a rate card cost permanently inactive or to temporarily skip a cost from processing.

### Before you begin

Role required: financial\_mgmt\_admin

### Procedure

1.  Navigate to **All** &gt; **Cost** &gt; **Costs** &gt; **CI Rate Cards**.

2.  Select a rate card.

3.  In the **Rate Card Costs** related list, click a **Number**.

4.  Clear the **Active** check box.


## Modify a rate card cost

Configuration item costs often change over time as facilities or vendor rates change.

### Before you begin

Role required: financial\_mgmt\_admin

### About this task

Expense lines are the snapshot of a given interval's costs, so changing the cost does not affect already generated expense lines. When costs change, either modify the cost amount or disable the current cost and create a new cost to represent the cost going forward. The changes are processed in the next generated expense line. To keep historical records of costs, create new costs rather than modifying existing ones and set the end date of the disabled cost to show that the cost agreement expired.

### Procedure

1.  Navigate to **All** &gt; **Cost** &gt; **Costs** &gt; **CI Rate Cards**.

2.  Select a rate card.

3.  Click a rate card cost **Number**.

4.  Modify the fields, as necessary.


