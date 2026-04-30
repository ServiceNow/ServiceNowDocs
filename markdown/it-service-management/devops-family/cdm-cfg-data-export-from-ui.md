---
title: Export a snapshot
description: Export a snapshot to generate config data for the pipeline to use.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use, DevOps Config, IT Service Management]
---

# Export a snapshot

Export a snapshot to generate config data for the pipeline to use.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

-   The cdm\_secrets role is required to export snapshots that include encrypted data.
-   The cdm\_viewer can export any snapshot that does not include encrypted data.
-   The cdm\_exporter\_editor can create, edit, publish, activate, and delete exporters.

Role required: cdm\_exporter\_editor or cdm\_editor or cdm\_admin

## About this task

-   Exporters in the content pack have the **Source** value of **ServiceNow**. You can duplicate, but cannot delete or modify content pack exporters.
-   You can execute only active published exporters.
-   For export, snapshots cannot exceed 10,000 config data items \(CDIs\) per deployable or 100,000 CDIs per application.
-   Records of exporter executions are deleted after a period of three years. For instructions on changing the default time period, see [Set the purge period for records of exporter executions](cdm-export-record-purge.md).

## Procedure

1.  Select the admin icon \(![Admin icon.](../image/icon-admin-wrench.png)\) to open the **Administration** page.

2.  On the **Exporters** tab, select the name of the exporter.

    **Tip:** Add commonly used exporters to the **My Exporters** list for quick access.

    The **Versions** tab for the exporter opens, displaying the list of draft and published versions of the exporter.

3.  Select a published version of the exporter to run.

    The exporter opens on the **Exporter Builder** tab. The text of the exporter script appears in a view-only panel. Use the Test playground panel to specify the snapshot to export and test settings before you export the config data.

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
</table>5.  Select **Save** to save your changes and then select **Evaluate**.

    The exporter script runs using the settings that you specified and then displays the resulting config data in the Output box on the Review output page.

6.  Review the results.

    To make changes, select **Select inputs**, specify new settings, and then select **Evaluate**. Repeat as often as needed.

    **Note:** When you are satisfied that the exporter generates complete config data and follows the required output format standards, you can publish it and activate it.


