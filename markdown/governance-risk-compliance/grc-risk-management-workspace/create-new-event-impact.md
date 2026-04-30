---
title: Create a risk event entry
description: Create a risk event entry to determine the monetary or non-monetary impact of the risk event. A risk event can have multiple risk event entries.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use Risk Events, Use, Risk Management, Governance, Risk, and Compliance]
---

# Create a risk event entry

Create a risk event entry to determine the monetary or non-monetary impact of the risk event. A risk event can have multiple risk event entries.

## Before you begin

Role required: sn\_risk.manager

## About this task

Risk event entries capture the direct and indirect losses reported due to the risk event.

## Procedure

1.  Navigate to **All** &gt; **Risk Events** &gt; **All Events** and select the event to be analyzed.

2.  Click the Risk Event Entries related list.

3.  Click **New**.

4.  On the form, fill in the fields.

<table id="table_cjy_rj3_f3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number for the event entry. This field value is automatically set.

</td></tr><tr><td>

Risk event

</td><td>

Title of the risk event. This field value is automatically set.

</td></tr><tr><td>

Date of impact

</td><td>

Date that the impact was recorded. **Note:** The date of discovery and the date of first recognition can be different. This date cannot be a future date.

</td></tr><tr><td>

Amount

</td><td>

Amount that the impact costs. The amount entered is reflected in the Summary related list.

</td></tr><tr><td>

Rapid recovery

</td><td>

Loss amount for this entry if it's recovered in a short time, which is generally five working days.

</td></tr><tr><td>

Impact type

</td><td>

Type of financial impact for the event. Select from the following types:-   **Direct/Indirect Impact**: Direct or indirect financial impact of the event on the entity.
-   **Recovery**: Amount recovered from the total financial impact.
-   **Additional Cost**: The additional cost incurred due to the impact.
-   **Non-Financial Impact**: The event has no financial impact.


</td></tr><tr><td>

Category

</td><td>

**Direct** or **Indirect**. For example, if the impact is direct, is it external?

</td></tr><tr><td>

Sub category

</td><td>

Sub category of the event impact. Select one of the following categories:-   **External Cost**: The cost that's incurred for external agencies. For example, if a loss is incurred due to erroneous accounting and an external auditor was hired to assess the event, the cost incurred in employing the auditor is an external cost.
-   **General Ledger**: The book of accounts in which this event is entered.
-   **Booked Provision**: Refers to the amount that you set aside in your accounts to cover a future event. For example, if a firm sets aside an amount to cover a risk event that might occur in the future.
-   **Revenue Reversal/Timing Losses**: When you reverse revenue, a reverse entry is created that backs out the original entry. Don't enter any new accounting information into the system.


</td></tr><tr><td>

GL account reference

</td><td>

Account number in which this entry is captured in the ERP system.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the impact.

</td></tr></tbody>
</table>5.  Click **Submit**.


## What to do next

-   **Create or edit a new risk**

    Creating or editing a new risk for an event is useful for future prediction of risks. The information obtained from the risks is useful for scoring and reporting. For more information, see [Create a risk manually](t_CreateRisk.md).

-   **Link new control to risks**

    A control is used to prevent a risk from occurring. Linking the controls to risks lets users know which controls failed and why the risk event occurred. This information can be used for future predictions and reporting.

    **Note:** Only those risks and controls that are tagged to the impacted entity can be related to this risk event.

    For more information, see [Create a control](../../grc-policy-and-compliance/task/t_CreateAControl.md).


**Parent Topic:**[Use Risk Events](../concept/use-risk-events.md)

