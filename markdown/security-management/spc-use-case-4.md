---
title: Security Posture Control use case: Detecting assets missing an endpoint management solution
description: To detect assets missing an endpoint management solution, the following pre-requisites are required.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Security Posture Control, Security Operations]
---

# Security Posture Control use case: Detecting assets missing an endpoint management solution

To detect assets missing an endpoint management solution, the following pre-requisites are required.

Depending on your use case, you can choose to activate only the required connectors.

1.  Activate at least one Service Graph Connector from the Endpoint Management category.
2.  At least one Service Graph Connector must be enabled for ONE of the following categories.
    1.  Directory Services \(Microsoft Active Directory\).
    2.  Endpoint Protection: CrowdStrike or SentinelOne.
    3.  Vulnerability Assessment: Qualys, Rapid7, or Tenable.
    4.  Configuration and Patch Management: Microsoft SCCM or IBM Bigfix.

After you verify you have met these prerequisites, you must activate the following policy, Assets missing endpoint management solution. For more information on policies, please refer to [Policies for Security Posture Control](spc-policies-overview.md).

