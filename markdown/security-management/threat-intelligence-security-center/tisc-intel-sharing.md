---
title: Configuring Threat Intelligence External Sharing
description: Threat Intelligence external sharing in TISC outlines the guidelines and functionalities for both automated and sharing from GUI of threat intelligence within and across organizations. This feature focuses on key areas such as sharing exclusion rules, approvals, data retention, and auditing to confirm secure, compliant, and efficient intelligence sharing.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administer, Threat Intelligence Security Center, Security Operations]
---

# Configuring Threat Intelligence External Sharing

Threat Intelligence external sharing in TISC outlines the guidelines and functionalities for both automated and sharing from GUI of threat intelligence within and across organizations. This feature focuses on key areas such as sharing exclusion rules, approvals, data retention, and auditing to confirm secure, compliant, and efficient intelligence sharing.

## External Sharing of Threat Intelligence with Threat Intelligence Security Center \(TISC\)

![TISC - Threat Intelligence Sharing (external)](../image/tisc-intel-sharing-external.png)

## Key features of external sharing of threat intelligence with TISC

-   **Sharing Templates**: Templates allow control over which entities and fields are included in shared intelligence, ensuring only relevant data is disseminated.
-   **Approval Rules for Sharing**: Administrators can configure approval rules for both outbound and inbound intelligence, enabling robust management of approval workflows.
-   **Redaction Capabilities**: Analysts have the ability to redact sensitive information from shared intelligence, with easy options to toggle redaction on or off.
-   **Audit Capabilities**: Every intelligence sharing action is audited, capturing details including the sender, recipient, timestamp, and shared content to ensure full compliance and traceability.
-   **Data Retention Policies**: Shared intelligence and related audit logs are retained per compliance requirements, with defined rules for archival and destruction of various record types.
-   **TISC to TISC Exchange**: Mechanisms for efficient, bi-directional intelligence exchange between Threat Intelligence Security Center \(TISC\) instances.
-   **User and Group Management for TAXII**: Defines TAXII users and groups by managing their access to collections, and maintaining secure data exchange protocols.

-   **[Exploring Outbound Intel Sharing](tisc-outbound-intel-sharing.md)**  
Using Outbound Sharing intelligence, you can define and share what threat intelligence entities and attributes, exclusion rules, profiles and groups, and approval rules that can be shared externally and internally.
-   **[Exploring Inbound Intel Sharing](tisc-inbound-intel-sharing.md)**  
Inbound intelligence sharing in TISC allows you to create profiles of external systems or devices that can submit intelligence to it.
-   **[Exploring TAXII Outbound Server](tisc-taxii-outbound-server.md)**  
TAXII collections are logical groupings of threat intelligence data.

