---
title: Operational Technology Hardware Vulnerability Assessment
description: The Operational Technology \(OT\) Hardware Vulnerability Assessment \(HVA\) application enables you to assess the firmware vulnerabilities of the OT devices in inventory and create vulnerable items \(VIT\) against the impacted OT devices.
locale: en-US
release: australia
product: Industrial Workspace
classification: industrial-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Explore, Industrial Workspace, Operational Technology]
---

# Operational Technology Hardware Vulnerability Assessment

The Operational Technology \(OT\) Hardware Vulnerability Assessment \(HVA\) application enables you to assess the firmware vulnerabilities of the OT devices in inventory and create vulnerable items \(VIT\) against the impacted OT devices.

## Hardware Vulnerability Assessment overview

Hardware Vulnerability Assessment uses normalized content for firmware discovery model to perform assessments. The normalized content contains OT device data, such as manufacturer, firmware version, and product model. It's based on the normalization process available in Enterprise Asset Management. The normalized content for OT devices is mapped according to the Common Platform Enumeration \(CPE\) format provided by the National Vulnerability Database \(NVD\). An OT device is considered at risk, when the Common Vulnerabilities and Exposures \(CVEs\) data available in the NVD database, matches the OT device data available in the CPE-mapped normalized content. The Hardware Vulnerability Assessment menu available in the Industrial Workspace displays the OT devices that are at risk.

HVA can assess firmware discovery models, which don’t have normalized content and they haven’t been CPE-mapped yet. HVA uses a matching score algorithm to compare CPE values with existing firmware discovery values. The matching algorithm searches for CPEs that matches OT devices with the same discovery publisher name, model name, and version. The HVA matching algorithm compares the data from CPEs and unmapped firmware discovery model. Based on the comparison, the matching algorithm evaluates the best possible CPE match for unmapped firmware discovery models. Even though the results may not be fully accurate, it helps in vulnerability assessments until CPE-mapped normalized content is available.

Also, HVA uses the range information provided by NVD to assess vulnerabilities more accurately. For example:

-   In case there’s a version information unavailable for a CPE, the range information available for a specific OT device publisher and model is used to perform a hardware vulnerability assessment.
-   For versions, a comparison algorithm is used to determine if the input version is in range.

**Important:** If you’re already using HVA, rerun the NVD Integrations to use the range information feature. For more information, see [Run NVD Integrations for Hardware Vulnerability Assessment](../task/jobs-hwd-nvd-integration.md).

You must activate and schedule the following scheduled jobs to perform hardware vulnerability assessment automatically and periodically:

-   **Hardware Vulnerability Assessment - Full**
-   **Hardware Vulnerability Assessment - Delta**

## Required Operational Technology and Hardware Vulnerability Assessment roles

You must have the following roles to use the Hardware Vulnerability Assessment \(HVA\) menu:

-   sn\_vul.manage\_exposure\_assessment: Assign roles to admin users or user groups as needed, which enables them to view or edit properties for HVA.
-   sn\_otvr.vul\_event\_manager \(OT Vulnerability Event Manager\): Assign roles to HVA users  or user groups as needed, which enables them to view assessment records and act accordingly.

## Use Case

OT hardware vulnerability analysts can use HVA to:

-   Identify cybersecurity risks in OT devices.
-   Focus on high-risk vulnerabilities via fully matched assessments on OT device data.
-   Set up automatic creation of vulnerable items for fully matched assessments.
-   Investigate and address partially matched assessments to identify potential risks and act accordingly.
-   Monitor unprocessed OT devices from the **Awaiting Normalization** tab, which are pending full discovery or pending content updates.

## HVA tabs

The HVA menu displays HVA records created for the OT devices. These assessment records are created based on many criteria. For example, CVE vulnerability, OT device at risk, Common Vulnerability Scoring System \(CVSS\) score, Confidence Score, and Device Criticality.

-   The **Fully matched assessments** tab displays the assessment records, where the CVEs fully match with the manufacturer, product model, and firmware version of the OT devices. A fully matched assessment means that an OT device matches all vulnerability factors specified in a CVE.
-   The **Partially matched assessments** tab displays the assessment records, where the CVEs partially match the firmware version or the manufacturer and model on the OT device. Also, HVA creates partial assessments for normalized discovery models, which don’t have firmware version available. Using the matching algorithm, the version information from the normalized content of OT devices with the same publisher and model​ is used to create an assessment.
-   The **Vulnerable Items** tab displays the VITs that are created automatically or you create manually based on the assessments.
-   The **Ignored assessments** tab displays the assessments of the devices that you choose to ignore.
-   The **Awaiting Normalization** tab displays the OT device data that doesn’t have the normalized data and hasn't been used for assessment.

**Important:**

-   If the property to create automatic VIT is enabled, the **Fully matched assessments** tab doesn’t display any data. You can view this information on the **Vulnerable Items** tab.
-   Enable the Firmware Discovery Model Opt-in feature in Enterprise Asset Management so that OT devices data are available for normalization. For more information, see Opt-in to Enterprise Asset Management Content Service.

## Additional Resources

-   **[Confidence score calculation for hardware vulnerability assessment](../reference/otvr-hva-confidence-score-sample.md)**  
Confidence Score is displayed for partially matched assessments, vulnerable items \(VITs\), and ignored assessments.
-   **[Confidence score reference tables for hardware vulnerability assessment](../reference/otvr-hva-confidence-score-ref.md)**  
Reference values used to calculate the confidence score.

**Parent Topic:**[Exploring the Industrial Workspace](../../operational-technology-management/concept/exploring-industrial-workspace.md)

**Related topics**  


[bundle-itam.normalization-eam]

[Industrial Workspace](../../operational-technology-management/concept/industrial-workspace-for-operational-technology.md)

[Set up the Hardware Vulnerability Assessment of Operational Technology devices using guided setup](../task/configure-hva-using-guided-setup.md)

[Use the Hardware Vulnerability Assessment menu in the Industrial Workspace](../task/using-hva-tabs-.md)

