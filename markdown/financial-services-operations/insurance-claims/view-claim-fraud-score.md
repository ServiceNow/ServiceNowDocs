---
title: Generate and view a claim's fraud score
description: Generate a fraud score, and view the fraud score page to get detailed insight into a claim's fraud score and history.
locale: en-US
release: australia
product: Insurance Claims
classification: insurance-claims
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Commercial Lines Claims, Claims applications, Insurance applications, Financial Services Operations \(FSO\)]
---

# Generate and view a claim's fraud score

Generate a fraud score, and view the fraud score page to get detailed insight into a claim's fraud score and history.

An adjuster, processor, and manager can generate a fraud score and view the fraud score page on a claim case and from an adjuster task to determine fraud risk of a case. Admins can use the baseline fraud score page to create a customized scoring page specific to requirements for your line of business.

**Note:** For more information, see [Configure the fraud score ranges with UI Builder](../../fso-friss-spoke/task/configure-ranges-for-scores.md).

## Generating and accessing fraud score details

If you're a claims manager, adjuster, or processor for a company, you can generate and access claim fraud score details by using Financial Services Operations Integration with FRISS. This option is only available on claim case records and adjuster task records.

From a claim case record or adjuster task record:

-   Select the Fraud score tab to view the fraud score page.
-   Select **Regenerate fraud score** to generate or regenerate a fraud score.

## Fraud score page

In the claim or from an adjuster task, you can see information about fraud scores on the **Fraud score** tab.

The following example shows the fraud score page for the Personal Lines Claims application with score details.

![Fraud score information in the Adjuster Workspace showing Score gauge, indicators, score history trend chart and history.](../../fso-personal-lines-claims/image/fraud-page-personal-regenerate-button.png "Fraud score page")

## Fraud score page details

-   **Score gauge**

    Shows a high, average, or low risk score based on the passed claim data. You can configure the display by defining the ranges for high, average, or low scores. For more information on how to configure the ranges, see [Configure the fraud score ranges with UI Builder](../../fso-friss-spoke/task/configure-ranges-for-scores.md).

-   **Fraud score**

    Overall fraud score number.

-   **Score trend**

    Displays the difference between the current and the previous score.

-   **Service provider**

    Shows the name of the fraud data analysis service provider.

-   **Screening date**

    Refers to the date that a claim was screened for fraud detection.

-   **Indicators contributing to the fraud score**

    If FRISS is enabled, displays a list of indicators such as Claim Date Check and Police report that factor into the fraud score, with accompanying scores and rationales for why each score was specified for the indicator. For more information about FRISS, see [Financial Services Operations Integration with FRISS](../../fso-friss-spoke/concept/fso-integration-with-friss-overview.md).

-   **Score history trend**

    Displays a visual chart of score history over time by screening date.

-   **Score history**

    Displays the number of times that the API is executed for the claim case. Lists scores with screening dates, rationale for screening requests, and screening requestors. You can select to filter and refresh history on demand.


