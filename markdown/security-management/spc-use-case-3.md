---
title: Security Posture Control use case: Detecting unmanaged assets
description: This use case includes two parts, detecting assets that are missing configuration and patch management agents.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Security Posture Control, Security Operations]
---

# Security Posture Control use case: Detecting unmanaged assets

This use case includes two parts, detecting assets that are missing configuration and patch management agents.

To detect assets missing configuration and patch management tools, the following pre-requisites are required.

For each Service Graph Connector in the list, you can see if that connector is required for monitoring on-premise assets or cloud assets.

Depending on your use case, you can choose to activate only the required connectors.

1.  Activate at least one Service Graph Connector from the Configuration and Patch Management categories.
2.  At least one Service Graph Connector must be enabled for ONE of the following categories.
    1.  Directory Services \(Microsoft Active Directory\).
    2.  Endpoint Protection: CrowdStrike or SentinelOne.
    3.  Vulnerability Assessment: Qualys, Rapid7, or Tenable.
    4.  Configuration and Patch Management: Microsoft SCCM or IBM Bigfix.
3.  \[Optional\] You can activate Service Graph Connectors for any of the following categories to improve overall coverage, that is, the number of assets that are reported and monitored by Security Posture Control.
    1.  Networking.
    2.  Infrastructure Monitoring
    3.  Network Security
    4.  Application Performance Monitoring .

After you verify you have met these prerequisites, you must activate at least one of the following policies.  For any policy that starts with ‘Cloud assets’, Service Graph Connectors under the category ‘Cloud Provider’ must be enabled.   For more information on policies, please refer to [Policies for Security Posture Control](spc-policies-overview.md).

-   Assets missing configuration and patch management.
-   Cloud assets missing configuration and patch management.

