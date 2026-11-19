---
title: Configuring Data Privacy for ServiceNow Otto
description: Configure a data privacy advanced configuration to de-identify personally identifiable information \(PII\) in AI calls \(prompts, skills, and agentic executions\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/data-privacy-classic/configure-now-assist-data-privacy.html
release: australia
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Data Privacy for ServiceNow Otto, Data Privacy, Platform Privacy]
---

# Configuring Data Privacy for ServiceNow Otto

Configure a data privacy advanced configuration to de-identify personally identifiable information \(PII\) in AI calls \(prompts, skills, and agentic executions\).

## Before you begin

You must have the following applications installed on your instance:

-   Data Privacy \(Classic\) \[com.glide.data\_privacy\]
-   Data Privacy \[sn\_dp\_store\_app\]
-   Data Discovery \[sn\_data\_discovery\]
-   Data Discovery APIs\[com.glide.data\_discovery\]

**Important:** To enable the NER capability, you need to create the following property and set it to true: com.glide.data\_privacy.include\_channel\_for\_ner\_usage.

Installing the latest version of the Generative AI controller will auto install the Data Privacy Store App\(sn\_dp\_store\_app\). The Data Privacy Store App will auto install the Data Discovery store app\[sn\_data\_discovery\], Data Privacy \(Classic\)\(com.glide.data\_privacy\) plug-in, and the Data Discovery APIs\[com.glide.data\_discovery\].

Role required: now\_assist\_data\_privacy\_admin

**Important:**

-   You do not need a full active license to configure Data Privacy for ServiceNow Otto.
-   You do not need a valid ServiceNow Vault license to configure Data Privacy for ServiceNow Otto if you are configuring REGEX data patterns for detection and masking.

## Procedure

1.  Navigate to **All** &gt; **Data Privacy \(Classic\)** &gt; **Privacy Policy Advanced Configuration**.

    If you previously used the Sensitive Data Handler to help de-identify data for generative AI, you may already see a privacy policy configured. Your previously configured regular expressions have been migrated as part of your upgrade. If you already have a data policy for ServiceNow Otto, skip to step 6.

2.  Select **New**.

3.  Enter a name for the privacy policy.

4.  In the **Data Channel** field, select the data channel to be used.

<table id="choicetable_ikl_yng_b2c"><thead><tr><th align="left" id="d79608e157">

Channel

</th><th align="left" id="d79608e160">

Description

</th></tr></thead><tbody><tr><td id="d79608e166">

**Data Kit**

</td><td>

Data, which AI models are using for evaluation, is sanitized by discovering and de-identifying sensitive data

</td></tr><tr><td id="d79608e175">

**Data Extraction**

</td><td>

Data is sanitized before being sent for model training

</td></tr><tr><td id="d79608e184">

**Now Assist**

</td><td>

Data is sanitized before being sent to GenAI Controller

</td></tr><tr><td id="d79608e194">

**Virtual Agent**

</td><td>

Data is sanitized during Virtual Agent \(and Now Assist Virtual Agent\) conversations as configured between requester and live or virtual agent.

</td></tr></tbody>
</table>5.  Set **Active** to `true`, then select **Submit** to create the policy advanced configuration.

    Only one policy configuration for each data channel can be active at a time. To activate a new policy advanced configuration, you must set **Active** to `false` for all other policy configurations on that data channel.

6.  After you’re redirected to the list of policy advanced configurations, open the record you created.

    Open the existing record with the ServiceNow Otto data channel if one is already present.

7.  To add a data pattern to de-identify, select **Select Data Patterns**.

    **Warning:**

    -   To add a Named Entity Recognition \(NER\) data pattern, you need a valid ServiceNow Vault license. You also need to agree to additional terms acknowledging that the capability requires sending your data to a controlled ServiceNow environment. Contact your account and support teams to enable a $0 SKU containing additional terms to enable NER data patterns.
    -   In addition, there are rate limits on how much data can be processed using NER data patterns for ServiceNow Otto. Once these limits are exceeded, any applicable regex-based data masking that was configured will continue to apply for all Otto prompts, skills, and agentic executions.
    When Regex patterns are selected alongside NER patterns, both configurations run on every prompt.

8.  To create your own data pattern, see [Configure Data Discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/data-discovery/configure-data-discovery-patterns.md).

9.  Select your data patterns, then select **Save**.


## Result

Data caught by the regular expressions selected in the data patterns is de-identified for generative AI applications. In this example policy, it is configured to catch a series of active data patterns and then use the data extraction data channel.

