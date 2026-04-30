---
title: View the history of exporter executions
description: View a list of exporter executions to identify config updates that are successful and to isolate changes that caused failure in the pipeline.
locale: en-US
release: xanadu
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Export a snapshot, Use, DevOps Config, IT Service Management]
---

# View the history of exporter executions

View a list of exporter executions to identify config updates that are successful and to isolate changes that caused failure in the pipeline.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: cdm\_viewer or cdm\_exporter\_editor or cdm\_editor or cdm\_admin

## About this task

## Procedure

1.  Select the Admin icon \(![Admin icon.](../image/icon-admin-wrench.png)\) to open the **Administration** page.

2.  On the **Exporters** tab, select the name of the exporter.

3.  Select the **Executions** tab to view the list of executions.

    ![Executions tab that lists all executions for an exporter](../image/cdm-exporter-executions-tab.png)

<table><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique auto-generated identifier for the execution.

</td></tr><tr><td>

Version

</td><td>

Version of the exporter.

</td></tr><tr><td>

Type

</td><td>

-   Test: An execution in the test playground.
-   Standard: An execution that generates published config data.


</td></tr><tr><td>

Executed by

</td><td>

User that executed the exporter.

</td></tr><tr><td>

Start time / Duration

</td><td>

Timestamp when the execution started and the period of time that the exporter ran.

</td></tr><tr><td>

State

</td><td>

Result of the execution.

</td></tr><tr><td>

Application / Deployable / Snapshot

</td><td>

The application, deployable, and snapshot that the exporter used.

</td></tr></tbody>
</table>
