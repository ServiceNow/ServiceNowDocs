---
title: Create a snapshot to share and save data in ERP Semantic Mining
description: Export and import ERP Semantic Mining base data to save and share.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-customization-mining/create-a-snapshot-to-share-and-save-data.html
release: yokohama
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configuring ERP Semantic Mining, ERP Semantic Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# Create a snapshot to share and save data in ERP Semantic Mining

Export and import ERP Semantic Mining base data to save and share.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **ERP Foundation** &gt; **ERP Customization Mining**.

2.  In the side panel, select the configuration icon \(\[Omitted image "configuration-alias-icon.png"\] Alt text: Configuration page link\).

3.  Select the **Change system** button.

4.  Select **Export data**.

    A check is performed automatically prior to exporting. For details about the process, see [ERP Semantic Mining snapshot prerequisite check](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-customization-mining/erpcm-snapshot-prerequisite-check.md).

    If another export is in progress, an export unavailable message is displayed. Select **OK** and view the **Snapshots** tab to monitor the progress.

    1.  On the pop-up window, review the message and select **Export data**.

        An automatic export is only performed before an import because an import overwrites the existing data. An export saves the data for a later import. An automatic export saves the data as a backup.

        In the **Snapshots** tab, the automatic export is **Pending**. Select the refresh icon to see the **Status** change to **In progress** and then **Complete**.

        \[Omitted image "erpcm-snapshot-export-pending.png"\] Alt text: Snapshots list with an automatic export listed in pending state.

        For more execution details, open Workflow Studio, select **Operations**, and select **Flows**. The flow named **Export snapshot** calls the sub flow **Check set Snapshot to in progress**, and then calls the sub flow **Create Snapshot**. For more information about viewing flows in Workflow Studio, see [Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio/workflow-studio.md).

    2.  When the export is finished, go to the **Snapshots** tab on the **Configuration** page and select the completed export.

        \[Omitted image "erpcm-snapshot-export-complete.png"\] Alt text: Snapshots list.

    3.  On the snapshot record, in **Attachments**, select the actions icon and then select **Download**.

        \[Omitted image "erpcm-snapshot-export-record.png"\] Alt text: Snapshot record with attachments area highlighted.

        Next, import the data into another system.

5.  In the side panel, select the configuration icon \(\[Omitted image "configuration-alias-icon.png"\] Alt text: Configuration page link\).

6.  Select the **Change system** button, and then select **Import data**.

    1.  On the pop-up window, review the message and select the **I understand and want to import** option.

    2.  Select **+ Add file**.

    3.  Navigate to your downloads folder, select the ERP mining snapshot zip file, and select **Open**.

        \[Omitted image "erpcm-snapshot-select-zip.png"\] Alt text: Downloads folder with ERP snapshot zip file highlighted.

        The zip process is done using the ServiceNow Integration Hub Professional Pack Installer plugin. If the plugin isn't installed, the process uses the existing zip functionality on the MID Server.

    4.  In the pop-up window, select **Upload**.

        Validation is done automatically, for example, determining if there's an incomplete import job or an export job in progress.

    5.  When validation is complete, select **Import data**.

    6.  Check the status on the **Snapshots** tab.

        \[Omitted image "erpcm-snapshot-import-running.png"\] Alt text: Snapshots list with automatic export completed and import listed as in progress.

    7.  When the import is complete, manually run AI/ML to obtain candidates out of the new imported data by selecting the **Change system** button and **Run AI/ML analysis**.

        \[Omitted image "erpcm-snapshot-run-aiml-ys2.png"\] Alt text: Connect system button with options expand and run ai/ml option highlighted.

        AI/ML runs once a day automatically, but you can initiate the process manually at any time using the **Run AI/ML analysis** option. The manual and automatic process are the same and identify technical clusters, then candidate identification, and, lastly, model extensions.

        View the **All tasks** tab to check the status.

        \[Omitted image "erpcm-snapshot-complete.png"\] Alt text: All tasks list with import tasks listed as completed.


**Parent Topic:**[Configuring ERP Semantic Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-customization-mining/configuring-ecm.md)

