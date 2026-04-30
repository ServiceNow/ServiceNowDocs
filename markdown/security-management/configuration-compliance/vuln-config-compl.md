---
title: Exploring Configuration Compliance
description: Use test results obtained from third-party Secure Configuration Assessment \(SCA\) integrations to verify compliance with security or corporate policies. Identify, prioritize, and remediate non-compliant configuration items.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2025-08-08"
reading_time_minutes: 4
breadcrumb: [Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Exploring Configuration Compliance

Use test results obtained from third-party Secure Configuration Assessment \(SCA\) integrations to verify compliance with security or corporate policies. Identify, prioritize, and remediate non-compliant configuration items.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## What is Configuration Compliance

The ServiceNow® Configuration Compliance application enables you to prioritize and remediate the most critical configuration-related vulnerabilities in your environment quickly and efficiently. Configuration Compliance is available by subscription in the ServiceNow® Store.

![Configuration Compliance workflow](../image/cc-overview-image.png)

## Key features of Configuration Compliance

Use the Configuration Management Database \(CMDB\) in your ServiceNow AI Platform® to help you expose and fix your most critical configuration-related security vulnerabilities. Focus your remediation resources on activities with the greatest risk reduction. Streamline the remediation process across security, IT, and your business process stakeholders. The Configuration Compliance application includes the following key features:

-   With supported third-party integrations, automatically import policies, tests, authoritative sources, and technologies. See [Configuration Compliance integrations](vuln-config-compl-integrations.md) for more information about supported integrations.
-   Correlate policies and tests to configuration items \(assets\) to identify configuration-related vulnerabilities and help you verify that your assets are in compliance with your policies and controls.
-   Unify configuration assessment, assignment, and remediation across all of your assets.
-   Configuration scanning content can be imported from leading Secure Configuration Assessment \(SCA\) ecosystem integration applications.
-   Configuration findings, test failures, can be grouped and routed automatically based on remediation specialist skill sets and areas of responsibility. Intelligent workflows and tight integration with change management provide smooth task hand-offs between groups.
-   When used with the ServiceNow Governance, Risk, and Compliance \(GRC\) application, configuration tests in Configuration Compliance can be rolled up to their corresponding GRC controls.
-   With enhanced change management, create pre-populated change requests for IT directly from Configuration Compliance to help you with your remediation tasks that require additional resources.
-   With dashboards, view remediation status metrics on remediation task, compliance test, and policy records.

## Who uses Configuration Compliance

Configuration Compliance activities can involve many levels of management.

-   System administrators
-   Vulnerability administrators
-   Vulnerability managers
-   Vulnerability analysts
-   Compliance administrators

Configuration Compliance tasks involve the following roles.

-   sn\_vulc.admin — can read, write, delete
-   sn\_vulc.write — can read and write
-   sn\_vulc.remediation\_owner — Can read and update assigned records

    **Note:** The sn\_vulc.remediation\_owner role is also automatically assigned when any user is assigned the itil role.

-   sn\_vulc.read — can read

## Configuration Compliance and Security Operations

When the Qualys Vulnerability Integration and the Tenable Vulnerability Integration are installed, access to Vulnerability Response becomes available. You can have multiple deployments of these integrations. Data sourced from each deployment is identified and available in a single instance of GRC.

## Available versions for Xanadu

<table id="table_svr_hvj_xlb"><thead><tr><th>

Release version

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Configuration Compliance v15.0, v15.1, v15.2, v15.3, 15.4

</td><td>

[Configuration Compliance release notes](https://www.servicenow.com/docs/access?context=secops-cc-rn&version=xanadu&pubname=xanadu-release-notes&ft:locale=en-US)For compatibility information, see [KB0856498 Vulnerability Response Compatibility Matrix and Release Schema Changes](https://support.servicenow.com/kb_view.do?sysparm_article=KB0856498)

</td></tr></tbody>
</table>-   **[Configuration Compliance imported data](vuln-config-compl-policies.md)**  
The Configuration Compliance application imports policies, tests, authoritative sources, and test results from third-party integrations and stores them in modules for viewing.
-   **[CI Lookup Rules for identifying configuration items from Configuration Compliance third-party vulnerability integrations](../../security-operations-common/concept/cc-ci-identifier-rules.md)**  
When data is imported from a third-party integration, Configuration Compliance automatically uses host data to search for matches in the Configuration Management Database \(CMDB\). It does this using **CI Lookup Rules**. These rules are used to identify configuration items \(CIs\) and add them to the test result record to aid in remediation.
-   **[Creating CIs for Configuration Compliance using the Identification and Reconciliation Engine](cc-ci-creation-using-ire.md)**  
Starting with Configuration Compliance 11.1, you can create configuration items \(CIs\) in the Configuration Management Database \(CMDB\) using the Identification and Reconciliation engine \(IRE\) API. By using the IRE API to create CIs, you can prevent duplicate CIs from being created and you can reconcile CI attributes by allowing only authoritative data sources to write to CMDB.
-   **[Configuration Compliance assignment rules overview](cc-assignment-rules.md)**  
Define the criteria by which test results are automatically assigned to an assignment group for remediation.
-   **[Configuration Compliance remediation tasks and remediation task rules overview](cc-groups.md)**  
Automatically create Remediation Tasks \(RTs\) to analyze results in bulk using remediation task rules. The criteria by which groups are formed is configured so that you do not have to manually assign test results into groups.
-   **[Configuring calculator groups and calculators for Configuration Compliance](vuln-configuring-cc-calcs.md)**  
Configuration Compliance calculators are used to update record values when pre- defined conditions are met. The calculators are grouped based on the criteria used to determine how the records are updated.
-   **[Configuration Compliance Exception Management overview](cc-ex-mgmt.md)**  
When your organization can't comply with a published vulnerability management or security policy, standard, or guideline, you can request an exception. Exception management entails requesting, reviewing, approving, or rejecting exceptions for a remediation task that cannot be remediated according to the policy.
-   **[Configuration Compliance change management](cc-chng-mngment.md)**  
As an IT remediation owner, you can create and manage change requests \(CHG\) directly from remediation tasks \(RTs\) in the Configuration Compliance application.

**Parent Topic:**[Configuration Compliance](../reference/vr-config-compliance-landing.md)

