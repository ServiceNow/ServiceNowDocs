---
title: Edit risk rollup calculators for Configuration Compliance
description: Edit an existing risk rollup calculator.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Calculator rules, Creating Calculator group, Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Edit risk rollup calculators for Configuration Compliance

Edit an existing risk rollup calculator.

## Before you begin

Role required: Role required: sn\_vulc.admin

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** and select **Risk Score Rollup Calculators**.

2.  With the list of Risk Score Rollup Calculators displayed, click a calculator to open the record and edit the form.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the Configuration Test or Remediation Task rollup calculator.|
    |Description|A description for the risk rollup calculator.|
    |Table|Table on which the rollup calculator is applied.|
    |Include deferral|Includes deferred test results during rollup of risk score.|

3.  Define the weightages in one of the following ways:

    -   In the Rollup Weights section, assign weightages for the following:

        |Field|Description|Default weight|
        |-----|-----------|--------------|
        |Maximum risk score|Maximum risk score of the test results considered.|85|
        |Average risk score|Aggregate of the risk scores of all the test results considered.|0|
        |Count of test results|Number of test results.|15|

    -   Select the **Advanced view** check box, and in the **Script values** editor, edit the values in the script as required.

        **Note:** Editing script requires advanced knowledge of the ServiceNow AI Platform and the Configuration Compliance application.

4.  Click **Update** to save your edits.

    Rollup calculators are scheduled jobs that run hourly to pick up changes. These scheduled jobs also overall risk scores for configuration tests and remediation task. The rolled-up values are displayed in the Risk Score fields.

    For an example of how a risk rollup calculator determines scores, see [Risk rollup calculation example for Configuration Compliance \(prior to v15.0\)](../reference/config-compliance-risk-calculator-example.md#).


