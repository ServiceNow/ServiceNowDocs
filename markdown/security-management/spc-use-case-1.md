---
title: Security Posture Control use case: Detecting assets with missing endpoint protection
description: To detect assets missing an endpoint protection agent, the following prerequisites are required. 
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Security Posture Control, Security Operations]
---

# Security Posture Control use case: Detecting assets with missing endpoint protection

To detect assets missing an endpoint protection agent, the following prerequisites are required. 

Depending on your use case, you can choose to activate only the required connectors.

1.  Activate at least one Service Graph Connector from the Endpoint Protection category.
2.  Activate at least one Service Graph Connector for ONE of the following categories.
    1.  Directory Services \(Microsoft Active Directory\).
    2.  Endpoint Management: Microsoft Intune or Jamf Device and Endpoint Management.
    3.  Configuration and Patch Management: Microsoft SCCM or IBM Bigfix.
    4.  Cloud Provider: Amazon AWS Cloud, Microsoft Azure, GCP.

        **Note:** If Cloud Discovery is activated, these service graph connector products are not required.

3.  \[Optional\] You can activate Service Graph Connectors for any of the following categories to improve overall coverage, that is, the number of assets that are reported and monitored by Security Posture Control.
    1.  Network Security 
    2.  Infrastructure Monitoring
    3.  Networking
    4.  Application Performance Monitoring .

After you verify you have met these prerequisites, you must activate the following policy, Assets missing endpoint protection   .  For more information on policies, please refer to [Policies for Security Posture Control](spc-policies-overview.md).

