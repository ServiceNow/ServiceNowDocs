---
title: Hardware Vulnerability Assessment
description: The Hardware Vulnerability Assessment \(HVA\) is available in the Industrial Workspace menu for users who are using the Operational Technology Vulnerability Response Pro.
locale: en-US
release: xanadu
product: Industrial Workspace
classification: industrial-workspace
topic_type: concept
last_updated: "2024-12-18"
reading_time_minutes: 3
breadcrumb: [Explore, Industrial Workspace, Operational Technology]
---

# Hardware Vulnerability Assessment

The Hardware Vulnerability Assessment \(HVA\) is available in the Industrial Workspace menu for users who are using the Operational Technology Vulnerability Response Pro.

## Hardware Vulnerability Assessment overview

You can use Hardware Vulnerability Assessment to assess the firmware vulnerabilities of the OT devices in inventory and create vulnerable items \(VIT\) against the impacted OT devices.

HVA uses normalized content for firmware discovery model and Common Platform Enumeration \(CPE\) format provided by the National Vulnerability Database \(NVD\) to perform assessments. The normalized content contains OT device data, such as manufacturer, firmware version, and product model. It's based on the normalization process available in the Enterprise Asset Management. The normalized content for OT devices is mapped with the Common Vulnerabilities and Exposures \(CVEs\) available in NVD. The **Hardware Vulnerability Assessment** menu displays the OT devices that are at risk, when the CVE data matches the OT device data available in the normalized content.

You must perform the following scheduled jobs to perform hardware vulnerability assessment automatically and periodically:

-   **Hardware Vulnerability Assessment - Full**
-   **Hardware Vulnerability Assessment - Delta**

## Required Operational Technology and Hardware Vulnerability Assessment roles

You need the following roles to use the Hardware Vulnerability Assessment \(HVA\) menu:

-   sn\_vul.manage\_exposure\_assessment: Assign roles to admin users or user groups as needed, which enables them to view or edit properties for Hardware Vulnerability Assessment.
-   sn\_otvr.vul\_event\_manager \(OT Vulnerability Event Manager\): Assign roles to Hardware Vulnerability Analyst users  or user groups as needed, which enables them to view assessment records and act accordingly.

## Use Case

OT hardware vulnerability analysts can use HVA to:

-   Identify cybersecurity risks in OT devices.
-   Focus on high-risk vulnerabilities via fully match assessments on OT device data.
-   Set up automatic creation of vulnerable items for fully matched assessments.
-   Investigate and address partially matched assessments to identify potential risks and act accordingly.
-   Monitor unprocessed OT devices from **Awaiting Normalization** tab, which are pending full discovery or pending content updates.

## HVA tabs

The HVA menu displays hardware vulnerability assessment records created for the OT devices. These assessment records are created based on many criteria. For example, CVE vulnerability, OT device at risk, Common Vulnerability Scoring System \(CVSS\) score, and Device Criticality.

-   The **Fully matched assessments** tab displays the assessment records, where the CVEs fully match with the manufacturer, product model, and firmware version of the OT devices. A fully matched assessment means that an OT device matches all vulnerability factors specified in a CVE.
-   The **Partially matched assessments** tab displays the assessment records, where the CVEs partially match the manufacturer and model on the OT device but the firmware version match is undetermined.
-   The **Vulnerable Items** tab displays the VITs that are created automatically or you create manually based on the assessments.
-   The **Ignored assessments** tab displays the assessments of the devices that you choose to ignore.
-   The **Awaiting Normalization** tab displays the OT device data that doesn’t have the normalized data and hasn't been used for assessment.

**Important:**

-   If the property to create automatic VIT is enabled, the **Fully matched assessments** tab doesn’t display any data. You can view this information in the Vulnerable Items tab.
-   Enable Opt-in feature in Enterprise Asset Management to allow OT devices be available for normalization. For more information, see [Opt-in to Enterprise Asset Management Content Service](https://www.servicenow.com/docs/access?context=optin-cs-eam&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).

## Delete obsolete assessments

You can also set up automatic deletion of obsolete assessment records.

1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Policies**.
2.  Search and select the **sn\_vul\_analyst\_firmware\_vulnerability\_assessment** policy.
3.  Select the **Active** check box.
4.  Select **Update**.

**Parent Topic:**[Exploring the Industrial Workspace](../../operational-technology-management/concept/exploring-industrial-workspace.md)

**Related topics**  


[Enterprise Asset Management normalization](https://www.servicenow.com/docs/access?context=normalization-eam&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)

[Industrial Workspace](../../operational-technology-management/concept/industrial-workspace-for-operational-technology.md)

[Setting up Hardware Vulnerability Assessment of OT devices using guided setup](../task/configure-hva-using-guided-setup.md)

[Using the Hardware Vulnerability Assessment menu in the Industrial Workspace](../task/using-hva-tabs-.md)

