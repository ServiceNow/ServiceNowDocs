---
title: Configuring Data Privacy for Now Assist
description: Configure a data privacy advanced configuration to de-identify personally identifiable information \(PII\) in generative AI applications.
locale: en-US
release: yokohama
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
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

These plugins should be installed automatically if you have the latest version of Generative AI Controller.

Role required: now\_assist\_data\_privacy\_admin

## Procedure

1.  Navigate to **All** &gt; **Data Privacy \(Classic\)** &gt; **Privacy Policy Advanced Configuration**.

    If you previously used the Sensitive Data Handler to help de-identify data for generative AI, you may already see a privacy policy configured. Your previously configured regular expressions have been migrated as part of your upgrade. If you already have a data policy for Now Assist, skip to step 6.

2.  Select **New**.

3.  Enter a name for the privacy policy.

4.  In the **Data Channel** field, select the data channel to be used, see [Contextual based discovery](contextual-based-discovery.md) for more information.

    |Channel|Description|
    |-------|-----------|
    |**Data Kit**|Data, which AI models are using for evaluation, is sanitized by discovering and de-identifying sensitive data.|
    |**Data Extraction**|Data is sanitized before being sent for model training|
    |**Now Assist**|Data is sanitized before being sent to GenAI Controller|

5.  Set **Active** to `true`, then select **Submit** to create the policy advanced configuration.

    Only one policy configuration for each data channel can be active at a time. To activate a new policy advanced configuration, you must set **Active** to `false` for all other policy configurations on that data channel.

6.  After you’re redirected to the list of policy advanced configurations, open the record you created.

    Open the existing record with the Now Assist data channel if one is already present.

7.  To add a data pattern to de-identify, select **Select Data Patterns**.

8.  To create your own data pattern, see [Configure Data Discovery patterns](../task/configure-data-discovery-patterns.md).

9.  Select your data patterns, then select **Save**.


## Result

Data caught by the regular expressions selected in the data patterns is de-identified for generative AI applications.

