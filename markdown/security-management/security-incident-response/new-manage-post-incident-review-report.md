---
title: Manage Post Incident Review Report
description: Manage post incident review report includes the information that was configured and applied by the Security Admin, and the security analysts can modify the timeline filters at run-time and download it.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Post incident review report, Manage post incident activities, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Manage Post Incident Review Report

Manage post incident review report includes the information that was configured and applied by the Security Admin, and the security analysts can modify the timeline filters at run-time and download it.

## Before you begin

Role required: sn\_si.analyst

## About this task

The Security Analyst can select either of the available primary or additional report templates, and configure the timeline filters, preview, and download the report. The Security Analyst can also directly download the report with the timeline configuration which was last applied.

The Security Analyst can access the reports using the Post Incident Review tab.

## Procedure

1.  Navigate to the security incident in the Review State.

2.  Click **Post Incident Review** tab.

3.  If the security incident is in the **Review** state:

    **Report Template:**

    -   By default, the primary report template that was configured on the set up page will be applied to the security incident and will be available to download.

    -   The analyst can choose other reports from the drop down list to configure and download the report.

4.  **Configure/Preview:**

    A security analyst can preview and modify the report template configuration. In the current configuration, the security analyst can only modify the timeline filters.

    In case the configuration is modified for the primary report before the security incident is closed, the post incident review report which is attached to the security incident will be updated as per the modifications done by the security analyst. After closure, the analyst will be able to modify the configuration and download the report on the go. However, the attached report would follow the last configuration before closure.

    To Configure/Preview the report, perform the following steps:

    1.  Select the desired report template from the **Report Template** drop down list on the **Post Incident Review** tab.
    2.  Click **Configure/Preview** tab.
    3.  **Update** or configure the timeline filters as required.
    4.  Use the **Show Images** checkbox to either include or exclude the images from the timeline. If unchecked, then only the names of the images are included in the timeline section.
    5.  Use the **Show Child Tasks** check box to list all the child tasks associated with the security incident.
5.  **Save** the configuration and click **Preview** tab to preview and download the report.

6.  Click **Download** to directly download the report.


