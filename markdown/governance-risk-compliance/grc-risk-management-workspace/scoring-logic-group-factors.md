---
title: Scoring logic for predefined formulas for group factors
description: Group factors have multiple predefined formulae and each of them has a specific contribution to the scoring logic.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a group factor, Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Scoring logic for predefined formulas for group factors

Group factors have multiple predefined formulae and each of them has a specific contribution to the scoring logic.

## Predefined formulae scoring logic

Users can select one of the following predefined formulae to calculate the scoring for group factors. The scores are contributed by scores of manual factors that comprise a group factor and have factor contribution as Qualitative or Quantitative, or Both.

The qualitative scores calculated using the predefined formulae are transformed using the transformation criteria if the **Transform qualitative score** option is selected for the group factor.

The qualitative scores calculated after transformation will be derived using the Qualitative weighting of the group factor. For example, if the calculated score is 10 and the Qualitative weighting is 50%, then the final score for group factor will be calculated as 10 x 0.5 = 5.

-   **Sum**

    For Qualitative, this formula adds up the qualitative scores in an assessment instance. The scores are contributed by scores of manual factors that comprise a group factor and have factor contribution as either Quantitative or Both.

    For Quantitative, this formula adds up the quantitative scores in an assessment instance. The scores are contributed by scores of manual factors that comprise a group factor and have factor contribution as either Quantitative or Both.

-   **Minimum**

    For Qualitative, this formula takes the minimum of qualitative scores in an assessment instance. The scores are contributed by scores of manual factors that comprise a group factor and have factor contribution as either Quantitative or Both.

    For Quantitative, this formula takes the minimum of quantitative scores in an assessment instance. The scores are contributed by scores corresponding to the factors that a comprise a group factor and have factor contribution of either Quantitative or Both.

-   **Maximum**

    For Qualitative, this formula takes the maximum of qualitative scores in an assessment instance. The scores are contributed by scores corresponding to the factors that a comprise a group factor and have factor contribution of either Qualitative or Both.

    For Quantitative, this formula takes the maximum of quantitative scores in an assessment instance. The scores are contributed by scores corresponding to the factors that a comprise a group factor and have factor contribution of either Quantitative or Both.

-   **Average**

    For Qualitative, this formula takes the average of qualitative scores in an assessment instance. The scores are contributed by scores corresponding to the factors that a comprise a group factor and have factor contribution of either Qualitative or Both.

    For Quantitative, this formula takes the average of quantitative scores in an assessment instance. The scores are contributed by scores corresponding to the factors that a comprise a group factor and have factor contribution of either Quantitative or Both.

-   **Product**

    For Qualitative, this formula multiplies qualitative scores in an assessment instance. The scores are contributed by scores corresponding to the factors that a comprise a group factor and have factor contribution of either Qualitative or Both.

    For Quantitative, this formula multiplies quantitative scores in an assessment instance. The scores are contributed by scores corresponding to the factors that a comprise a group factor and have factor contribution of either Quantitative or Both.

-   **Weighted average**

    For Qualitative, this formula divides the sum of qualitative scores in an assessment instance by the sum of weights. The scores are contributed by scores corresponding to the factors that a comprise a group factor and have factor contribution of either Qualitative or Both.


**Parent Topic:**[Create a group factor](../task/define-group-factor.md)

