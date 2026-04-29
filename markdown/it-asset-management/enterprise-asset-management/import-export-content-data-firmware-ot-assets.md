---
title: Import and export content data for firmware in your operational technology \(OT\) assets
description: Import and export content data for firmware that is embedded into your on-premise OT assets. Share this data with the Content Service team so that you can help improve the normalization process.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Normalizing firmware for OT assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Import and export content data for firmware in your operational technology \(OT\) assets

Import and export content data for firmware that is embedded into your on-premise OT assets. Share this data with the Content Service team so that you can help improve the normalization process.

## Before you begin

**Important:** You can import and export this firmware content data only the in OT Asset Workspace. To use the OT Asset Workspace, install the OT Asset Management application on your ServiceNow instance. See [Install OT Asset Management](install-otam.md) for detailed instructions.

**Important:** To import and export this firmware content data, set the **sn\_itam\_common.onprem\_content\_import\_export** system property to `true` on your ServiceNow instance. In addition, opt in to the Enterprise Asset Management Content Service and verify that the Custom Firmware Models KPI is enabled. See [Opt-in to Enterprise Asset Management Content Service](optin-cs-eam.md) for detailed instructions.

Role required: sn\_otam.ot\_asset\_manager

## Procedure

1.  Navigate to **All** &gt; **OT Asset Workspace** &gt; **Admin center**.

2.  Import firmware content data onto your ServiceNow instance.

    1.  From the navigation menu of the Admin center view, navigate to **Manage library** &gt; **Import firmware content**.

    2.  Select the Attachments icon ![](../../contract-management/image/attachments-icon.png) on the sidebar of the Import page.

    3.  In the Attachments window, select **Select a file**.

    4.  When prompted, search for and select the zip file that contains your firmware content data.

    5.  In the Upload a file dialog box, select **Upload**.

    6.  After the dialog box closes, select **Run Import** on the Import page.

    After the content data is successfully imported, the OT Asset Management application automatically triggers the **EAM - Apply latest content changes** scheduled job to process any corresponding content updates, which you can then use to normalize your firmware.

3.  Export firmware content data from your ServiceNow instance.

    By exporting your firmware content data, you can share any custom or partially normalized firmware with the Content Service team. In addition, you can share data for your firmware versions, firmware models, and firmware life cycles.

    1.  From the navigation menu of the Admin center view, navigate to **Manage library** &gt; **Export firmware content**.

    2.  Select **Run Export**.

        The OT Asset Management application compresses all of your firmware content data into a single zip file. When the zip file is ready for download, the page automatically reloads.

    3.  Select the Attachments icon ![](../../contract-management/image/attachments-icon.png) on the sidebar of the Export page.

    4.  In the Attachments window, select the Actions icon ![](../../../common/image/icon-menu.png) for the zip file that you want to download.

    5.  Download the zip file and then send it to the Content Service team.


