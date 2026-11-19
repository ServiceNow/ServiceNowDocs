---
title: Configuring Data Privacy for Now Assist
description: Configure a data privacy advanced configuration to de-identify personally identifiable information \(PII\) in generative AI applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/data-privacy-classic/configure-now-assist-data-privacy.html
release: zurich
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Data Privacy for Now Assist, Data Privacy, Platform Privacy]
---

# Configuring Data Privacy for Now Assist

Configure a data privacy advanced configuration to de-identify personally identifiable information \(PII\) in generative AI applications.

## Before you begin

You must have the following applications installed on your instance:

-   Data Privacy \(Classic\) \[com.glide.data\_privacy\]
-   Data Privacy \[sn\_dp\_store\_app\]
-   Data Discovery \[sn\_data\_discovery\]
-   Data Discovery APIs\[com.glide.data\_discovery\]

Installing the latest version of the Generative AI controller will auto install the Data Privacy Store App\(sn\_dp\_store\_app\). The Data Privacy Store App will auto install the Data Discovery store app\[sn\_data\_discovery\], Data Privacy \(Classic\)\(com.glide.data\_privacy\) plug-in, and the Data Discovery APIs\[com.glide.data\_discovery\].

Role required: now\_assist\_data\_privacy\_admin

**Important:** You do not need a full active license to configure Data Privacy for Now Assist.

## Procedure

1.  Navigate to **All** &gt; **Data Privacy \(Classic\)** &gt; **Privacy Policy Advanced Configuration**.\[Omitted image "image.dpna-config"\] Alt text: The advanced policy configuration page

    If you previously used the Sensitive Data Handler to help de-identify data for generative AI, you may already see a privacy policy configured. Your previously configured regular expressions have been migrated as part of your upgrade. If you already have a data policy for Now Assist, skip to step 6.

2.  Select **New**.

3.  Enter a name for the privacy policy.

4.  In the **Data Channel** field, select the data channel to be used.

    |Channel|Description|
    |-------|-----------|
    |**Data Kit**|Data, which AI models are using for evaluation, is sanitized by discovering and de-identifying sensitive data|
    |**Data Extraction**|Data is sanitized before being sent for model training|
    |**Now Assist**|Data is sanitized before being sent to GenAI Controller|

5.  Set **Active** to `true`, then select **Submit** to create the policy advanced configuration.

    Only one policy configuration for each data channel can be active at a time. To activate a new policy advanced configuration, you must set **Active** to `false` for all other policy configurations on that data channel.

6.  After you’re redirected to the list of policy advanced configurations, open the record you created.

    Open the existing record with the Now Assist data channel if one is already present.

7.  To add a data pattern to de-identify, select **Select Data Patterns**.\[Omitted image "image.dpna-patterns"\] Alt text: The data patterns configuration panel

8.  To create your own data pattern, see [Configure Data Discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-discovery/configure-data-discovery-patterns.md).

9.  Select your data patterns, then select **Save**.


## Result

\[Omitted image "image.dpna-drilldown"\] Alt text: An advanced configuration policy with several data patterns active.

Data caught by the regular expressions selected in the data patterns is de-identified for generative AI applications. In this example policy, it is configured to catch a series of active data patterns and then use the data extraction data channel.

