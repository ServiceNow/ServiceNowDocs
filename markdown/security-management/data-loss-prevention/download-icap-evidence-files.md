---
title: Download evidence files for DLP alerts
description: Download files that violate the DLP policy on provider that supports ICAP. Download this file onto your local machine from the DLP IR Analyst workspace and DLP IR End user workspace for approvers.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Internet Content Adaption Protocol \(ICAP\) integration for DLP IR, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Download evidence files for DLP alerts

Download files that violate the DLP policy on provider that supports ICAP. Download this file onto your local machine from the DLP IR Analyst workspace and DLP IR End user workspace for approvers.

## Before you begin

Role required:

-   sn\_dlir.analyst and approvers can download

## About this task

You need to enable file download for ICAP before moving ahead.

## Procedure

1.  Navigate to **All** &gt; **ICAP DLP Integration** &gt; **Settings**.

2.  Enable the property sn\_icap\_dlp.enable\_file\_download **Enabling this property allows downloading the evidence file of the reported ICAP incident**.

    You will be able to see the **Download File** button on the DLP IR Analyst Workspace and DLP IR End user workspace.

3.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP Analyst Workspace**.

4.  Open a DLP incident record which is ingested from ICAP provider source.

5.  Click **Download File**.

    **Note:** DLP admin can control the access of **Download File** action for all integrations by disabling the **Should downloading the violating file of the reported incident be allowed** option from the **Advanced Settings** page of DLP Administration. For more information, see [Configure advanced settings](../../data-loss-prevention/task/configure-advanced-settings-dlp.md).


**Parent Topic:**[Internet Content Adaption Protocol \(ICAP\) integration for DLP IR](../concept/icap-dlp-integration.md)

