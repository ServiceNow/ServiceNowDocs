---
title: Viewing risk intelligence scores
description: For DD requests, risk intelligence scores appear in a list. For an individual third party, a card displays the most recent score or rating and a link for each risk intelligence report.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Overview of a third party, Monitor third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Viewing risk intelligence scores

For DD requests, risk intelligence scores appear in a list. For an individual third party, a card displays the most recent score or rating and a link for each risk intelligence report.

Risk intelligence scores are described in [Integrating scores from risk intelligence providers](../../grc-vendor-risk/concept/tprm-riskintelprvdr-overview.md), [Set up a risk intelligence provider service](../../grc-vendor-risk/task/tprm-riskintelprvdr-set-up.md), and [Add a risk intelligence score to risk data for a third party](../../grc-vendor-risk/task/tprm-riskintelprvdr-add-score.md).

## Risk intelligence scores for DD requests

While viewing the data for a DD request, select the **Risk intelligence scores** tab to view the list of reports that risk intelligence providers have returned.

![All risk intelligence scores for a DD request.](../image/tprm-ws-riskintel-scores-for-dd-tab.png)

## Risk intelligence scores for a third party

While viewing the data for a third party, select the **Risk intelligence scores** tab.

The list of risk intelligence providers that have returned data for the third party includes the count of scores that were associated with the third party. Select a number to view report details.

![All risk intelligence scores for a third party.](../image/tprm-ws-riskintel-scores-for-tp-tab.png)

Each card displays the following information:

![All risk intelligence scores for a third party.](../image/tprm-ws-riskintel-card-for-tp.png)

-   A. Overall value: The most recently added overall raw score or raw rating from the provider.
-   B. Normalized risk rating. If you entered a numerical raw score or raw rating from the provider, then this is the computed normalized TPRM rating. You specified the mapping from the provider's values to the TPRM rating while configuring the provider service.
-   C. Link to the report that the provider returned for your request for a risk intelligence score.

**Related topics**  


[Add a risk intelligence score to risk data for a third party](../../grc-vendor-risk/task/tprm-riskintelprvdr-add-score.md)

[Set up a risk intelligence provider service](../../grc-vendor-risk/task/tprm-riskintelprvdr-set-up.md)

