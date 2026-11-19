---
title: Configure Data Privacy for ServiceNow Otto
description: Configure a data privacy advanced configuration to de-identify sensitive information in AI calls \(prompts, skills, and agentic executions\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-privacy-classic/configure-now-assist-data-privacy.html
release: brazil
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Data Privacy for ServiceNow Otto, Data Privacy, Platform Privacy]
---

# Configure Data Privacy for ServiceNow Otto

Configure a data privacy advanced configuration to de-identify sensitive information in AI calls \(prompts, skills, and agentic executions\).

## Before you begin

You must have the following applications installed on your instance:

-   Data Privacy \(Classic\) \[com.glide.data\_privacy\]
-   Data Privacy \[sn\_dp\_store\_app\]
-   Data Discovery \[sn\_data\_discovery\]
-   Data Discovery APIs \[com.glide.data\_discovery\]

Installing the latest version of the  will auto-install the Data Privacy Store App \(sn\_dp\_store\_app\). The Data Privacy Store App will auto-install the Data Discovery store app \[sn\_data\_discovery\], Data Privacy \(Classic\)\(com.glide.data\_privacy\) plugin, and the Data Discovery APIs\[com.glide.data\_discovery\].

**Warning:**

Ensure that you have access to this configuration option if you are configuring regex data patterns for detection and masking. To add a Named Entity Recognition \(NER\) data pattern, you need a valid ServiceNow Vault license. You must also agree to additional terms acknowledging that the capability requires sending your data to a controlled ServiceNow environment.

Role required: now\_assist\_data\_privacy\_admin

## Procedure

1.  Navigate to **All** &gt; **Data Privacy \(Classic\)** &gt; **Privacy Policy Advanced Configuration**.

    If you previously used the Sensitive Data Handler to help de-identify data for generative AI, a privacy policy may already be configured. Your previously configured regular expressions have been migrated as part of your upgrade. If you already have a data policy for ServiceNow Otto, skip to the step for opening the existing record.

2.  Select **New**.

3.  Enter a name for the privacy policy.

4.  In the **Data Channel** field, select the data channel to be used.

<table id="choicetable_ikl_yng_b2c"><thead><tr><th align="left" id="d82765e145">

Channel

</th><th align="left" id="d82765e148">

Description

</th></tr></thead><tbody><tr><td id="d82765e154">

**Data Kit**

</td><td>

Data, which AI models are using for evaluation, is sanitized by discovering and de-identifying sensitive data Data Extraction.

</td></tr><tr><td id="d82765e163">

**Data Extraction**

</td><td>

Data is sanitized before being sent for model training.

</td></tr><tr><td id="d82765e175">

**ServiceNow Otto \(AI Inference\)

**

</td><td>

Data is sanitized before being sent from the  to the LLMs to help prevent plain text sensitive data from reaching any LLMs.

</td></tr><tr><td id="d82765e194">

**ServiceNow Otto \(Conversational\)**

</td><td>

Data is sanitized during Virtual Agent \(and Now Assist Virtual Agent\) conversations, as configured between requester and the live or virtual agent.

</td></tr></tbody>
</table>5.  Set **Active** to **true**, then select **Submit** to create the policy advanced configuration.

    Only one policy configuration for each data channel can be active at a time. To activate a new policy advanced configuration, you must set **Active** to **false** for all other policy configurations on that data channel.

6.  Open the record you created in the list of policy advanced configurations.

    Open the existing record with the ServiceNow Otto data channel if one is already present.

7.  Choose **Select Data Patterns** to add the applicable REGEX data patterns.

    **Important:**

    -   To add a Named Entity Recognition \(NER\) data pattern, you need a valid ServiceNow Vault license. You must also agree to additional terms acknowledging that the capability requires sending your data to a controlled ServiceNow environment. Check your entitlements to determine whether you have access to this capability.
    -   In addition, there are rate limits on how much data can be processed using NER data patterns for ServiceNow Otto. After you exceed these limits, any applicable REGEX-based data masking that was configured will continue to apply for all Otto prompts, skills, and agentic executions.
    When Regex patterns are selected alongside NER patterns, both configurations run on every prompt.

8.  To create your own data pattern, see [Configure Data Discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/data-discovery/configure-data-discovery-patterns.md).

9.  Select your data patterns, then select **Save**.


## Result

Data discovered by the REGEX and NER data patterns is de-identified for AI calls.

