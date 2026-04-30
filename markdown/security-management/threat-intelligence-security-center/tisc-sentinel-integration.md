---
title: TISC - Microsoft Sentinel integration
description: Threat Intelligence Security Center for Microsoft Sentinel offers several capabilities, including importing observables from TISC to Sentinel, enriching Sentinel incidents with details of related observables, and also allow exporting observables from Sentinel to TISC.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [TISC Security Tools integrations, TISC Integrations, Integrate Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# TISC - Microsoft Sentinel integration

Threat Intelligence Security Center for Microsoft Sentinel offers several capabilities, including importing observables from TISC to Sentinel, enriching Sentinel incidents with details of related observables, and also allow exporting observables from Sentinel to TISC.

**Note:** On Microsoft Sentinel, observables are referred as entities.

## Prerequisites

**Dependencies**

The **Threat Intelligence** solution from Microsoft Sentinel Content Hub must be installed.

<table id="table_yg1_hpw_c2c"><thead><tr><th>

Application

</th><th>

Roles and Permissions

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Microsoft Sentinel-specific roles

</td><td>

1.  Logic App Contributor
2.  Microsoft Sentinel Contributor

</td><td>

1.  To install the required playbooks on a Resource Group level.
2.  Interact with Microsoft Sentinel playbooks.

 For more information, see [Roles and Permissions](https://learn.microsoft.com/en-us/azure/sentinel/roles#roles-and-permissions-for-working-in-microsoft-sentinel) in Microsoft Sentinel.

</td></tr><tr><td>

Threat Intelligence Security Center

</td><td>

sn\_sec\_tisc.api\_azure\_sentinel\_solution

</td><td>

User configured in the TISC Custom Connector should have this role to allow access to TISC APIs.

</td></tr></tbody>
</table>-   **[TISC playbook templates](tisc-playbook-templates.md)**  
This section describes the playbook templates that are shipped with TISC Sentinel solution.

**Parent Topic:**[TISC Security Tools integrations](tisc-edr-integrations.md)

