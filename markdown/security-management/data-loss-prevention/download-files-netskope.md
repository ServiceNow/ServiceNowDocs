---
title: Download evidence files
description: Download files that violate the DLP policy on Netskope. Download this file onto your local machine from the DLP IR Analyst workspace and DLP IR End user workspace for approvers.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Loss Prevention Incident Response Integration with Netskope, Integrate, Data Loss Prevention Incident Response, Security Operations]
---

# Download evidence files

Download files that violate the DLP policy on Netskope. Download this file onto your local machine from the DLP IR Analyst workspace and DLP IR End user workspace for approvers.

## Before you begin

Role required:

-   sn\_dlir.analyst
-   sn\_dlir.secure\_file\_download \(any approver with this role\)

## About this task

You need to enable file download for Netskope before moving ahead.

## Procedure

1.  Navigate to **All** &gt; **Netskope DLP Integration** &gt; **Settings**.

2.  Enable the property **Should downloading the violating file of the reported incident be allowed**.

    You will be able to see the **Download File** button in the DLP IR Analyst Workspace and DLP IR End user workspace.

3.  Navigate to **All** &gt; **DLP Incident Management** &gt; **DLP Analyst Workspace**.

4.  Open a DLP incident record which is ingested from Netskope source.

5.  Click **Download File**.

    The file that violates the DLP policy on the Netskope will be downloaded to the user’s local machine.

    **Note:** DLP admin can control the access of **Download File** action for all integrations by disabling the **Should downloading the violating file of the reported incident be allowed** option from the **Advanced Settings** page of DLP Administration. For more information, see [Configure advanced settings](../../data-loss-prevention/task/configure-advanced-settings-dlp.md).


**Parent Topic:**[Data Loss Prevention Incident Response Integration with Netskope](../concept/dlp-incident-response-integration-netskope.md)

