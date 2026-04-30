---
title: Exporting Application Portfolio Management data to Microsoft PowerPoint - Legacy
description: Generate and download the status reports from your Application Portfolio Management instance as a Microsoft PowerPoint file. You can share this report with stakeholders and teams for collaboration.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore- Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Exporting Application Portfolio Management data to Microsoft PowerPoint - Legacy

Generate and download the status reports from your Application Portfolio Management instance as a Microsoft PowerPoint file. You can share this report with stakeholders and teams for collaboration.

Stakeholders might not have access to the ServiceNow instance, or they might prefer using Microsoft PowerPoint to consume key information. You can convey critical application portfolio status and health details to stakeholders via Microsoft PowerPoint. Instead of collecting all the data manually, you can export the data from the ServiceNow instance to Microsoft PowerPoint.

**Important:** Export to PowerPoint is currently unavailable for customers in the FedRAMP, NSC DOD IL5, or Australia IRAP-Protected data centers, self-hosted customers, or in other restricted environments. Please check for availability updates in future releases.

You can export the following Application Portfolio Status data:

-   Application Landscape
    -   Application Portfolio by Install Type
    -   Application Portfolio by Platform
    -   Application Portfolio by Technology Stack
    -   Application Portfolio by Category
    -   Most Used Applications by Application Family
    -   Application Portfolio by Install Type and Platform
-   Capabilities Landscape
    -   Capabilities by Assessment \(Top Scoring Capabilities\)
    -   Capabilities by Assessment \(Low Scoring Capabilities\)

The Export to PowerPoint feature in APM uses the Export to PowerPoint for Application Portfolio Management plugin \(com.snc.apm\_ppt\_export\). This plugin depends on the base plugin Export to PowerPoint \(com.snc.sn\_ppt\_export\). Ensure that both APM and PowerPoint plugins are installed to use the Export to PowerPoint feature in APM. For more information about the base plugin, creating templates, and report types, see [Export to PowerPoint for Strategic Portfolio Management](https://www.servicenow.com/docs/access?context=export-ppt-landing-page&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US).

**Related topics**  


[Export data to Microsoft PowerPoint - Legacy](../task/export-apm-data-ppt.md)

