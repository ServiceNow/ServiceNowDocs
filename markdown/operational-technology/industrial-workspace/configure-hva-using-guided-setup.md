---
title: Set up the Hardware Vulnerability Assessment of Operational Technology devices using guided setup
description: Use the Industrial Workspace Admin guided setup to walk you through configuring the Hardware Vulnerability Assessment feature available on the Industrial Workspace menu.
locale: en-US
release: australia
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Industrial Workspace, Operational Technology]
---

# Set up the Hardware Vulnerability Assessment of Operational Technology devices using guided setup

Use the Industrial Workspace Admin guided setup to walk you through configuring the Hardware Vulnerability Assessment feature available on the Industrial Workspace menu.

## Before you begin

Role required: admin

## About this task

Use the Industrial Workspace Admin guided setup to assign required user roles, configure a system property, and schedule jobs to perform the hardware vulnerability assessment of Operational Technology devices.

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Guided Setup** &gt; **Operational Technology Vulnerability Response**.

2.  Select **Get Started** for the Operational Technology Vulnerability Response application.

3.  Select the **Hardware Vulnerability Assessment** task.

4.  Select the following task tabs, then select **Configure** to complete the configuration tasks.

    |Task|Purpose|
    |----|-------|
    |**User Roles assignment**|Assign users or user groups with roles that enable them to use the Hardware Vulnerability Assessment feature.|
    |**Install and Run NVD Integration**|Run the National Vulnerability Database \(NVD\) integration to import data from the NIST NVD database to help you determine the severity and details of CVEs found in your environment.|
    |**Configure Vulnerability Assessment properties**|Configure the properties required to perform hardware vulnerability assessment for OT devices.|
    |**Schedule Vulnerability Assessment Jobs**|Execute scheduled jobs that enable vulnerability assessment on OT devices in the inventory and mark expired assessments that must be deleted.|
    |**Normalization opt-in**|Select **Firmware Discovery Model** Opt-in option for ServiceNow Asset Management Content Service to collect unnormalized firmware details of OT devices and update the normalized content library. This process improves the ratio of normalized data mapping to CVEs and therefore improves assessment of vulnerabilities.|
    |**Delete obsolete assessments**|Configure the time duration after which the obsolete and expired assessments are deleted.|


-   **[Assign roles for Hardware Vulnerability Assessment](assign-hva-roles.md)**  
Assign roles to users so that they can configure properties, and use hardware vulnerability assessments features, capabilities, and data.
-   **[Run NVD Integrations for Hardware Vulnerability Assessment](jobs-hwd-nvd-integration.md)**  
Install and run National Vulnerability Database \(NVD\) integrations to perform hardware vulnerability assessment.
-   **[Configure properties for Hardware Vulnerability Assessment](configure-hva-properties.md)**  
Configure the properties required to perform hardware vulnerability assessment.
-   **[Run scheduled jobs to perform Hardware Vulnerability Assessment](jobs-hwd-vul-assessment.md)**  
Execute scheduled jobs to perform hardware vulnerability assessment.
-   **[Configure Normalization Opt-in for Hardware Vulnerability Assessment](hva-normalization-opt-in.md)**  
Select **Firmware Discovery Model** Opt-in option for ServiceNow Asset Management Content Service to collect unnormalized firmware details of Operational Technology \(OT\) devices and update the normalized content library. This process improves the ratio of normalized data mapping to CVEs and therefore improves assessment of vulnerabilities.
-   **[Delete obsolete and expired hardware vulnerability assessments](otvr-delete-obsolete-and-expired-assessments.md)**  
Set up automatic deletion of obsolete or expired assessment records.

**Parent Topic:**[Configuring the Industrial Workspace](../../operational-technology-management/concept/configuring-industrial-workspace.md)

**Related topics**  


[Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/guided-setup.md)

[Operational Technology Hardware Vulnerability Assessment](../concept/understanding-hwd-vuln-assessment.md)

