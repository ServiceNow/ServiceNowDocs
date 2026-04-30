---
title: Mitigation controls and policies required for Exploit Protection \(EDR\) mitigation controls
description: This category of mitigation controls covers mitigations available on your assets in the form of endpoint protection agent configuration. This applies to endpoint protection agents such as CrowdStrike and SentinelOne.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use mitigation controls, Security Posture Control, Security Operations]
---

# Mitigation controls and policies required for Exploit Protection \(EDR\) mitigation controls

This category of mitigation controls covers mitigations available on your assets in the form of endpoint protection agent configuration. This applies to endpoint protection agents such as CrowdStrike and SentinelOne.

Exploit mitigation settings such as ‘Force Address Space Layout Randomization’ and ‘Force DEP’ can be enabled in endpoint protection tools like CrowdStrike. SPC automatically detects this configuration on devices with the help of the policies included with the application and the API integration with endpoint protection tools.

Roles required: SPC Admin Group and SPC Analyst Group.

## Prerequisites for CrowdStrike Exploit Protection \(EDR\) mitigation control detection

1.  Verify that you have activated the CrowdStrike Service Graph Connector. This application is available in the ServiceNow Store. The installation and configuration information is included on the app listing. See [Install and configure the CrowdStrike integrations for mitigation controls monitoring](../task/spc-install-config-controls.md) for more information.
2.  Verify that the CrowdStrike API integration is activated in the Security Posture Control Workspace.

## Prerequisites for Microsoft Exploit Protection \(EDR\) mitigation control detection

Microsoft SCCM credentials that include the Script Authors role. The Script Authors role provides required permissions to create a script that is required to import mitigation information on the SCCM server.

You must activate the SCCM integration to identify mitigation controls configured in Microsoft Defender.

See [Install and configure the Service Graph Connector for Microsoft SCCM and the Microsoft Defender Mitigation Control Integration](../task/spc-install-config-sccm-defender.md) for more information.

-   Defender – Exploit Mitigation – CFG

    Microsoft Defender Control Flow Guard.

-   Defender – Exploit Mitigation – DEP

    Microsoft Defender Data Execution Prevention.

-   Defender – Exploit Mitigation – Mandatory ASLR and Bottom-Up ASLR

    Microsoft Defender force ASLR.

-   MITRE tactics addressed: Initial Access, Execution, Credential Access, Defense Evasion, Privilege Escalation, Lateral Movement.

1.  Verify that you have activated the SentinelOne Service Graph Connector.

    This application is available in the ServiceNow Store. The installation and configuration information is included on the app listing. See [Install and configure the Service Graph Connector for SentinelOne and the SentinelOne Mitigation Control Integration](../task/spc-install-config-sentinelone-mc.md) for more information.

2.  Verify that the SentinelOne API integration is activated in the Security Posture Control Workspace.

