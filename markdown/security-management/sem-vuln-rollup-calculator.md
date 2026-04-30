---
title: Vulnerability Response Rollup Calculators
description: After your initial assessment of risk calculators in the Setup Assistant, use the vulnerability rollup calculators to configure how the cumulative risk score is computed for remediation tasks and imported vulnerabilities.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Prioritizing vulnerabilities and other findings using roll-up calculators, Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Vulnerability Response Rollup Calculators

After your initial assessment of risk calculators in the Setup Assistant, use the vulnerability rollup calculators to configure how the cumulative risk score is computed for remediation tasks and imported vulnerabilities.

Use the vulnerability rollup calculators to configure how the cumulative risk score is computed for remediation tasks and imported vulnerabilities. The following rollup calculators are shipped with the base system:

-   **Remediation Task Rollup**: Rolls up the risk scores for all vulnerable items in a remediation tasks, to provide an overall risk score for the entire group of vulnerable items.
-   **Patch Update Rollup**: Rolls up the risk scores for all vulnerable items with same patch update, to provide an overall risk score for the patch update.
-   **Organization Risk Score Rollup**: Rolls up the risk scores for all host vulnerable items, application vulnerable items, container vulnerable items and configuration issues in an organization, to provide an overall risk score for the entire organization in unified dashboard.

    **Note:** Starting with v22.0 of Vulnerability Response, you can configure rollup weights for organizational score. Also, individual roll-up calculators have been removed.

-   **Vulnerable Item Rollup**: Rolls up the risk scores for all host vulnerable items in an organization, to contribute to the overall risk score of the entire organization for unified dashboard.
-   **Vulnerability Entry Rollup**: Rolls up the risk scores for all vulnerable items with the same vulnerability entry, to provide an overall risk score for the vulnerability entry.
-   **Rollup EPSS Scores from NVD to TPEs**: Rolls up the EPSS scores for all vulnerable items/ CVEs listed on the NVD table to existing TPEs, to provide an overall probability of the vulnerability being exploited.
-   **Remediation Effort Rollup**: Rolls up the risk scores for all the records in a remediation effort, to provide an overall risk score for the remediation effort.

Navigate to **All** &gt; **Vulnerability Response** &gt; **Administration** &gt; **Vulnerability Rollup Calculator**.

Configure the rollup calculator to specify how much weight to give each of those computed values in setting the cumulative risk score. The higher the weight, the more that value is used to determine the rolled up risk score in the vulnerability or remediation tasks.

**Note:** When **Include deferred** is selected, all deferred vulnerable items are included in the rollup calculation for the remediation tasks. Be sure that you understand the impact on the total calculation before selecting this option.

Rollup calculators run the scheduled job, **Rollup vulnerable item values to vulnerability and groups**, every 15 minutes to pick up changes and roll up the details and risk scores to remediation tasks and vulnerabilities. These scheduled jobs also calculate cumulative values for the number of VIs, maximum risk score, remediation target date, and status for remediation tasks.

**Note:** Calculated values for vulnerability entries do not include remediation target data.

The risk score is calculated when:

-   The risk score, remediation target, remediation status, or vulnerability changes on the vulnerable items.
-   The vulnerable item state changes to Open, Deferred, Closed, or changes from Closed or Deferred.
-   Vulnerable items are deleted.
-   Vulnerable items are added or removed from the remediation task.

Vulnerability rollup calculator example: Consider a remediation task VUL324567, which has the following vulnerable items:

-   VIT1001 with risk score of 30
-   VIT1002 with risk score of 40
-   VIT1003 with risk score of 50

Also, consider the following weights in the vulnerability rollup calculator:

-   Maximum risk score: 80
-   Average risk score: 5
-   Count of vulnerable items: 15

![Vulnerability rollup calculator example with a maximum risk score of 80, an average risk score of 5, and a count of vulnerable items of 15.](../../vulnerability-response/image/RollupCalculator.png "Vulnerability rollup calculator example")

In the Vulnerability rollup calculator example, the formula for determining the remediation task **Risk Score** is:

\(**Maximum risk score**/100\) \* 80 + \(**Average risk score** /100\) \* 5 + \(factor \* 15\)

The factor is determined as follows:

|VI count|Factor|
|--------|------|
|&lt;10|0.2|
|10-100|0.4|
|101-1000|0.6|
|1001-10000|0.8|
|&gt; 10000|1|

So, for the remediation task, VUL324567:

-   Average risk score is 40
-   Maximum risk score is 50
-   50 \(Maximum risk score\)
-   Factor is 0.2

The **Risk Score** would be 45 \[\(50/100\) \* 80 + \(40/100\) \* 5 + 0.2 \* 15 = 40 + 2 + 3 = 45\]

![EPSS rollup calculator script.](../../secops-integration-vr/epss/image/epss-rollup-calculator.png "Rollup EPSS Scores from NVDs to TPEs")

## EPSS Rollup calculator - Example

For example, consider an organization with 100 vulnerabilities, each with a 5% chance of being exploited. The question of great interest to a network defender might be: what is the probability that at least one of those vulnerabilities will be exploited, and therefore what is my overall threat? The probability of at least one event occurring is simply the complement \(opposite\) of no events occurring, that is:

```
P(at least one exploited vulnerability) = 1 - P(no vulnerabilities are exploited)
```

Where, the probability of no vulnerabilities is the linear product of each vulnerability not being exploited. In this example, since each vulnerability has a 5% chance of being exploited, they each have a 95% chance of not being exploited. And since there are 100 of them, we can write this as:

```
P(at least one vuln exploited) = 1 - P(no vulns are exploited) = 1 - P(one vuln not exploited)^100 = 1 - 0.95^100 = 0.994
```

Which says that the probability of at least one of the vulnerabilities being exploited is 99.4%.

**Important:** To modify the **Rollup EPSS Scores from NVD to TPEs**, you need to switch the Form context menu view to **Rollup Developer View** from the **Default view**.

**Parent Topic:**[Prioritizing vulnerabilities and other findings using roll-up calculators](sem-prioritizing-vulnerabilities-other-findings.md)

