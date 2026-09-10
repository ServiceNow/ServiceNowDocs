---
title: Add costs for integrated vendors
description: Define the token cost rates for integrated LLM vendors, such as Amazon Bedrock and Google Cloud Vertex AI, based on your commercial agreements.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
---

# Add costs for integrated vendors

Define the token cost rates for integrated LLM vendors, such as Amazon Bedrock and Google Cloud Vertex AI, based on your commercial agreements.

## Before you begin

Role required: AI steward \(`sn_ai_governance_ai_steward`\).

## About this task

The system automatically captures token usage from integrated LLM providers, such as Amazon Bedrock, Google Cloud AI, ServiceNow, and Microsoft. However, you must configure the cost rates for each vendor based on your specific commercial agreements.

Cost setup is a single four-step flow: configure hourly rates, add integrated vendor costs, add other vendor costs, and preview cost and savings. You can select **Save and close** at any step and come back to it later.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Settings** &gt; **Rules and Templates** &gt; **Cost**.

2.  Select **Edit configuration**.

3.  Make sure you have configured the average rate.

    For more information, see [Configure average hourly rate for your organization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mc-configure-the-average-hourly-rate-for-your-organization.md).

4.  In the **Add integrated vendor costs** section, select **Add vendor** and enter the details.

    |Field|Description|
    |-----|-----------|
    |Vendor|Name of the vendor. Only vendors that your organization has integrated with the AI Control Tower appear in the drop-down list. Available vendors typically include ServiceNow \(Creator Skills\), Anthropic, Amazon Bedrock, Google Cloud Vertex AI, and other approved partners.|
    |Cost type|Choose Overall for a single cost per token, ServiceNow Assist, or Input and output cost to add a separate per-token cost for input and output tokens.|

5.  Define the costs by using one of the two cost models.

    -   Overall cost model — For vendors that charge a blended or flat rate. Enter a single overall cost per million tokens.
    -   Input/output cost model — For most LLM vendors, such as Google and Amazon. Enter an input cost per million tokens and an output cost per million tokens. Input tokens \(prompts\) are cheaper than output tokens \(completions\) because completions require more computation.
    Add costs for all integrated vendors that your organization uses.

    Enter the amount in the cost field for the vendor, for example **Cost per million tokens**. The unit depends on the vendor and the cost type you selected: per million tokens for token-priced vendors, and per assist for ServiceNow Assist.

    Select **Add vendor**. Repeat for every integrated vendor before you continue.

    To see previous cost entries for a vendor, select **View history**.

6.  Select **Next** to continue.


## Result

All integrated LLM vendors that your organization uses are configured with their token cost rates. The Cost Framework uses these rates to automatically calculate token costs based on the token usage captured from each vendor's integration.

