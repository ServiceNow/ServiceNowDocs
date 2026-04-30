---
title: Using the Hardware Vulnerability Assessment menu in the Industrial Workspace
description: The Hardware Vulnerability Assessment menu provides information of all vulnerabilities in the OT inventory that match fully or partially to the vulnerabilities enlisted in NVD.
locale: en-US
release: xanadu
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2025-01-13"
reading_time_minutes: 2
breadcrumb: [Use, Industrial Workspace, Operational Technology]
---

# Using the Hardware Vulnerability Assessment menu in the Industrial Workspace

The Hardware Vulnerability Assessment menu provides information of all vulnerabilities in the OT inventory that match fully or partially to the vulnerabilities enlisted in NVD.

## Before you begin

Role required: sn\_otvr.vul\_event\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Industrial Workspace** &gt; **Hardware Vulnerability Assessment\(![menu](../image/hva-menu.png)\)**.

2.  You can perform the following actions on the **Fully matched assessments**, **Partially matched assessments**, **Vulnerable Items**, **Ignored assessments**, and **Awaiting Normalization** tabs:

    1.  Select ![Update Personalized List](../image/update-personalized-list.png) to choose additional columns and view for more information regarding the assessment.
    2.  Select ![Refresh](../image/refresh-icon.png) to update the displayed list of assessments.
    3.  Select ![Filter](../image/filter-icon.png) to display assessment information in the tab according to the additional filter conditions you choose.
    4.  Select **Choose Filters** to perform a quick filtration of assessments.
3.  Select the **Fully matched assessments** and **Partially matched assessments** tabs to display the assessment records.

    1.  Select one or more assessment records and select **Create Vulnerable Items** to manually create vulnerable items for the assessment records you choose from the displayed list.
    2.  Select **Ignore** to ignore the assessment records you choose from the displayed list. The assessment you ignore are available in the **Ignored assessments** tab.
4.  In the **Ignored assessments** tab:

    1.  Select **Revert** to perform assessments on the OT devices you have ignored previously.
    2.  Select **Create Vulnerable Items** to create vulnerable items manually for the assessments you choose from the displayed list.
5.  Select the **Vulnerable Items** tab.

    This tab displays the list of vulnerability items that are created based on the assessment records created in the **Fully matched assessments**, **Partially matched assessments**, and **Ignored assessments** tabs.

6.  Select the **Awaiting Normalization** tab to display the OT device data that hasn't been used for assessment, where the normalization status is:

    -   **New**
    -   **Match not found**
    -   **Publisher normalized**
    **Important:** Enable the Opt-in feature in Enterprise Asset Management, which enables OT devices to be available for normalization. For more information, see [Opt-in to Enterprise Asset Management Content Service](https://www.servicenow.com/docs/access?context=optin-cs-eam&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).


**Parent Topic:**[Using the Industrial Workspace](../../operational-technology-management/concept/using-industrial-workspace.md)

**Related topics**  


[Hardware Vulnerability Assessment](../concept/understanding-hwd-vuln-assessment.md)

[Setting up Hardware Vulnerability Assessment of OT devices using guided setup](configure-hva-using-guided-setup.md)

