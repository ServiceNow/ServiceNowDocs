---
title: Add costs for other vendors
description: Configuring costs for LLM vendors without direct integrations with the AI Control Tower requires manual input. You must manually enter token usage, direct costs, or a per-seat subscription. The AI Control Tower can then include these costs in total AI cost calculations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/mc-add-and-configure-costs-for-non-integrated-vendors.html
release: zurich
topic_type: task
last_updated: "2026-10-08"
reading_time_minutes: 3
breadcrumb: [Cost, Configure, Measure AI system, Measure AI systems, AI Control Tower, Enable AI experiences]
---

# Add costs for other vendors

Configuring costs for LLM vendors without direct integrations with the AI Control Tower requires manual input. You must manually enter token usage, direct costs, or a per-seat subscription. The AI Control Tower can then include these costs in total AI cost calculations.

## Before you begin

Role required: AI steward \(sn\_ai\_governance.ai\_steward\).

## About this task

Not all LLM vendors have direct integrations with the AI Control Tower. For vendors without integrations, you manually capture and configure their costs so that they are included in your total AI cost calculations. The following approaches are available:

-   Token-based: You enter the units consumed, and the system calculates cost based on the rate you provide.
-   Direct cost: You enter the total cost directly.
-   Subscription: Use a subscription when the vendor bills per seat.

The cost entry you add stays in draft until you submit the configuration in the **Preview cost &amp; savings** step.

Cost setup is a single four-step flow: configure hourly rates, add integrated vendor costs, add other vendor costs, and preview cost and savings. You can select **Save and close** at any step and return to it later.

This step is optional. If every vendor you use is integrated, select **Next** and move on.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Settings** &gt; **Rules and Templates** &gt; **Cost**.

2.  Navigate to **Settings** &gt; **Rules and Templates** &gt; **Cost**.

3.  Select **Edit configuration**.

    The Edit value and cost configuration page opens at the **Configure hourly rates** step.

4.  Confirm that the average rate is configured.

    For more information, see [Configure average hourly rate for your organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mc-configure-the-average-hourly-rate-for-your-organization.md).

5.  Select **Next** until the **Add other vendor costs** step opens.

6.  In the **Add other vendor costs** section, select **Add vendors** and choose an approach.

    -   Token-based — Track token usage for the vendor and let the system calculate cost from the rate.
    -   Direct cost — Enter the total cost for the vendor for a time period.
    -   Subscription — Use a subscription when the vendor bills per seat.
7.  For a token-based vendor, enter the details.

    |Field|Description|
    |-----|-----------|
    |Start date|Start date for calculating the vendor cost.|
    |End date|End date for calculating the vendor cost.|
    |Vendor|Name of the vendor.|
    |Unit type|Choose Assist or Tokens according to the consumed category of cost.|
    |Cost type|Choose Overall for a single cost per token, ServiceNow Assist, or Input and output cost to add a separate per-token cost for input and output tokens.|
    |Units consumed|Total number of units consumed.|
    |Avg cost per million units|Average cost per million units within the selected time period.|

8.  For a direct-cost vendor, enter the details.

    |Field|Description|
    |-----|-----------|
    |Start date|Start date for calculating the vendor cost.|
    |End date|End date for calculating the vendor cost.|
    |Vendor|Name of the vendor.|
    |Unit type|Choose Assist or Tokens according to the consumed category of cost.|
    |Total cost|Total cost within the selected time period.|

    Add costs for all non-integrated vendors that your organization uses.

    Select **Add vendor** to save each entry, and then continue.

9.  For a subscription vendor, enter the details.

<table id="table_hdh_lrh_rkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Contract start

</td><td>

Select the contract start date.The contract start date defaults to the current date.

</td></tr><tr><td>

Contract end

</td><td>

Select the contract end date.

</td></tr><tr><td>

Vendor

</td><td>

Select a vendor or sub-vendor.

</td></tr><tr><td>

Licensed seats

</td><td>

Enter the number of seats.

</td></tr><tr><td>

Cost per seat \(per month\)

</td><td>

Enter the monthly cost of one seat.The **Estimated monthly cost** value updates to the number of seats multiplied by the cost per seat.

</td></tr><tr><td>

Add a one-time setup fee

</td><td>

Turn on **Add a one-time setup fee** toggle, and then enter the fee amount in **One-time setup fee** and specify the duration in **Amortise over \(months\)**.

</td></tr></tbody>
</table>    Select **Add vendor** to save each entry, and then continue.

    The subscription is saved as a draft. It's applied after you submit the configuration in the **Preview cost &amp; savings** step.

10. Select **Next** to continue, or **Save and close** to complete the configuration later.


## Result

All non-integrated vendors that your organization uses are configured in the Cost Framework. The AI Control Tower uses these rates for total AI cost calculations, even though the vendors don't have automatic data integrations.

