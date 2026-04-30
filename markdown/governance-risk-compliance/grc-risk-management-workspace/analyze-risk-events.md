---
title: Analyze a risk event
description: Analyze user-submitted risk events to determine if the risk event is valid and needs further processing.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Use Risk Events, Use, Risk Management, Governance, Risk, and Compliance]
---

# Analyze a risk event

Analyze user-submitted risk events to determine if the risk event is valid and needs further processing.

## Before you begin

Role required: sn\_risk.manager

## About this task

When you analyse a risk event, you add more relevant details to the risk event that is submitted. During analysis, you can either reject the event if the risk event doesn't appear to be an actual risk event, or request more information if the information is insufficient.

## Procedure

1.  Navigate to **All** &gt; **Risk Events** &gt; **All Events** and open the risk event that you want to analyze.

    Alternatively, you can also navigate to **Risk Events** &gt; **New Events**.

2.  On the form, review the fields and edit them as necessary.

<table id="table_cjy_rj3_f3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the risk event. Edit the name of the risk, if necessary, to provide a more intuitive name.

</td></tr><tr><td>

Number

</td><td>

Number of the risk event. This field is automatically set.

</td></tr><tr><td>

Discovered by

</td><td>

The person who discovered the risk event. Edit the **Discovered by** field, if necessary.

</td></tr><tr><td>

Opened by

</td><td>

Person who created the event.

</td></tr><tr><td>

Primary entity

</td><td>

Entity that bears the loss. This entity is visible to management for reporting.

</td></tr><tr><td>

Owning group

</td><td>

Group responsible for monitoring the event to closure.

</td></tr><tr><td>

Owner

</td><td>

The person who owns the risk event. A risk manager can be an event owner. If the owning group is specified, the owners are filtered from the owning group.

</td></tr><tr><td>

State

</td><td>

State of the risk event. This field is automatically set.

</td></tr><tr><td>

Substate

</td><td>

Substate of the event. This field is automatically set.

</td></tr><tr><td>

Event type

</td><td>

Type of event. You can edit the event type, if necessary. For example, if during analysis you observe that the event type isn't a financial impact, you can edit the entry.

</td></tr><tr><td>

Sub type

</td><td>

Event sub type. You can edit the sub type, if necessary. For example, if during analysis you observe that the event type isn't an actual event but a potential event, you can edit the entry.

</td></tr><tr><td>

Category

</td><td>

Event category. You can edit the category to apply one of the following options:-   **Personal**: For example, any physical harm caused to an employee.
-   **Legal**: For example, an employee is found conducting business that is a conflict of interest.
-   **Information Security**: For example, a theft, burglary, or system crash.
-   **Human Resources**: For example, sensitive lawsuits by an employee against another employee.


</td></tr><tr><td>

Approvers

</td><td>

The person who approves the risk event. Any user with the sn\_risk.user role can approve the risk event.

</td></tr><tr><td>

Cost center

</td><td>

Corresponding account number of the entity.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the event in this field.

</td></tr><tr><td class="sub-head" colspan="2">

Dates

</td></tr><tr><td>

Date of occurrence

</td><td>

Exact day, month, and year when the event occurred. For example, a mortgage was lent against a property that didn't comply with the building regulations on August 12, 2019.

</td></tr><tr><td>

Date of discovery

</td><td>

Date that the event was first discovered or noticed. For example, the mortgage was discovered on August 24, 2019.

</td></tr><tr><td>

Date of first recognition

</td><td>

Date that the event was first recognized and entered in the book of accounts. For example, the loss entries were entered in the firm’s book of accounts on August 26, 2019.

</td></tr><tr><td class="sub-head" colspan="2">

Loss/Gain Estimates

</td></tr><tr><td>

Expected loss

</td><td>

Amount of loss expected. Expected loss is the probability weighted average of all possible losses. This amount is based on the user’s judgment of the expected amount that the organization might lose.

</td></tr><tr><td>

Potential loss

</td><td>

Amount expected to be a potential loss due to the risk event. This amount is the maximum loss an entity can incur due to the loss from the risk event.

</td></tr><tr><td class="sub-head" colspan="2">

Event Analysis

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

Consequence of the risk event. For example: Regulatory fines can be imposed as a result of the risk event.

</td></tr><tr><td>

Actions taken

</td><td>

Remedial actions that were taken to address the issue. This is the initial record of the event.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Credit/Market Risk

</td></tr><tr><td>

Boundary event

</td><td>

Option for a boundary event. A boundary event is an operational risk event which leads to a consequence, such as a financial loss in another risk category.

</td></tr><tr><td>

External risk type

</td><td>

-   **Credit**: Credit risk is the possibility of a loss resulting from a borrower's failure to repay a loan or meet contractual obligations. For example, when lenders offer credit cards, or loans, there's a risk that the borrower might not repay the loan.
-   **Market**: Market risk is the possibility of an investor incurring losses due to factors that affect the performance of the financial markets in which the investor is involved. For example, a recession might impact the entire market.


</td></tr><tr><td>

External risk reference

</td><td>

ID for reconciliation in the book of accounts. Specify the IDs for reconciliation purposes. The credit and market risk systems are different.

</td></tr><tr><td class="sub-head" colspan="2">

Additional Classification

</td></tr><tr><td>

Used in modeling

</td><td>

Option to share these risk event records with external systems where they want to perform advanced analysis using simulation techniques such as Monte Carlo simulation.

</td></tr><tr><td>

Full rapid recovery

</td><td>

Total loss recovered. Select if the total loss is recovered within a short duration and doesn't impact the organization. **Note:** Generally, a short duration refers to five working days, but this value can be configured according to your requirements.

</td></tr><tr><td>

Financial gain

</td><td>

This option is automatically selected if the risk event meets one of the following conditions.-   Risk event is a potential event and the **Expected loss** field or the **Potential loss** field has a negative value because of the gain.
-   Risk event is an actual event and the **Net loss** field has a negative value.


</td></tr><tr><td>

Near miss

</td><td>

This option can either be modified or can be automatically set based on the event type. If the event sub type is **Actual**, and the **Full rapid recovery** option is selected, the **Near miss** option is automatically selected.

</td></tr><tr><td>

Reason for near miss

</td><td>

Reason which prevented the risk event from incurring the loss. If the event type is Potential, select the **Near miss** option and in the **Reason for near miss** field, enter the reason why the event was a near miss

</td></tr><tr><td class="sub-head" colspan="2">

Confidentiality

</td></tr><tr><td colspan="2">

**Note:** This section only appears when:

-   The **sn\_grc.enable\_record\_confidentiality** property is enabled under GRC properties.
-   The risk event is in New or Analyze state


</td></tr><tr><td>

Confidential

</td><td>

Option to mark the risk event record as confidential.

</td></tr><tr><td>

Allowed users

</td><td>

Users who can view the risk event. **Note:** By default, the risk event owner and the logged in user are added to the list of confidential users.

</td></tr><tr><td>

Allowed groups

</td><td>

Groups that can view the risk event.

</td></tr><tr><td class="sub-head" colspan="2">

Summary

</td></tr><tr><td colspan="2">

To understand how the values in this section appear, refer to the example given after this step.

</td></tr><tr><td>

Direct amount

</td><td>

The aggregated sum of all direct losses. This field is automatically set.

</td></tr><tr><td>

Additional cost

</td><td>

The aggregated sum of all additional costs. This field is automatically set.

</td></tr><tr><td>

Gross loss

</td><td>

Sum of all direct losses, indirect amounts, and additional costs. This field is automatically set.

</td></tr><tr><td>

Net loss

</td><td>

The net amount of the loss. This field is automatically set.

</td></tr><tr><td>

Indirect amount

</td><td>

The aggregated sum of all indirect losses. This field is automatically set.

</td></tr><tr><td>

Rapid recovery amount

</td><td>

The aggregated sum of the amount that was recovered rapidly. This field is automatically set.

</td></tr><tr><td>

Recovered amount

</td><td>

The amount to be recovered for the risk event. This field is automatically set.

</td></tr><tr><td>

Non financial impact

</td><td>

Impact of the event when it does not have a monetary loss. The choices are as follows:-   **None**
-   **Low**
-   **Medium**
-   **High**


</td></tr><tr><td class="sub-head" colspan="2">

Activity

</td></tr><tr><td>

Additional comments

</td><td>

Provide additional comments that you may have about the risk event.

</td></tr><tr><td>

Work notes

</td><td>

Option to provide work notes for reference. Work notes are not visible to the risk event creator.

</td></tr></tbody>
</table>    The values in the Summary section, the values in the fields are calculated in the Event Impacts related list. For example, consider that a firm has a fire outbreak. This event can result in multiple direct and indirect impacts such as loss of information and business.

    If you enter the value of a direct impact as **$2000**, then the **Direct amount** field reflects the same value. If you enter two indirect amounts, each with a value of **$300** and **$500** respectively, then the **Indirect amount** field reflects a value of **$800**.

    If an external agency is hired to address the root cause of the fire outbreak, the cost incurred reflects an additional cost.

    If the firm was able to recover a part of the cost of the event in five working days, then the **Rapid recovery amount** field reflects the same amount.

    The **Gross loss** field reflects the total loss incurred by the event.

    The currency conversion rates impact the values displayed in the Summary related list. For example, if you enter a value of **300** Japanese Yen as the recovery amount, you see the amount in the concurrent USD value of **2756** in the Summary related list. This conversion occurs because the currency conversion rates are applied from the Exchange Rate table. For more information on how the values in the exchange rate table are calculated, see [Use your own currency-conversion rates](https://www.servicenow.com/docs/access?context=t_UseYourOwnConversionTable&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

3.  To send the risk event for approval, click **Request Approval**.


**Parent Topic:**[Use Risk Events](../concept/use-risk-events.md)

