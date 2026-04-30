---
title: Configuration Compliance calculators and calculator rules
description: Configuration Compliance automate calculating initial values for the fields on test results. The condition for each calculator is evaluated in order, and the first matching calculator is used.
locale: en-US
release: zurich
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
keywords: [calculator rules for test results]
breadcrumb: [Creating Calculator group, Configure, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configuration Compliance calculators and calculator rules

Configuration Compliance automate calculating initial values for the fields on test results. The condition for each calculator is evaluated in order, and the first matching calculator is used.

## Configuration Compliance calculators

The Configuration Compliance base system includes one configuration compliance calculator \(Default Risk Calculator \) that sets the base Risk Score on the test result. Configuration Compliance calculators can be built to prioritize and rate the impact of test results based on any criteria by using condition filters. Whether it is the business impact of the vulnerability, the class of the configuration item \(CI\), you can create additional configuration compliance calculators to set other fields on test results or you can customize the existing configuration compliance calculators. A calculator can be written to reflect any set of priorities.

Each calculator contains a list of calculator rules, with a condition determining when to apply it. When the calculator is run, the condition for each calculator rule is evaluated in order, and the first matching calculator rule is used.

All enabled configuration compliance calculators set the selected fields each time a test result is created, when an associated CI or Configuration Test changes, or when the **Calculate Risk Score** related link in a test result is used. As an example, the Risk Score is automatically updated on test result records when the control.criticality value is updated on a test result that is imported. After a test result import has updated a test result score, you can recalculate the risk score of the test results by selecting the **Reapply Calculator** button.

From an existing test result, if you select the **Calculate Risk Score** related link and either of the calculators is enabled, the Risk Score field in the test result is updated.

**Note:**

-   The **Calculate Risk Score** related link is only visible when at least one configuration compliance calculator is enabled.
-   Starting from v22.0 of Vulnerability Response, you can update the risk score for a test result in the Vulnerability Manager Workspace and IT Remediation Workspace by selecting the **Calculate Risk Score** button in its record view.
-   Starting with version 14.13 of Configuration Compliance, whenever the risk score on a test result changes, the following details are documented in the Notes section of the test result:
    -   Calculator group name
    -   Calculator name: Depending on whether the calculator rule is based on a template or a script, the name is appended with the details in brackets. To modify or view the basis of the calculator rule, select any rule and select the **Advanced view** check box. From the **Value type** drop-down box, select the required option. If **Template** is selected, the risk score is updated according to the specified condition in the rule. If **Script** is selected, you can either add or update the existing script.
    -   Field values with their weightage and risk score contribution
    -   Final risk score
    -   The system property **sn\_sec\_cmn.risk\_score\_changes\_add\_worknotes** helps populate the work notes section. Starting with v15.2.1 of Configuration Compliance, the system property **sn\_sec\_cmn.risk\_score\_changes\_add\_worknotes** is inactive by default. If you enable it, only then you can see all the changes related to the risk score of a test result in the Work notes section. Additionally, the work notes are updated only if there’s a change in the risk score.

## Configuration Compliance calculator rules

By default, a base system **Default Risk Calculator** is provided. If you want to create a risk rule for this calculator, you must set the target field of **Default Risk Calculator** to **Risk Score**. Select the **New Risk Rule** button to create a new risk rule . This creates a specialized test result calculator rule called a Risk Rule, which in turn, calculates the Risk Score based on multiple values. By default, the following values for calculating risk score are considered:

-   Business Criticality
-   Criticality

You can adjust the values to use in the Default Risk Rule and how much weight to give each of these values. Weights are used to adjust how much each element counts when setting the base Risk Score.

Starting with Configuration Compliance version 13.0, you can customize the criteria for the default risk rule. For more information, see [Define fields and weights for the risk rule](../task/define-fields-weights-risk-rule.md).

## Assigning a weightage percentage

You can also assign weightage percentage \(0-100\) at the field value level. For example, you can assign a weightage percentage to each level of Severity \(None to Critical\). If the criticality weightage is 50 for the risk rule, and the following weightage values are assigned for the Criticality level:

|Criticality|Risk Score|
|-----------|----------|
|Critical|100|
|High|50|
|Medium|20|
|None|0|

If the criticality is critical, the corresponding weightage is 50. If the criticality is high, the weightage is 25, and if the criticality is medium, the weightage is 10. If the criticality is none, the corresponding weightage is 0. For more information, see the Risk score calculation example for Configuration Compliance.

Each rule has an **Order** setting however, the first one to match the conditions updates the **Risk score** field in the test result. Non-scripted calculator rules typically create less of a performance impact than scripted calculator rules.

The base system Configuration Compliance calculator contains calculator rules that assign each level of criticality \(None to Critical\) a value \(0-100\) for Risk Score based on severity. Unknown severity is automatically assigned a risk score of 100. These values can be adjusted, like Default Risk Calculator, new calculator rules or new risk rules can be created.

## Vulnerability Risk Score Weights

All vulnerabilities are assigned a risk score and rating based on factors such as severity, criticality, exploit information, and so on. The business rule **Update Risk Rating from Risk Score** on the vulnerable item table is responsible for calculating the risk rating. Whenever the risk score changes, the risk rating is calculated and populated on the vulnerable items. Prior to version 17.1 of the Vulnerability Response \(VR\) application, the following risk ratings were provided as part of script include `VulnerabilityUtils`, which were hard-coded.

|Value \(Risk Rating\)|Weight \(Risk Score\)|
|---------------------|---------------------|
|1|90–100|
|2|70–89|
|3|40–69|
|4|1–39|
|5|0|

Starting with the 18.0 version of Vulnerability Response,

-   The risk rating types are shipped in the base table as cc\_risk\_rating. These types are passed as part of the business rule on each table where the risk rating is calculated.
-   The script is modified so that you can query the entries in the Risk Score Weights table values for risk rating calculation.
-   Add additional entries for an existing type or create a new type. When you create a new type, ensure that you add the labels for the new risk rating, and also modify the related scripts and business rules. You must also add a new style for the new risk score.
-   Modify the script to query the records in the base table.

You can access the Risk Score Weights table by entering sn\_sec\_cmn\_risk\_score\_weight in the filter navigator.

In addition, the risk score is automatically recalculated in the following scenarios:

-   When a configuration item \(CI\) changes from non-internet facing to internet facing.
-   When the associated Common Vulnerabilities and Exposures \(CVEs\) or third-party entries \(TPEs\) on the vulnerability items \(VIs\) are linked to a CVE Known Exploit Vulnerability \(KEV\).

