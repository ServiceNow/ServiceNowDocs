---
title: Prioritizing vulnerabilities and other findings using roll-up calculators
description: After assessing risk calculators, use the roll-up calculators to configure how the cumulative risk scores are computed for remediation tasks and other higher entities.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Prioritizing vulnerabilities and other findings using roll-up calculators

After assessing risk calculators, use the roll-up calculators to configure how the cumulative risk scores are computed for remediation tasks and other higher entities.

The base system includes the following roll-up calculators:

-   **Discovered Application Rollup Calculator**: Roll up the risk scores for all application vulnerable items with the same discovered application, to provide an overall risk score for the discovered application.
-   **Vulnerability Entry Rollup Calculator**: Roll up the risk scores for all vulnerable items with the same vulnerability entry, to provide an overall risk score for the vulnerability entry.
-   **Discovered Item Rollup Calculator**: Roll up the risk scores for all vulnerable items and test results with the same discovered item, to provide an overall risk score for the discovered items.
-   **Remediation Task Rollup Calculator**: Roll up the risk scores for all vulnerable items in a remediation task, to provide an overall risk score for the entire group of vulnerable items.
-   **Configuration Test Rollup Calculator**: Roll up the risk scores for all test results with the same configuration test, to provide an overall risk score for the configuration test.
-   **Discovered Image Rollup Calculator**: Roll up the risk scores for all container vulnerable items with the same discovered container image, to provide an overall risk score for the discovered container images.
-   **Remediation Effort Rollup Calculator**: Roll up the risk scores for all the records in a remediation effort, to provide an overall risk score for the entire effort.
-   **Container Remediation Task Calculator**: Roll up the risk scores for all container vulnerable items in a remediation task, to provide an overall risk score for the entire group of vulnerable items.
-   **Application Remediation Task Calculator**: Roll up the risk scores for all application vulnerable items in a remediation task, to provide an overall risk score for the entire group of vulnerable items.
-   **Test Results Remediation Task Calculator**: Roll up the risk scores for all test results in a remediation task, to provide an overall risk score for the entire group of vulnerable items.
-   **Organization Risk Score Rollup**: Roll up the risk scores for all vulnerable items and configuration issues in an organization, to provide an overall risk score for the entire organization for unified dashboard.
-   **Patch Update Rollup**: Rolls up the risk scores for all findings with same patch update, to provide an overall risk score for the patch update.
-   **Remediation Effort Rollup**: Provides an overall risk score for records within a remediation effort.

## Configuring roll-up calculators

When configuring a roll-up calculator, you specify the weight given to each computed value in determining the cumulative risk score. The higher the weight, the more that value influences the rolled-up risk score.

**Note:** When **All active records** is selected, all deferred findings are included in the rollup calculation for the remediation tasks. Understand the impact on the total calculation before selecting this option.

## How roll-up calculators work

Rollup calculators run a scheduled job every 15 minutes to update risk scores and other details for remediation tasks and findings. The risk score is recalculated when:

-   Findings risk scores, remediation targets, or statuses change.
-   Finding states change \(for example, Open, Deferred, Closed\).
-   Findings are added or removed from a remediation task.

## Example: Remediation Rollup Calculator

Vulnerability roll-up calculator example: Consider a remediation task VUL324567, which has the following vulnerable items:

-   VIT1001 with a risk score of 30
-   VIT1002 with a risk score of 40
-   VIT1003 with a risk score of 50

Also, consider the following weights in the vulnerability roll-up calculator:

-   Maximum risk score: 80
-   Average risk score: 5
-   Count of vulnerable items: 15

In the Vulnerability rollup calculator example, the formula for determining the remediation task **Risk Score** is:

\(**Maximum risk score** /100\) \* 80 + \(**Average risk score** /100\) \* 5 + \(factor \* 15\)

The factor is determined as follows:

|VI count|Factor|
|--------|------|
|&lt;10|0.2|
|10–100|0.4|
|101–1000|0.6|
|1001–10000|0.8|
|&gt; 10000|1|

So, for the remediation task, VUL324567:

-   The average risk score is 40
-   The maximum risk score is 50
-   50 \(Maximum risk score\)
-   The factor is 0.2

The **Risk Score** would be 45 \[\(50/100\) \* 80 + \(40/100\) \* 5 + 0.2 \* 15 = 40 + 2 + 3 = 45\]

## Organizational risk score roll-up calculations

The Organization Risk Score Rollup calculator calculates the overall risk score for an organization in the [Unified Vulnerability Response Dashboard](../../../use/dashboards/application-content-packs/vr-unified-dashboard.md) and [Cybersecurity Executive Dashboard](../../../use/dashboards/application-content-packs/vr-unified-CISO-dashboard.md). It rolls up the risk scores for host vulnerable items, application vulnerable items, container vulnerable items, and configuration issues.

To calculate the maximum risk score, the highest score among VIT, AVIT, test results, and CVIT is chosen. For example, if VITs have the highest score, that score is considered as the maximum risk score.

Once the counts of VIT, AVIT, CVIT, and test results are obtained, they’re added and normalized using a count method. The resulting risk score is then multiplied by the count weight specified in the configuration.

The same process is followed for calculating the average risk score. The risk scores for AVIT, configuration issues, test results, and other scores are summed up, and then divided by the total count to obtain the average risk score. Finally, all the risk scores are added to derive the organization risk score.

-   **[Vulnerability Response Rollup Calculators](sem-vuln-rollup-calculator.md)**  
After your initial assessment of risk calculators in the Setup Assistant, use the vulnerability rollup calculators to configure how the cumulative risk score is computed for remediation tasks and imported vulnerabilities.

**Parent Topic:**[Automating prioritization and triaging](sem-automating-prioritization-triaging.md)

**Related topics**  


[Configuring roll-up calculator rules](sem-configure-risk-rules.md#)

