---
title: Create a snapshot to share and save data in ERP Semantic Mining
description: Export and import ERP Semantic Mining base data to save and share.
locale: en-US
release: australia
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, ERP Semantic Mining overview, Workflow Data Fabric]
---

# Create a snapshot to share and save data in ERP Semantic Mining

Export and import ERP Semantic Mining base data to save and share.

## Before you begin

Role required: admin

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

## Procedure

1.  Navigate to **All** &gt; **ERP Foundation** &gt; **ERP Semantic Mining**.

2.  In the side panel, select the configuration icon.

3.  Select the **Change system** button.

4.  Select **Export data**.

    A check is performed automatically before exporting. For details about the process, see [ERP Semantic Mining snapshot prerequisite check](../reference/erpcm-snapshot-prerequisite-check.md).

    If another export is in progress, an export unavailable message is displayed. Select **OK** and view the **Snapshots** tab to monitor the progress.

    1.  On the pop-up window, review the message and select **Export data**.

        An automatic export is only performed before an import because an import overwrites the existing data. An export saves the data for a later import. An automatic export saves the data as a backup.

        In the **Snapshots** tab, the automatic export is **Pending**. Select the refresh icon to see the **Status** change to **In progress** and then **Complete**.

        For more execution details, open Workflow Studio, select **Operations**, and select **Flows**. The flow named **Export snapshot** calls the sub flow **Check set Snapshot to in progress**, and then calls the sub flow **Create Snapshot**. For more information about viewing flows in Workflow Studio, see [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

    2.  When the export is finished, go to the **Snapshots** tab on the **Configuration** page and select the completed export.

    3.  On the snapshot record, in **Attachments**, select the actions icon and then select **Download**.

5.  In the side panel, select the configuration icon.

6.  Select the **Change system** button, and then select **Import data**.

    1.  On the pop-up window, review the message and select the **I understand and want to import** option.

    2.  Select **+ Add file**.

    3.  Navigate to your downloads folder, select the ERP mining snapshot zip file, and select **Open**.

        The zip process is done using the ServiceNow Integration Hub Professional Pack Installer plugin. If the plugin isn't installed, the process uses the existing zip functionality on the MID Server.

    4.  In the pop-up window, select **Upload**.

        Validation is done automatically, for example, determining if there's an incomplete import job or an export job in progress.

    5.  When validation is complete, select **Import data**.

    6.  Check the status on the **Snapshots** tab.

    7.  When the import is complete, manually run AI/ML to obtain candidates out of the new imported data by selecting the **Change system** button and **Run AI/ML analysis**.

        AI/ML runs once a day automatically, but you can initiate the process manually at any time using the **Run AI/ML analysis** option. The manual and automatic process are the same and identify technical clusters, then candidate identification, and, lastly, model extensions.

        View the **All tasks** tab to check the status.


**Parent Topic:**[Configuring ERP Semantic Mining](../concept/configuring-ecm.md)

