---
title: Configuration Compliance integrations
description: Third-party integrations import configuration assessment findings, policies, tests, technologies, authoritative sources, test results along with other vulnerability data into the Configuration Compliance application.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Configuration Compliance integrations

Third-party integrations import configuration assessment findings, policies, tests, technologies, authoritative sources, test results along with other vulnerability data into the Configuration Compliance application.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

The Configuration Compliance application supports the following third-party integrations:

-   Starting with v14.11, drive remediation for security gaps in your enterprise assets identified by the Security Posture Control application by publishing findings as test results in the Configuration Compliance application. The Security Posture Control application and its supported applications are available with separate subscriptions from the ServiceNow® Store. See [Security Posture Control](../../security-posture-control/reference/spc-landing.md) for more information.
-   [Microsoft Defender for Cloud Integration for Security Operations](../../secops-integration-vr/azure-security-center/concept/cc_asc_overview.md)
-   [Palo Alto Prisma Cloud Vulnerability Integration](../../secops-integration-vr/prisma/concept/pcc-integration.md)
-   [Qualys integration with Configuration Compliance](../../secops-integration-cc/qualys/concept/Qualys-cc-Integration.md)
-   The Tenable.io product of the [Tenable Vulnerability Integration](../../secops-integration-vr/tenable/concept/tenableIntegration.md)

## Additional notes for integrations

During integration execution, multiple processes are generated, and data is received in the form of pages. Each process can contain one or more import queue entries with attached data in pages. These entries must process the data within the one-hour time limit. However, if the payload size is large, the processing time may exceed one hour or get stuck, resulting in an integration timeout error. The integration continues to process the data despite the timeout error. To avoid this miscommunication, starting from version 14.8.5 of Configuration Compliance, timestamps \(heartbeats\) are sent periodically to indicate if the queue is active and processing data. The **Last Record Processed** field in the Import Queue Entry page is updated based on the count of records the import queue creates or updates. In case an import queue entry exceeds the one-hour time limit, the system checks the **Last Record Processed** field to see if it is also older than one hour. If it is, this indicates that the import queue entry is stuck, and it is timed out to prevent any further delays in processing.

**Note:** The **Last Record Processed** field is updated based on what is defined in the following system properties:

-   **sn\_sec\_cmn.record\_threshold\_heartbeat**: Defines the number of processed records, after which the heartbeat \(timestamp\) is sent to the import queue entry.
-   **sn\_sec\_cmn.maximum\_heartbeat\_delay**: Defines the time after which the import queue entry must be timed out.

-   **[Microsoft Defender for Cloud Integration for Security Operations](../../secops-integration-vr/azure-security-center/concept/cc_asc_overview.md)**  
The Microsoft Defender for Cloud Integration product is an infrastructure security management system that enhances the security posture of your cloud environments.
-   **[Understanding the Vulnerability Response Integration with Palo Alto Prisma Cloud](../../secops-integration-vr/prisma/concept/prisma-cloud-overview.md)**  
Prisma Cloud is an API-based cloud infrastructure security solution. It connects to your cloud environment and monitors the resources deployed on the public cloud environments, such as Amazon Web Services \(AWS\), Microsoft Azure, and so on. You get complete visibility and control over risks within your public cloud infrastructure.
-   **[Qualys integration with Configuration Compliance](../../secops-integration-cc/qualys/concept/Qualys-cc-Integration.md)**  
The Qualys Policy Compliance collects the data and automatically sends it to the Qualys application, which continuously analyzes and correlates the information. It easily integrates as the Qualys Integration for Security Operations to map configuration findings to CIs and business services to determine the impact and priority of potential misconfigurations.
-   **[Understanding the Tenable Vulnerability Integration](../../secops-integration-vr/tenable/concept/tenableIntegration.md)**  
The Vulnerability Response Integration with Tenable application developed by ServiceNow engineering for the Tenable Vulnerability Integration uses data imported from the Tenable.io, Tenable.sc, and Tenable.cs products to help you prioritize and remediate vulnerabilities for your assets. The application is available with a separate subscription from the ServiceNow® Store.
-   **[Exploring the Wiz Test Results and Issues Integrations with Configuration Compliance](../../secops-integration-cc/wiz-test-results-integration/concept/exploring-wiz-ctest-results-int.md)**  
Import cloud configuration data with the Wiz Test Results and Issues Integrations with Configuration Compliance that are included with the Wiz Vulnerability Response Integration.

**Parent Topic:**[Configuration Compliance](../reference/vr-config-compliance-landing.md)

