---
title: Using mitigation controls monitoring with Security Posture Control
description: From within in the Security Posture Control \(SPC\) Workspace, gain insight into which threats to your assets are mitigated by available mitigation controls based on how various security tools are configured.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Security Posture Control, Security Operations]
---

# Using mitigation controls monitoring with Security Posture Control

From within in the Security Posture Control \(SPC\) Workspace, gain insight into which threats to your assets are mitigated by available mitigation controls based on how various security tools are configured.

## Mitigation controls monitoring

For supported applications for Security Posture Control and Mitigation Controls Monitoring, see [Exploring Security Posture Control](spc-overview.md).

The Security Posture Control application focuses on three core problem areas:

-   Asset inventory - Identifying all your enterprise assets that include unmanaged or unknown assets.
-   Security controls coverage and health - Identifying any coverage gaps with your security controls
-   Vulnerability and threat mitigation visibility - Identifying which threats or vulnerabilities to your assets are mitigated by applicable mitigation controls.

Mitigation controls monitoring describes the features in Security Posture Control that fall under vulnerability and threat mitigation visibility.

Roles required:

-   admin - Installs applications from the ServiceNow® Store and activates plugins \(ITOM Discovery\).
-   SPC Admin Group and SPC Analyst Group - Users in this group have full read and write access to all the records for the product and the workspace.
-   SPC Analyst Read Only Group - Users in this group have full read access to all the records for the product.

## Mitigation controls monitoring users and benefits

<table id="table_pss_ygt_pcc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cybersecurity teams, Security analysts and managers

</td><td>

-   Gain visibility into all your enterprise assets that include unmanaged or unknown assets.
-   Identify coverage gaps with your security controls, toxic combinations of problems such as critical vulnerabilities and internet exposure on your assets, and deviations from your internal security standards.

</td></tr><tr><td>

Vulnerability management teams

</td><td>

Gain insights in mitigations available for vulnerabilities on the assets and dynamically adjust risk score for those vulnerabilities.

</td></tr><tr><td>

Threat defense teams

</td><td>

Gain insights into gaps in mitigations or security controls configuration against specific attack techniques.

</td></tr></tbody>
</table>## Security Posture Control and the mitigation controls monitoring workflow

Security Posture Control uses API integrations with security tools such as web-application-firewalls and endpoint protection tools to import additional configuration data about your assets and analyze it to identify the applicable mitigation controls for a given asset. These API integrations are separate from the service graph connector integrations that are supported by SPC and import different data. You configure these API integrations from within the SPC Workspace.

Service graph connector integrations or ITOM Discovery are still required for mitigation controls monitoring. For example, both the CrowdStrike Service Graph Connector and the CrowdStrike API integration supported by SPC must be activated to import additional insights about which mitigation controls are enabled by the CrowdStrike endpoint protection configuration.

