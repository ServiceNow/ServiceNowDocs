---
title: Exploring Configuration Compliance
description: Use test results obtained from third-party Secure Configuration Assessment \(SCA\) integrations to verify compliance with security or corporate policies. Identify, prioritize, and remediate non-compliant configuration items.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
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

## Available versions for Australia

<table id="table_svr_hvj_xlb"><thead><tr><th>

Release version

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

If you intend to upgrade to a version that is compatible with Unified Security Exposure Management \(USEM\), please select a version starting with 30.x when installing or upgrading.

</td><td>

[Configuration Compliance release notes](https://www.servicenow.com/docs/access?context=secops-cc-rn&version=australia&pubname=australia-release-notes&ft:locale=en-US).For compatibility information, see [KB0856498 Vulnerability Response Compatibility Matrix and Release Schema Changes](https://support.servicenow.com/kb_view.do?sysparm_article=KB0856498)

See [Setting up, installing, and configuring the Configuration Compliance application](cc-configuring.md) for more information about activating the application.

</td></tr><tr><td>

If you do not intend to upgrade to a version that is compatible with Unified Security Exposure Management \(USEM\), please select a version below 30.x when installing or upgrading.

</td><td>

 

</td></tr></tbody>
</table>