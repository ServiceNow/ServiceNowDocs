---
title: Create a risk event in the Risk Workspace
description: Create a risk event in the Risk Workspace. Risk events are potential or actual financial and non-financial losses, near misses, and gains that occur within an organization.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Create a risk event in the Risk Workspace

Create a risk event in the Risk Workspace. Risk events are potential or actual financial and non-financial losses, near misses, and gains that occur within an organization.

## Before you begin

Role required: sn\_risk.manager

## About this task

When you create a risk event, the risk event goes through the defined lifecycle of analysis, approval, and closure. Creating or recording risk events enables your organization to prevent similar events from occurring.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace** &gt; **Risk events** &gt; **All events**.

2.  Click **New**.

3.  On the form, fill in the following fields:

<table id="table_epy_qrq_f5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the risk event such as `ATM Theft`.

</td></tr><tr><td>

Description

</td><td>

Description of the risk event reported.

</td></tr><tr><td class="sub-head" colspan="2">

Classification

</td></tr><tr><td>

Event type

</td><td>

Type of event. The options are as follows:-   **Financial Impact**: Select this option when the event leads to monetary losses.
-   **Non-Financial Impact**: Select this option when the event does not have monetary losses.


</td></tr><tr><td>

Category

</td><td>

Event category. You can edit the category to apply one of the following options:-   **Personal**: For example, any physical harm caused to an employee.
-   **Legal**: For example, an employee is found conducting business that is a conflict of interest.
-   **Information Security**: For example, a theft, burglary, or system crash.
-   **Human Resources**: For example, sensitive lawsuits by an employee against another employee.


</td></tr><tr><td>

Sub type

</td><td>

Event sub type. The choices are as follows:-   **Actual**: Select this option if the event has actually occurred.
-   **Potential**: Select this option if the event has the potential to occur.


</td></tr><tr><td>

Discovered by

</td><td>

Person who discovered the risk event.

</td></tr><tr><td>

Opened

</td><td>

Date of risk event creation.

</td></tr><tr><td>

Opened by

</td><td>

Person creating the risk event.

</td></tr><tr><td>

Near miss

</td><td>

Option to specify if the risk event had the potential to incur losses but did not result in losses. This field is available when **Potential** is selected from the **Sub type** field.

</td></tr><tr><td>

Financial gain

</td><td>

Option to show if the risk event resulted in a gain instead of a loss. This option is automatically selected if the risk event meets one of the following conditions:-   If **Potential** is selected from **Sub type** field and the **Expected loss** field or the **Potential loss** field has a negative value because of the gain.
-   If **Actual** is selected from **Sub type** field and the **Net loss** field has a negative value.


</td></tr><tr><td>

Used in modeling

</td><td>

Option to share the risk event records with external systems where advanced analysis is performed using simulation techniques such as the Monte Carlo simulation. The Monte Carlo simulation is a mathematical technique used to estimate the possible outcomes of an uncertain event.

</td></tr><tr><td class="sub-head" colspan="2">

Ownership

</td></tr><tr><td>

Primary entity

</td><td>

Entity that bears the loss. This entity is visible to management for reporting.

</td></tr><tr><td>

Owning group

</td><td>

Group responsible for monitoring the event to closure.

</td></tr><tr><td>

Cost center

</td><td>

Account number of the entity.

</td></tr><tr><td>

Owner

</td><td>

Person who owns the risk event. A risk manager can be an event owner. If the owning group is specified, the owners are filtered from the owning group.

</td></tr><tr><td class="sub-head" colspan="2">

Key Dates

</td></tr><tr><td>

Date of occurrence

</td><td>

Date when the event occurred.

</td></tr><tr><td>

Date of discovery

</td><td>

Date that the event was first discovered or noticed.

</td></tr><tr><td class="sub-head" colspan="2">

Loss/Gain Estimates

</td></tr><tr><td>

Expected loss

</td><td>

Amount of loss expected. Expected loss is the probability weighted average of all possible losses. This amount is based on the user’s judgment of the expected amount that the organization might lose.

</td></tr><tr><td>

Non financial impact

</td><td>

Rating for the non-financial impact associated with the event.

</td></tr><tr><td>

Potential loss

</td><td>

Amount expected to be a potential loss due to the risk event. This amount is the maximum loss an entity can incur due to the loss from the risk event.

</td></tr><tr><td class="sub-head" colspan="2">

Credit/Market Risk Overlap

</td></tr><tr><td>

Boundary event

</td><td>

Option to mark the event as a boundary event. A boundary event is an operational risk event which leads to a consequence, such as a financial loss, in another risk category.

</td></tr><tr><td>

External risk type

</td><td>

Type of external risk the risk event can have. The choices are as the following:-   **Credit**: Credit risk is the possibility of a loss resulting from a borrower's failure to repay a loan or meet contractual obligations. For example, when lenders offer credit cards, or loans, there's a risk that the borrower might not repay the loan.
-   **Market**: Market risk is the possibility of an investor incurring losses due to factors that affect the performance of the financial markets in which the investor is involved. For example, a recession might impact the entire market.
 This option appears when **Boundary event** is selected.

</td></tr><tr><td>

External risk reference

</td><td>

ID for reconciliation in the book of accounts. This value is automatically set.This option appears when **Boundary event** is selected.

</td></tr><tr><td class="sub-head" colspan="2">

Root Cause Analysis

</td></tr><tr><td>

Cause

</td><td>

Primary reason why the risk event occurred.

</td></tr><tr><td>

Cause description

</td><td>

Brief description about why the risk event occurred.

</td></tr><tr><td>

Consequence

</td><td>

Consequence of the risk event. For example, regulatory fines can be imposed as a result of the risk event.

</td></tr><tr><td>

Actions taken

</td><td>

Remedial actions that were taken to address the issue. This is the initial record of the event.

</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Work notes

</td><td>

Notes about the risk event. These notes are not visible to external users.

</td></tr><tr><td>

Additional comments

</td><td>

Additional comments about the risk event. These notes are visible to the external users.

</td></tr></tbody>
</table>4.  Click **Save**.


**Parent Topic:**[Using the Risk Workspace](../concept/using-risk-workspace.md)

