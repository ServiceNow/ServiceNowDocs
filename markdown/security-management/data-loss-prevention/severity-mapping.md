---
title: Severity mapping between Symantec DLP incidents with ServiceNow incidents
description: Use the severity mapping feature to configure and synchronize the mapping between Symantec incidents and ServiceNow AI Platform incidents.
locale: en-US
release: zurich
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Symantec Integration for Data Loss Prevention Incident Response, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Severity mapping between Symantec DLP incidents with ServiceNow incidents

Use the severity mapping feature to configure and synchronize the mapping between Symantec incidents and ServiceNow AI Platform® incidents.

## Before you begin

Role required: sn\_dlir.admin

## About this task

DLP Severity mapping allows you to map the source severity with the DLP incident severity. You can customize and define the source severity value and map it to the desired DLP incident severity value.

## Procedure

1.  Navigate to **Symantec DLP integration** &gt; **Incident Severity Mapping**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Source|The configured Symantec Endpoint source from where you want to fetch the incident.|
    |Target Value|Target value is the DLP incident severity ID. The available values are Critical, High, Medium, Low, and Info \(used as the info severity in Symantec\).|
    |Source Value|Source value is the Symantec incident severity.|

    **Note:** Within the base system, there are four severity mappings that are shipped to the DLP users.

4.  Click **Submit**.

    ![DLP Severity Mapping](../image/dlp-severity-mapping.png "Severity Mapping")


**Parent Topic:**[Symantec Integration for Data Loss Prevention Incident Response](../concept/symantec-dlp-integration.md)

