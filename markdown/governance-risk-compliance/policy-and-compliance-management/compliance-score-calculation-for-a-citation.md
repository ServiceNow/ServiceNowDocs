---
title: Compliance score calculation for a citation
description: Two methodologies determine a citation's compliance score. The previous method averaged child citations and associated control objectives. The current method averages child citations and directly linked controls.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2025-11-17"
reading_time_minutes: 2
breadcrumb: [Association of citations to controls, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Compliance score calculation for a citation

Two methodologies determine a citation's compliance score. The previous method averaged child citations and associated control objectives. The current method averages child citations and directly linked controls.

## Old formula \(before enabling property\)

```
Compliance Score for a Citation = Average(Child Citations + Associated Control Objectives)

```

Under the old calculation method, a citation’s compliance score is based on the following factors:

-   The compliance scores of its child citations
-   The compliance scores of its associated control objectives.

Example 1:

-   If a citation has no child citations and is associated with one control objective that has a compliance score of 42%, then the citation’s compliance score is 42%.
-   The control objective’s score \(42%\) comes from averaging its own controls \(50%\) and its child control objective’s score \(33%\).

Example 2:

-   If a citation has one child citation with a compliance score of 70% and one associated control objective with a compliance score of 42%, then the compliance score is 56%, which comes from averaging 70% and 42%.
-   ```
Compliance Score = (70% + 40%) ÷ 2 = 56%

```


## New formula \(after enabling property\)

```
Compliance Score for a Citation = 
(Average of child citations + Average of directly linked Controls) ÷ 2

```

With the new feature enabled, the compliance score calculation changes significantly:

-   Control objective scores are no longer used.
-   Instead, the calculation considers the compliance scores of directly linked controls \(Level 1 controls\).

    **Note:** Level 1 controls are the controls of the control objectives directly associated with the citation.


Example:

If a citation has one child citation with a compliance score of 70% and four directly linked controls with compliance statuses of 100%, 0%, 100%, and 0%, then average compliance score for controls is as follows:

```
Average compliance score for controls = 
(100% + 0% + 100% + 0%) ÷ 4 = 50%
```

Compliance score = 70% + 50%​ = 60%.

## Weighted control average

When the Use weighted control average when calculating compliance scores property is enabled, the compliance score of a citation changes.

For example, consider the following scenario:

1.  Controls associated to the citation through one control objective: 3
2.  The status of the controls: 1 compliant, 2 non-compliant
3.  The weights of each control:
    -   Control A \(Compliant\) → **100**
    -   Control B \(Non-compliant\) → **10**
    -   Control C \(Non-compliant\) → **10**

If you consider flat average, the compliance score is 33%.

```
Compliance score = (100% + 0% + 0%) ÷ 3 = 33%
```

If you consider weighted average, the compliance score is 83.3%.

```
Compliance score = (Sum of weights of compliant controls X 100) 
÷ Sum of weights of all the controls
So Compliance score = (100 X 100) ÷ 120 = 83.3%
```

