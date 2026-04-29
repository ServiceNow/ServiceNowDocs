---
title: Set up a risk intelligence provider service
description: After you register a risk intelligence provider, you specify which of the provider's scoring or rating services you’ll use. You also specify how their scores or ratings map to your TPRM ratings.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Scores from risk intelligence providers, Integrate, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Set up a risk intelligence provider service

After you register a risk intelligence provider, you specify which of the provider's scoring or rating services you’ll use. You also specify how their scores or ratings map to your TPRM ratings.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer

## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Risk Intelligence Provider Setup** &gt; **Provider Services**.

    Current risk intelligence provider services appear in the Third-party Provider Services related list.

    **Note:** The list of provider services also appears as a related list while you’re registering a provider. The system auto-generates a unique name for the service by concatenating the **Provider** name and **Score type**.

    ![List of risk intelligence provider services.](../image/3rd-party-service-provider.png)

2.  Select **New** and then fill in the fields on the form.

<table id="table_dwc_zzm_pdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Provider

</td><td>

Name of the risk intelligence provider for this scoring service.

</td></tr><tr><td>

Score type

</td><td>

Each service offered by the provider returns a particular type of risk rating or score, for example, Financial risk or Security risk.

 For each provider, you define at least two services.

-   Define a service that returns the overall risk score for the third party.
-   Define a service for each additional type of score that the provider can return.
 **Important:**

-   The **Is multi-factor** setting for a provider indicates that the provider can return multiple different score types. For providers that you configure as multi-factor, you must define a service with **Score type** = **Overall Score** before you can create other services for the provider. When the provider returns an overall score, you add the data. The normalized value appears as the "Overall" value on the provider's card on the **Risk intelligence scores** tab.
-   For providers that you configure as not multi-factor, you specify only one score type. The score or rating returned by the provider is converted to the normalized TPRM score. The normalized value is also displayed as the "Overall" value on the provider's card on the **Risk intelligence scores** tab.


</td></tr><tr><td>

Name

</td><td>

Name of the provider service being set up.

 The system auto-generates a unique name for the service by concatenating the **Provider** name and **Score type**.

</td></tr><tr><td>

Risk area

</td><td>

Select the third-party risk domain associated with the score type.

 For more information, see [Define a third-party risk domain](tprm-risk-domain-define.md).

 **Note:** Risk domains are called "risk areas" in some platform applications.

</td></tr><tr><td>

Copy mapping from

</td><td>

If applicable, specify an existing service with this provider that uses identical mapping as the service that you’re configuring. -   The mappings are copied to the current record.
-   The mappings become read-only.


</td></tr></tbody>
</table>3.  Scroll to the **Mapping** area and perform one of the following actions.

    -   To map the provider ratings to the ratings used by TPRM, select the **Is rating** check box and then enter each provider rating next to its corresponding platform rating.
    -   To associate a range of provider scores with each TPRM rating, don’t select **Is rating**. Each row identifies the lowest and highest values in a rating. Enter the lowest value in the **from** column and the highest value in the **to** column.
    You must fill in at least three rows.

    -   All rows must be either ratings or ranges. A mix of the two types isn’t allowed.
    -   If there are more returned values than rows, group values in the appropriate row and separate with commas.
    ![Mapping a range of scores to each platform rating.](../image/is-not-rating.png)

4.  Select **Submit**.

    You can now specify the types of requests that you might later request from the provider.

    A request type is the name of the report available for the provider. For more information, [Set up a request type for a provider](tprm-riskintelprvdr-request-type.md).


**Parent Topic:**[Integrating scores from risk intelligence providers](../concept/tprm-riskintelprvdr-overview.md)

