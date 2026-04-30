---
title: Components installed with the GRC: Metrics application
description: When the ESG Management application is activated, the GRC: Metrics application is automatically installed. The GRC: Metrics application adds several tables, properties, and roles that are listed here.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [GRC: Metrics reference, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Components installed with the GRC: Metrics application

When the ESG Management application is activated, the GRC: Metrics application is automatically installed. The GRC: Metrics application adds several tables, properties, and roles that are listed here.

## Roles installed

The following roles are installed with the GRC: Metrics application.

<table id="table_dhm_jyl_frb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains

</th></tr></thead><tbody><tr><td>

sn\_grc\_metric.admin

</td><td>

This role is the admin role for the application. This role can do the following:-   Create, read, write, and delete metric definitions, metrics, and metric units.
-   Override the results in metric data tasks.
-   Read metric data.
-   Create schedule.

</td><td>

sn\_grc\_metric.manager, sn\_grc.library\_admin

</td></tr><tr><td>

sn\_grc\_metric.manager

</td><td>

Enterprise owner and approver role for the application. This role can do the following:-   Create, read, write, and delete material topics, goals, targets, metric definitions, metrics, citations, and metric units.
-   Override the results in metric data tasks.
-   Read metric data, metric data tasks, disclosures, and authority documents.

 If there's an integration with Project Portfolio Management

-   Create, read, and write, projects and programs
-   Delete projects and programs

 If there's an integration with Integrated Risk Management, this role can do the following:

-   Create, read, write, and delete control objectives, controls, risk statements, and policies.
-   Read risks and issues.

</td><td>

sn\_grc\_metric.user

</td></tr><tr><td>

sn\_grc\_metric.user

</td><td>

This role is a read-only role. Users with this role can't create, edit, or update any metric definitions or metrics

</td><td>

None

</td></tr><tr><td>

sn\_grc\_metric.developer

</td><td>

User with this role can edit the script in automated metric definition.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

The following tables are installed with the GRC: Metrics application.

<table id="table_m2t_l4m_frb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Base Metric Definition

 \(sn\_grc\_metric\_base\_definition\)

</td><td>

Base table for all metric definitions.

</td></tr><tr><td>

Calculated Metric Definition

 \(sn\_grc\_metric\_composite\_definition\)

</td><td>

Calculated metric definitions that are used to aggregate data for two or more metric definitions.

</td></tr><tr><td>

Metric Definition

 \(sn\_grc\_metric\_definition\)

</td><td>

Metric definitions that are used to define automated and manual metrics.

</td></tr><tr><td>

Metric

 \(sn\_grc\_metric\_metric\)

</td><td>

Metric instances that are generated when a metric definition is applied to an entity.

</td></tr><tr><td>

Metric Unit

 \(sn\_grc\_metric\_unit\)

</td><td>

Unit for a metric definition or metric.

</td></tr><tr><td>

Parent Data

 \(sn\_grc\_metric\_parent\_data\)

</td><td>

Parent table for metric data.

</td></tr><tr><td>

Metric definition data

 \(sn\_grc\_metric\_collector\_data\)

</td><td>

Data for automated and manual metric definitions.

</td></tr><tr><td>

Metric Data

 \(sn\_grc\_metric\_metric\_data\)

</td><td>

Data for metric instances.

</td></tr><tr><td>

Metric Data Task

 \(sn\_grc\_metric\_data\_task\)

</td><td>

Task to collect data for manual metrics.

</td></tr><tr><td>

Entity type to Metric Definition

 \(sn\_grc\_metric\_m2m\_definition\_profile\_type\)

</td><td>

Association between Entity type and Metric definition.

</td></tr><tr><td>

Entity to Metric Definition

 \(sn\_grc\_metric\_m2m\_definition\_profile\)

</td><td>

Association between Entity and Metric definition.

</td></tr><tr><td>

Metric to Calculated Metric Definition

 \(sn\_grc\_metric\_m2m\_metric\_composite\_defnition\)

</td><td>

Association between Metric and Calculated Metric definition.

</td></tr><tr><td>

Child Metric Definition

 \(sn\_grc\_metric\_m2m\_metric\_definition\)

</td><td>

Association between Metric and Metric definition.

</td></tr><tr><td>

Control objective to Metric Definition\(sn\_grc\_metric\_m2m\_definition\_control\_objective\)

</td><td>

Association between Control objective and Metric definition.

</td></tr><tr><td>

Control to Metric Definition

 \(sn\_grc\_metric\_m2m\_definition\_control\)

</td><td>

Association between a control and a metric definition

</td></tr><tr><td>

Unit family

 \(sn\_grc\_metric\_unit\_family\)

</td><td>

A unit family to group similar units together.

</td></tr><tr><td>

Unit conversion

 \(sn\_grc\_metric\_unit\_conversion\)

</td><td>

Convert any metric data into a preferred reporting unit.

</td></tr><tr><td>

Metric to Calculated Metric Definition

 \(sn\_grc\_metric\_m2m\_metric\_composite\_definition\)

</td><td>

Association between a metric and calculated metric definition.

</td></tr><tr><td>

Metric data process queue\(sn\_grc\_metric\_data\_process\_queue\)

</td><td>

Indicates the metric definitions that are in the queue for refreshing the data for calculated metric definitions or updating the entity hierarchical data for all the types of metric definitions.

</td></tr><tr><td>

Metric data by entity\(sn\_grc\_metric\_data\_by\_entity\)

</td><td>

Includes data for entities in metric definition and aggregated data for its parent entities defined in the entity hierarchy.

</td></tr><tr><td>

Time dimension\(sn\_grc\_metric\_time\_dimension\)

</td><td>

Includes date, week, quarter, month, semi\_annual, year for each day in the year.

</td></tr><tr><td>

Metric import job\(sn\_grc\_metric\_import\_job\)

</td><td>

Table that holds the details of import jobs for metrics.

</td></tr><tr><td>

Metric data importsn\_grc\_metric\_data\_import

</td><td>

Staging table that stores the records parsed from input data file.

</td></tr><tr><td>

Metric import logsn\_grc\_metric\_st\_import\_log

</td><td>

Remote table that has data for showing import logs for import jobs.

</td></tr><tr><td>

Metric transform historysn\_grc\_metric\_st\_transform\_history

</td><td>

Remote table that has data of transaction history for import jobs.

</td></tr><tr><td>

Metric import templatesn\_grc\_metric\_import\_template

</td><td>

Table that stores the import templates used for preparing input data file for import job.

</td></tr></tbody>
</table>## Scheduled jobs

The scheduled jobs installed with the GRC: Metrics application run automatically at a specific time or schedule. Scheduled jobs can be set up to perform a wide variety of tasks such as running reports or data exports on a regular schedule.

|Name|Description|
|----|-----------|
|Aggregate metric definitions|This job is executed every 30 minutes. It pulls all types of metric definitions data which are active and have the state as **Pending**. It updates the "state" and "value" for each metric definitions data based on the aggregation of its corresponding metric data for that period.|
|CMD validity check|This job is executed once everyday at 12AM. For Each calculated metric definition, it updates the "status" to valid/invalid and the "notes" based on its duplicate child metric definitions and child metrics.|
|Execute calculated metric definitions|This job is executed for each calculated metric definition for both the entity level as well as the metric data definition level and updates with the calculated value.|
|Execute metrics|This job is executed daily once at 4:30PM. This executes for each metric definition and its metrics that create metric data and the metric data task if it does not exists for that period.|
|Generate metric data by entity|This job runs daily to do entity hierarchy rollup for all the metric definitions.|
|Generate time dimensions|This job runs on first day of every year and creates time dimensions for that year.|

## Properties installed

|Name|Description|Default value|
|----|-----------|-------------|
|sn\_grc\_metric.metric\_data\_task\_schedule|Specifies schedule to be used for due date calculation|08fcd0830a0a0b2600079f56b1adb9ae|
|sn\_grc\_metric.all\_words|Is used to replace all comma separated defined string in value to 'All' while importing metric data using Metric Integration.|\(blank\), blank, na, all, empty, \(empty\)|
|com.glide.event\_manager.grc\_metrics\_queue.even.load.distribution.enabled|Is used to distribute the events in the 'grc\_metric\_queue' queue equally between two worker threads.|500|
|com.glide.event\_manager.grc\_metrics\_queue.claim\_limit|Defines the maximum number of events that one worker thread can claim from the event queue.|true|

**Parent Topic:**[GRC: Metrics reference](../concept/grc-metrics-reference.md)

