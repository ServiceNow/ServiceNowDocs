---
title: Add costs for integrated vendors
description: Add the cost of a vendor or sub-vendor integrated with ServiceNow so that AI Control Tower includes it in the total Enterprise AI cost. Set a sub-vendor rate when a specific service is billed differently from the vendor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/mc-add-and-configure-costs-for-integrated-vendors.html
release: australia
topic_type: task
last_updated: "2026-10-08"
reading_time_minutes: 2
breadcrumb: [Cost, Configure, Measure AI system, Measure AI systems, AI Control Tower, Enable AI experiences]
---

# Add costs for integrated vendors

Add the cost of a vendor or sub-vendor integrated with ServiceNow so that AI Control Tower includes it in the total Enterprise AI cost. Set a sub-vendor rate when a specific service is billed differently from the vendor.

## Before you begin

Role required: AI steward \(sn\_ai\_governance.ai\_steward\).

## About this task

The system automatically captures token usage from integrated LLM providers, such as Amazon Bedrock, Google Cloud AI, ServiceNow, and Microsoft. However, you must configure the cost rates for each vendor based on your specific commercial agreements.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Settings** &gt; **Rules and Templates** &gt; **Cost**.

2.  Select **Edit configuration**.

    The Edit value and cost configuration page opens at the **Configure hourly rates** step.

3.  Verify that you have configured the average rate.

    For more information, see [Configure average hourly rate for your organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/mc-configure-the-average-hourly-rate-for-your-organization.md).

4.  Select **Next**.

    The **Add integrated vendor costs** step displays the vendors that already have costs.

5.  Select **Add vendor**.

6.  In the **Vendor** field, select a vendor or sub-vendor.

    Sub-vendors appear after their vendor name, for example, **Amazon - AWS AgentCore**. A sub-vendor rate takes precedence over its vendor's rate.

7.  In the **Cost type** field, select a cost type and enter the related values.

    |Cost type|Values to enter|
    |---------|---------------|
    |**__Overall cost__**|In **Cost per million tokens**, enter the cost for one million tokens.|
    |**__Input and output costs__**|In **Input cost \(per million tokens\)** and **Output cost \(per million tokens\)**, enter the cost for one million input tokens and one million output tokens.|
    |**__Subscription__**|In **Licensed seats**, enter the number of seats. In **Cost per seat \(per month\)**, enter the monthly cost of one seat. In **Contract start** and **Contract end**, select the contract dates.|

    **Contract start** defaults to the current date.

    For a subscription, the **Estimated monthly cost** value updates as you enter details.

8.  To include a one-time setup fee in a subscription, turn on **Add a one-time setup fee**, and then enter the fee in **One-time setup fee** and the number of months in **Amortise over \(months\)**.

    The fee is spread evenly over the number of months that you enter. The monthly amount appears after the **Amortise over \(months\)** field and is added to the estimated monthly cost.

9.  Select **Save**.

    The entry appears in the vendor list with the status **Draft**. If you added a sub-vendor, its vendor's entry shows the message **Applies only where no sub-vendor rate is set**.


## Result

The cost is saved as a draft. It's applied after you submit the configuration in the **Preview cost &amp; savings** step.

## What to do next

Select **Next** to add costs for other vendors, or continue to the **Preview cost &amp; savings** step to submit your changes.

**Related topics**  


[Cost types and sub-vendor rates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/mc-ai-cost-types-and-sub-vendor-rates.md)

[Add costs for other vendors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/mc-add-and-configure-costs-for-non-integrated-vendors.md)

[Review and submit the cost configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/mc-review-and-submit-the-cost-configuration.md)

