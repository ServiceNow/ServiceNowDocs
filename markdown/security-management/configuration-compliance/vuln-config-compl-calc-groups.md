---
title: Configuration Compliance calculator groups
description: Configuration Compliance calculators are used to update record values when pre-defined conditions are met. The calculators are grouped based on the criteria used to determine how the records are updated.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configuration Compliance calculator groups

Configuration Compliance calculators are used to update record values when pre-defined conditions are met. The calculators are grouped based on the criteria used to determine how the records are updated.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Configuration Compliance calculator groups

From the Default Risk Calculator record, calculator rules can be applied to all affected test results and collections on-demand. Vulnerability managers may use this feature adjust their risk calculator configuration. They might experiment with several prioritization schemes early in their deployment and apply those changes on-demand to view how they impact import findings.

The Risk Score calculator group has been renamed to Risk Calculators.

Risk Score Rollup Calculators are included with Configuration Compliance. There are two types of individual rollup calculators:

-   **Configuration Test Risk Roll Up**

    Calculators that roll up risk scores for all Test Results with the same Configuration Test to provide an overall risk score for the Configuration Test. The rolled-up value is displayed in the Risk Score fields.

-   **Remediation Task Risk Score Rollup**

    These calculators roll up risk scores for all Test Results in a Remediation Task to provide an overall risk score for that remediation task. The rolled-up value is displayed in the Risk Score fields.


Both the Risk Score calculator group and Risk Score Rollup Calculators group are enabled by default.

For more information, review the following key terms for Configuration Compliance calculators:

-   **Test result**

    A test result is the outcome of the configuration test on a configuration item \(CI\) and the associated technology. Test results in Failed, error, and Unknown states identify hardware, software, and assets that are out of compliance with your policies.

-   **Remediation task**

    Test results are grouped together at the time of data import based on the pre-defined remediation task rules. These remediation tasks are similar to vulnerability groups in Vulnerability Response. Remediation Tasks organize test results into groups for bulk analysis and represent a set of items to remediate.

-   **Risk score in a test result**

    A value calculated by risk score calculators that is based on the business context of an asset and the severity of the associated test. It is the average of the business criticality of the affected asset as defined in the CMDB, and the severity of the test as communicated by the scanner.

    Each asset can have multiple services associated with it. The business criticality of an asset is determined by the service with the highest criticality.

    The calculated value is displayed in the Risk Score fields of test results. The scores display values that range from 0-100. Fields are also color-coded to provide you with the severity at-a-glance.

-   **Risk score in remediation task**

    This score is displayed on the Remediation Task record and is the rolled up value of the risk scores for all the active test results in a Remediation Task. This score changes as test results are remediated in the Remediation Task.

-   **Risk score in configuration test**

    This score is displayed on configuration tests and is the rolled up value of the risk scores for all the active test results with that configuration test. This score changes as the test results associated with this configuration test are remediated.

-   **Risk rating**

    The amount of risk a failed test result poses to your system. It is based on a range of risk scores on a 1-5 numeric scale that rates risks as Critical \(1\) to None \(5\). The score is based on a range of risk scores and is displayed in Risk Rating fields.

    |Risk rating|Risk score|
    |-----------|----------|
    |1- Critical|90 to 100|
    |2- High|70 to 89|
    |3- Medium|40 to 69|
    |4- Low|1 to 39|
    |5- None|0|

-   **Risk score rollup calculators**

    There are two types of rollup calculators:

    -   Configuration Test Risk Roll Up: These calculators roll up risk scores for all Test Results with the same Configuration Test to provide an overall risk score for the Configuration Test. The rolled-up value is displayed in the Risk Score fields. You can edit the script values for weight and score for these calculators.
    -   Remediation Task Risk Score Rollup: These calculators roll up risk scores for all Test Results in a remediation task to provide an overall risk score for that remediation task. The rolled-up value is displayed in the Risk Score fields. You can edit the script values for weight and score for these calculators. For an example of a Risk score rollup calculator and how it calculates scores, see [Risk rollup calculation example for Configuration Compliance \(prior to v15.0\)](../reference/config-compliance-risk-calculator-example.md#).
-   **Historical risk score**

    The inherent risk score across all the passed test results in a remediation task. This field displays the amount of risk that was remediated by a test group and is only displayed after a test group is in the ‘Closed’ state and the risk score is zero.


Scores are calculated whenever the risk score changes or when test results are added or removed from a remediation task.

**Note:** To work properly, this script requires the Service Mapping plugin. Service Mapping is available as a separate subscription and requires activation by ServiceNow personnel.

