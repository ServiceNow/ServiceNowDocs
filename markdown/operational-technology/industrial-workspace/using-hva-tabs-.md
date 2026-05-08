---
title: Use the Hardware Vulnerability Assessment menu in the Industrial Workspace
description: Use the Hardware Vulnerability Assessment menu to view and track all the firmware vulnerability assessments in your OT environment. Also, in the HVA menu you can view the vulnerable items that are created based on the firmware vulnerability assessments.
locale: en-US
release: australia
product: Industrial Workspace
classification: industrial-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Industrial Workspace, Operational Technology]
---

# Use the Hardware Vulnerability Assessment menu in the Industrial Workspace

Use the Hardware Vulnerability Assessment menu to view and track all the firmware vulnerability assessments in your OT environment. Also, in the HVA menu you can view the vulnerable items that are created based on the firmware vulnerability assessments.

## Before you begin

Role required: sn\_otvr.vul\_event\_manager

## About this task

The Hardware Vulnerability Assessment menu provides information of all vulnerabilities in the Operational Technology \(OT\) inventory that match fully or partially to the vulnerabilities enlisted in the National Vulnerability Database \(NVD\).

## Procedure

1.  Navigate to **Workspaces** &gt; **Industrial Workspace** &gt; **Hardware Vulnerability Assessment. Select the menu icon \(![Menu icon.](../image/hva-menu.png)\)**.

2.  Perform the following actions on the **Fully matched assessments**, **Partially matched assessments**, **Vulnerable Items**, **Ignored assessments**, and **Awaiting Normalization** tabs as needed:

    1.  Choose additional columns and view them for more information regarding the assessment by selecting the update pPersonalized list icon \(![Update Personalized List.](../image/update-personalized-list.png)\).
    2.  Update thethe displayed list of assessments by selecting the refresh icon \( ![Refresh icon](../image/refresh-icon.png)\).
    3.  View assessment information in the tab according to the additional filter conditions that you select from the filter list icon \(![Filter list icon](../../mftg-manufacturing-process-mgr/image/filter-list-icon.png)\) icon.
    4.  Perform a quick filtration of assessments by selecting **Choose Filters**.
3.  View the assessment records by selecting the **Fully matched assessments** and **Partially matched assessments** tabs.

    1.  You can manually create vulnerable items for any assessment records that you choose. Select one or more records from the displayed list and then select **Create Vulnerable Items**.
    2.  You can ignore assessment records that you choose from the displayed list. Select one or more assessment records and then select **Ignore**. These ignored assessments are available on the **Ignored assessments** tab.
4.  On the **Ignored assessments** tab:

    1.  If you want to perform assessments on the OT devices that you have ignored previously, select **Revert**.
    2.  If you want to create vulnerable items manually for the assessments that you choose from the displayed list, select **Create Vulnerable Items**.
5.  The **Vulnerable Items** tab View the list of vulnerability items that are created based on the assessment records created in the **Fully matched assessments**, **Partially matched assessments**, and **Ignored assessments** tabs.

6.  View the OT device data that hasn't been used for assessment and awaiting normalization, by selecting the **Awaiting Normalization** tab.

    The device data may have the following normalization status:

    -   **New**
    -   **Match not found**
    -   **Publisher normalized**
    **Important:** Enable the Opt-in feature in Enterprise Asset Management, which enables OT devices to be available for normalization. For more information, see Opt-in to Enterprise Asset Management Content Service.


**Parent Topic:**[Using the Industrial Workspace](../../operational-technology-management/concept/using-industrial-workspace.md)

**Related topics**  


[Operational Technology Hardware Vulnerability Assessment](../concept/understanding-hwd-vuln-assessment.md)

[Set up the Hardware Vulnerability Assessment of Operational Technology devices using guided setup](configure-hva-using-guided-setup.md)

