---
title: Add costs for other vendors
description: Configure costs for LLM vendors without direct integrations with the AI Control Tower. You can do this by manually entering token usage or a direct cost. This will ensure they are included in your total AI cost calculations.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
---

# Add costs for other vendors

Configure costs for LLM vendors without direct integrations with the AI Control Tower. You can do this by manually entering token usage or a direct cost. This will ensure they are included in your total AI cost calculations.

## Before you begin

Role required: AI steward \(`sn_ai_governance_ai_steward`\).

## About this task

Not all LLM vendors have direct integrations with the AI Control Tower. For vendors without integrations, you manually capture and configure their costs so that they are included in your total AI cost calculations. Two approaches are available:

-   Token-based: You enter the units consumed, and the system calculates cost based on the rate you provide.
-   Direct cost: You enter the total cost directly \(the simplest option\).

Cost setup is a single four-step flow: configure hourly rates, add integrated vendor costs, add other vendor costs, and preview cost and savings. You can select **Save and close** at any step and come back to it later.

This step is optional. If every vendor you use is integrated, select **Next** and move on.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Settings** &gt; **Rules and Templates** &gt; **Cost**.

2.  Navigate to **Settings** &gt; **Rules and Templates** &gt; **Cost**.

3.  Select **Edit configuration**.

4.  Make sure you have configured the average rate.

    For more information, see [Configure average hourly rate for your organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mc-configure-the-average-hourly-rate-for-your-organization.md).

5.  In the **Add other vendor costs** section, select **Add vendors** and choose an approach.

    -   Token-based — Track token usage for the vendor and let the system calculate cost from the rate.
    -   Direct cost — Enter the total cost for the vendor for a time period.
6.  For a token-based vendor, enter the details.

    |Field|Description|
    |-----|-----------|
    |Start date|Start date for calculating the vendor cost.|
    |End date|End date for calculating the vendor cost.|
    |Vendor|Name of the vendor.|
    |Unit type|Choose Assist or Tokens according to the consumed category of cost.|
    |Cost type|Choose Overall for a single cost per token, ServiceNow Assist, or Input and output cost to add a separate per-token cost for input and output tokens.|
    |Units consumed|Total number of units consumed.|
    |Avg cost per million units|Average cost per million units within the selected time period.|

7.  For a direct-cost vendor, enter the details.

    |Field|Description|
    |-----|-----------|
    |Start date|Start date for calculating the vendor cost.|
    |End date|End date for calculating the vendor cost.|
    |Vendor|Name of the vendor.|
    |Unit type|Choose Assist or Tokens according to the consumed category of cost.|
    |Total cost|Total cost within the selected time period.|

    Add costs for all non-integrated vendors that your organization uses.

    Select **Add vendor** to save each entry, and then continue.

8.  Select **Next** to continue, or **Save and close** to complete the configuration later.


## Result

All non-integrated vendors that your organization uses are now configured in the Cost Framework. The AI Control Tower uses these rates for total AI cost calculations, even though the vendors don't have automatic data integrations.

