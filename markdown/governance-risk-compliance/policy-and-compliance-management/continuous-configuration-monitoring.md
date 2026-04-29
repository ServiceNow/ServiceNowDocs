---
title: Manage continuous monitoring for controls between Configuration Compliance and Policy and Compliance Management
description: Continuous monitoring for controls is a feature integration between the GRC: Policy and Compliance Management product and the Security Operations Configuration Compliance products. This feature integrates the scan results from third-party applications, like Qualys to determine the compliance status for each associated control.The compliance manager maps control objectives or controls to the configuration tests, which generate the controls, entities, and indicators associated with configuration compliance.If the configuration test scan results of the control indicate any failures, the control is marked non-compliant. If the scan results indicate the control passed, all the configuration tests, then the control is marked compliant.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Manage continuous monitoring for controls between Configuration Compliance and Policy and Compliance Management

Continuous monitoring for controls is a feature integration between the GRC: Policy and Compliance Management product and the Security Operations Configuration Compliance products. This feature integrates the scan results from third-party applications, like Qualys to determine the compliance status for each associated control.

Continuous monitoring is a pro-active security management approach. Customers monitor and validate compliance and manage risks against authority documents.

## Continuous monitoring workflow

1.  The system admin activates the Configuration Compliance and Policy and Compliance Management plugins.
2.  The compliance manager maps control objectives or controls to configuration tests, which generate controls, entities, and indicators related to those configuration tests.
3.  The integration ingests the results of the third-party configuration test scan results at defined intervals.
4.  If the configuration test scan results of the configuration tests indicate a failure, then the control is non-compliant and an issue is automatically generated.
5.  If the next scan result of the configuration test indicates that the failure has been remediated, then the control is compliant and the issue is automatically closed.

**Parent Topic:**[Policy and Compliance Management](r_PolicyComplianceMgmt.md)

## Map control objective or controls to configuration tests

The compliance manager maps control objectives or controls to the configuration tests, which generate the controls, entities, and indicators associated with configuration compliance.

### Before you begin

Role required: compliance manager

The Configuration Compliance plugin must be activated to access this feature and the **sn\_compliance.auto\_create\_profile\_and\_control** property must be set to true.

### Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Policies and Procedures** &gt; **Policies**.

2.  Open the policy record, click the Control Objectives related list, and click **Edit**.

    **Note:** The **Password** Policy is used in this example.

3.  Select each control objective to associate to the policy.

4.  Open a control objective, and click the Citations related list to view the authority document citation that is associated to this control objective.

    **Note:** The **Configure the maximum password age** control objective is used in this example.

5.  Click the Configuration Tests related list and select one of the following add options:

    -   Click **Add**
    -   Click **Add from Policies**
    -   Click **Add from Authoritative Sources**
    **Note:** The **Source** field for each configuration test identifies the third-party provider of the information.

6.  After selection, click **Add**.

    All the configuration items \(controls, entities, and indicators\) are mapped and displayed on the Configuration Tests related list. The results may take a few minutes to generate.


## Interpret configuration compliance scan results

If the configuration test scan results of the control indicate any failures, the control is marked non-compliant. If the scan results indicate the control passed, all the configuration tests, then the control is marked compliant.

### Before you begin

Role required: compliance manager

The Configuration Compliance plugin must be activated to access this feature and the **sn\_compliance.auto\_create\_profile\_and\_control** property must be set to true

### Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Policies and Procedures** &gt; **Control Objectives**.

    **Note:** The **Configure the maximum password age** policy statement is used in this example.

2.  Open the control objective record and click the Controls related list.

    11 controls were generated from the configuration compliance test scan. Each control has an associated **Profile** and because all the controls show a **Status** of **Non Compliant**, an equal number of issues have been automatically generated.

3.  Open a control record, and click the Indicator related list.

4.  Open the indicator record to see the indicator results.

    The configuration test scan results are updated at regular intervals. If the scan results indicate that the failure has been remediated, then the control is marked compliant and the issue is automatically closed.


