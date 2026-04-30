---
title: View detected mitigations
description: You must activate policies before you can view which threats to your assets are mitigated by available mitigation controls.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use mitigation controls, Security Posture Control, Security Operations]
---

# View detected mitigations

You must activate policies before you can view which threats to your assets are mitigated by available mitigation controls.

## Before you begin

Verify you have completed the requirements listed in [Install and configure the CrowdStrike integrations for mitigation controls monitoring](spc-install-config-controls.md), [Install and configure the Service Graph Connector for Microsoft SCCM and the Microsoft Defender Mitigation Control Integration](spc-install-config-sccm-defender.md) and [Configure the F5 BIG-IP integrations for mitigation controls monitoring](spc-install-config-f5-controls.md).

Roles required: SPC Admin Group and SPC Analyst Group.

## Procedure

1.  To view assets with mitigations detected by Security Posture Control with the ‘Assets with MITRE mitigations’ widget on the dashboard, follow these steps.

    1.  Navigate to **Workspaces** &gt; **Security Posture Control** &gt; **Home**.

    2.  Under the Key insights section, review the Assets with MITRE mitigations widget.

    3.  Select a mitigation category, **Exploit Protection \(EDR\)** or **Exploit Protection \(WAF\)** in the widget.

    4.  You can see the list of assets with mitigations detected in that mitigation category.

    5.  Select an asset.

    6.  Select the **Mitigation controls** tab to see the details of the mitigation control detected.

    7.  Select the **Mitigated vulnerable items** tab to see the list of vulnerable items mitigated by this mitigation control.

        **Note:** For this tab to be populated, the Vulnerability Response application must be installed and activated.


