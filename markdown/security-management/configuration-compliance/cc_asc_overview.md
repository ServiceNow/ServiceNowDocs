---
title: Microsoft Defender for Cloud Integration for Security Operations
description: The Microsoft Defender for Cloud Integration product is an infrastructure security management system that enhances the security posture of your cloud environments.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuration Compliance integrations, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Microsoft Defender for Cloud Integration for Security Operations

The Microsoft Defender for Cloud Integration product is an infrastructure security management system that enhances the security posture of your cloud environments.

Microsoft Defender for Cloud Integration for Security Operations integrates with the Configuration Compliance application to map tests to configuration items \(CIs\) to create test results. It continuously discovers new cloud resources deployed across workloads and determines whether they are configured according to security standards such as the Center for Internet Security \(CIS\).

Starting with version 2.2, Microsoft Azure Security Center is renamed to Microsoft Defender for Cloud Integration for Security Operations.

## Available versions

|Application|Version|
|-----------|-------|
|Microsoft Defender for Cloud Integration for Security Operations|2.3|
|Configuration Compliance|14.3|
|Security Support Common|13.2|
|Vulnerability Response|16.2|

## Multiple deployments of the Microsoft Defender for Cloud Platform

If you have multiple deployments of the Microsoft Defender for Cloud Platform application, you can add an integration for each deployment. Resources that are identified by multiple third-party deployments, are consolidated and reconciled with your Configuration Management Database \(CMDB\). This consolidation takes place even when scan processes overlap between the multiple deployments.

## ServiceNow Microsoft Defender for Cloud Integrations

The Microsoft Defender for Cloud Integration for Security Operations enriches the compliance data on your instance by retrieving data from Microsoft Defender for Cloud. A series of scheduled jobs invokes the integrations automatically. You can also run these scheduled jobs manually. Scheduled jobs simplify the test results remediation life cycle by keeping the instance synchronized with Microsoft Defender for Cloud.

There is a configured run-as user for each integration record, with the default value **VR.System**. This value must remain the same.

**Note:** If you do not set a valid run-as user, duplicate or multiple data retrieval attachments are created for the data source records. The number of attachments increases each time the integration is run. This increases the processing time, resulting in inconsistent transform results.

Microsoft Defender for Cloud Platform integration tasks involve the following roles.

-   sn\_vul\_asc.configure\_integration: Ability to read, write, and delete records.
-   sn\_vul\_asc.read\_integration: Ability to read records.

## Viewing the Microsoft Defender for Cloud Integrations

View the integrations by navigating to **All** &gt; **Microsoft Defender for Cloud Integration** &gt; **Integrations**.

The following integrations are included in the base system.

|Integration|Description|
|-----------|-----------|
|Policy Definition Integration|Retrieves policies and creates policy entries in your instance.|
|Assessment Metadata Integration|Retrieves assessment metadata and creates tests in your instance.|
|Compliance Standards &amp; Controls Integration|Retrieves standards and controls and creates the authorization source and citations. It then links them to the tests created.|
|Assessment Integration|Retrieves assessments and processes them in your instance. The output of this integration is test results.|

## Create CIs using the Identification and Reconciliation Engine

Use the Identification and Reconciliation Engine \(IRE\) to create CIs, when an existing CI cannot be matched with a host imported from a third-party scanner.

If a CI is not matched in the CMDB, a CI is created in the **cmdb\_ci\_cmp\_resource** class. Later, when a discovery finds the same CI, it enriches the CI or creates another one.

**Note:** Automatic reconciliation does not happen for cloud resources.

-   **[Install and configure Microsoft Defender for Cloud Integration for Security Operations](../task/cc_asc_install_configure.md)**  
Install and configure the Microsoft Defender for Cloud Integration for Security Operations, so that you can use the data that is imported from Microsoft Defender for Cloud to prioritize and remediate any misconfigurations on your assets.
-   **[Configuration Compliance imported data for Microsoft Defender for Cloud Integration](cc-asc-policies.md)**  
Configuration Compliance imports policies, tests, authoritative sources, and test results from third-party integrations and stores them in modules for viewing.

**Parent Topic:**[Configuration Compliance integrations](../../../vulnerability-config-compliance/concept/vuln-config-compl-integrations.md)

