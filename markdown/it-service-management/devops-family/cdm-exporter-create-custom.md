---
title: Create a custom exporter
description: Copy an existing exporter script as a starting point for a custom exporter.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Export a snapshot, Using DevOps Config, DevOps Config, IT Service Management]
---

# Create a custom exporter

Copy an existing exporter script as a starting point for a custom exporter.

## Before you begin

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

Role required: cdm\_exporter\_editor or cdm\_editor or cdm\_admin

## About this task

DevOps Config content packs provide a variety of exporters. You can use any of the provided exporter scripts as a starting point for a custom exporter that you design.

## Procedure

1.  Select the admin icon \(![Admin icon.](../image/icon-admin-wrench.png)\) to open the **Administration** page.

2.  On the **Exporters** tab, select **New**, enter a unique and meaningful name and description, and then select **Confirm**.

    The first draft version of the exporter is named **Draft 0.1** and is listed on the **Versions** tab.

    ![DevOps Config validate](../image/cdm-exporter-create.png)

3.  Select the **Version name** to open default exporter script on the **Exporter builder** tab.

    The text of the exporter script appears in a view-only panel.

4.  On the **Exporters** tab, select the name of the exporter that will act as the starting point for the new custom exporter.

5.  Select the exporter version to use on the **Versions** tab for the exporter.

    The exporter opens on the **Exporter Builder** tab. The text of the exporter script appears in a view-only panel.

6.  Copy the text of the script for use in the new exporter.

7.  To enable users to specify dynamic execution conditions or CDI values when editing the exporter, create an input argument.

    1.  On the **Input arguments** tab, click **New**.

    2.  On the Create argument pop-up window, define the argument.

<table id="table_spt_qkq_wsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name / Description

</td><td>

Meaningful name and description for the argument.

</td></tr><tr><td>

Default value

</td><td>

Value that the argument will have when a user opens the exporter for editing.

</td></tr><tr><td>

Mandatory

</td><td>

Select the check box to require that the argument value is specified.

</td></tr></tbody>
</table>    3.  Select **Create**.

        The argument now appears in the **Input arguments** field on the Test Playground panel.


