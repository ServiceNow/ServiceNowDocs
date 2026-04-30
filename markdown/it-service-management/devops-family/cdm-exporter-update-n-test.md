---
title: Test an exporter and export a snapshot
description: Set and validate input settings to test an exporter before you export the config data in a snapshot.
locale: en-US
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Export a snapshot, Use, DevOps Config, IT Service Management]
---

# Test an exporter and export a snapshot

Set and validate input settings to test an exporter before you export the config data in a snapshot.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Role required: cdm\_exporter\_editor or cdm\_editor or cdm\_admin

-   The cdm\_secrets role is required to export snapshots that include encrypted data.
-   The cdm\_viewer can export any snapshot that does not include encrypted data.
-   The cdm\_exporter\_editor can create, edit, publish and delete exporters.

## About this task

Be sure to install the exporter content pack for DevOps Config. Exporters in the content pack are good starting points for your custom exporters. Some content pack exporters generate subsets of config data and others generate data for full applications. For example, to export updated config data for a database, you might select the **returnAllDataforNodeName** exporter. In the input arguments for the exporter, you would specify the database deployable as the node and then specify the updated settings as input arguments. After you determine that the settings generate the desired config data, you can export the data to the pipeline.

-   Exporters in the content pack have the **Source** value of **ServiceNow**. You can duplicate, but cannot delete or modify content pack exporters.
-   You can run only published exporters.
-   For export, snapshots cannot exceed 10,000 config data items \(CDIs\) per deployable or 100,000 CDIs per application.
-   For information on creating a custom exporter, see [Create a custom exporter](cdm-exporter-create-custom.md).
-   Records of exporter executions are deleted after a period of three years. For instructions on changing the default time period, see [Set the purge period for records of exporter executions](cdm-export-record-purge.md).

## Procedure

1.  Select the admin icon \(![Admin icon.](../image/icon-admin-wrench.png)\) to open the **Administration** page.

2.  On the **Exporters** tab, select the name of the exporter.

    **Tip:** Add commonly used exporters to the **My Exporters** list for quick access.

3.  Select the exporter version on the **Versions** tab.

    The exporter opens on the **Exporter builder** tab. The text of the exporter script appears in a view-only panel. Use the **Test playground** panel to specify the snapshot to export and test settings before you export the config data.

4.  Specify the settings for the exporter execution on the **Select inputs** page.

<table id="table_x4p_3m1_rqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Deployable and published snapshot to export

</td><td>

Deployable for export and the particular published snapshot that you have validated and want to use.

 Deployables appear in the list using the format `<AppName/DeployableName>`. When you select a deployable, another field lists all published snapshots for the deployable. The most recently published snapshot appears first in the list. Select the snapshot to export.

</td></tr><tr><td>

Input arguments

</td><td>

The arguments that the exporter script uses to generate config data as output. The text box displays the default values for all arguments. Update values as needed.

</td></tr><tr><td>

Output format

</td><td>

Format in which to generate the config data.

</td></tr><tr><td>

Additional deployables

</td><td>

Deployables for which to generate config data in addition to the primary deployable that you specified in the **Deployable and published snapshot to export** field.

 Only the latest published snapshots appear for this optional setting.

</td></tr></tbody>
</table>5.  Select **Evaluate**.

    -   The exporter script executes using the settings that you specified.
    -   The **Test playground** panel displays the Review output page.
    -   The config data that the exporter generates appears in the **Output** box.
    -   The system lists information about the execution on the **Executions** tab.
6.  Review the results.

    1.  To make changes, select **Select inputs**, specify new settings, and then select **Evaluate**.

    2.  Repeat the previous step as often as needed.

    **Note:** When you are satisfied that the exporter generates complete config data and follows the required output format standards, you can publish it and activate it.

7.  Publish the exporter by selecting **Publish** on the **Exporter builder** tab.

    **Note:** You must set an exporter to active to enable it to be executed in a pipeline.


