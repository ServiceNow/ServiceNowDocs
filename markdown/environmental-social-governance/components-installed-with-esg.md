---
title: Components installed with Operational Sustainability Management \(formerly ESG Management\)
description: Several types of components such as roles, tables, and properties are installed with the Operational Sustainability Management application and the GRC: Metrics application.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Operational Sustainability Management \(formerly ESG\) reference, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Components installed with Operational Sustainability Management \(formerly ESG Management\)

Several types of components such as roles, tables, and properties are installed with the Operational Sustainability Management application and the GRC: Metrics application.

## Roles

The following roles are installed with the Operational Sustainability Management application.

**Note:** For the tables and roles installed with the GRC: Metrics application, see [Components installed with the GRC: Metrics application](../../metrics/reference/tables-installed-with-metrics.md).

<table id="table_m4l_lwl_frb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Privileges

</th><th>

Contains

</th></tr></thead><tbody><tr><td>

sn\_esg.admin

</td><td>

Manages all the items within the application and configures the setup for ESG integrations.

</td><td>

Users with this role can read, write, update, and delete the following:-   Material topics
-   Goals
-   Targets
-   Metric definitions
-   Metrics
-   Metric data
-   Metric data task
-   Disclosures
-   Authority documents
-   Citations
-   Citations and metric definitions from the Unified content management application
-   Risk assessment factors
-   Update and publish risk assessments methodologies
-   Emission activity
-   Emission activity source
-   Emission factor
-   Emission factor location

If Scope 3 emissions is installed, this role can do the read, write, update, and delete the following.

-   Scope 3 emission category types
-   Supplier emissions by model
-   Inflation factors

These users can read and update the **sn\_esg\_scope3.historical\_years\_selector** system property and can access the Scope 3 dashboard.

</td><td>

sn\_esg.program\_manager, sn\_esg.integrations\_admin, sn\_esg.internal\_admin, sn\_grc\_metric.admin, sn\_esg.internal\_disclosure\_manager, report\_user, sn\_esg\_msoff\_intg.admin, If the ESG Risk Management plugin is activated, sn\_risk\_advanced.ara\_admin, and sn\_risk.manager roles are installed. If the com.snc.multiprovider\_documents plugin is activated, the mp\_document\_user role is added.

</td></tr><tr><td>

sn\_esg.metrics\_manager

</td><td>

Manages metrics in the ESG workspace.

</td><td>

Users with this role can read the following:-   Material topics
-   Goals
-   Targets
-   Metric data
-   Metric data task
-   Authority documents
-   Citations

 These users can read, write, and update the metrics and metric definitions. These users can only delete those metrics definitions and metrics that they have created.

</td><td>

sn\_esg.reader, sn\_grc\_metric.manager

</td></tr><tr><td>

sn\_esg.reporting\_disclosure\_manager

</td><td>

Manages disclosure report in the ESG workspace.

</td><td>

Users with this role can read the following:-   Material topics
-   Goals
-   Targets
-   Metric definitions
-   Metrics
-   Metric data
-   Metric data task
-   Authority documents
-   Citations
-   Scope 3 emission category types
-   Supplier emissions by model
-   Inflation factors

 These users can read, write, and update the disclosures. These users can only delete those disclosure that they have created.

</td><td>

sn\_esg.internal\_disclosure\_manager, sn\_esg.reader, report\_user, sn\_esg\_msoff\_intg.reader If the com.snc.multiprovider\_documents plugin is activated, the mp\_document\_user role is added.

</td></tr><tr><td>

sn\_esg.data\_owner

</td><td>

Data owner role to provide input to the assigned metric data tasks.

</td><td>

Users with this role can read the following:-   Goals
-   Targets
-   Metric definitions
-   Metrics
-   Metric data
-   Authority documents
-   Citations

 These users can read, and update the metric data tasks.

</td><td>

sn\_grc\_metric.user, workspace\_user, sn\_gf.goal\_user\_read, canvas\_user, sn\_grc\_metric.reader, sn\_grc\_workspace.task\_reader,sn\_grc\_workspace.user, sn\_grc.library\_readerIf the ESG Risk Management plugin is activated, sn\_risk\_advanced.ara\_assessor sn\_risk.reader roles are installed.

</td></tr><tr><td>

sn\_esg.program\_manager

</td><td>

Supports the execution and management of ESG program development, implementation, and reporting.

</td><td>

Users with this role can read, write, update, and delete the following:-   Material topics
-   Goals
-   Targets
-   Metric definitions
-   Metrics
-   Metric data
-   Metric data task
-   Content accelerator
-   Emission activity
-   Emission activity source
-   Emission factor
-   Emission factor location
-   Scope 3 emission category types
-   Supplier emissions by model
-   Inflation factors

 These users can read authority documents, citations, framework status, GRI citation, Metric definition, SASB citation, TCFD citation, UN SDG citation, Scope 3 dashboard, inflation factors.

If the Unified content management, application is installed, these users can read emission activity source, emission activity, emission factor location, emission unit, and disclosures. They can read and update Emission activity location.

They can also delete only those metrics and metric definitions that they have created.

They can read and update the system property Scope 3 dashboard's historical years selector.

</td><td>

sn\_esg.reader, sn\_gf.epmo\_strategy\_planner, sn\_grc\_metric.manager, sn\_gf.goal\_user, sn\_esg.internal\_manager, sn\_grc.library\_admin, sn\_compliance.library\_adminIf the ESG Risk Management plugin is activated, sn\_risk.reader sn\_risk\_advanced.ara\_approver,sn\_risk\_advanced.ara\_assessor,sn\_risk\_advanced.ara\_creator roles are installed.

</td></tr><tr><td>

sn\_esg\_risk\_mgmt.risk\_manager

</td><td>

Manages risk assessments in the ESG domain.**Note:** This role is available only when the sn\_esg\_risk\_mgmt is installed and activated.

</td><td>

Users with this role can do the following tasks:-   Create the risk framework
-   Create risk statements
-   Create risks
-   Create the risk scope to generate risks
-   Initiate risk assessments
-   Approve risk assessments

</td><td>

sn\_risk.manager

</td></tr><tr><td>

sn\_grc\_claims.manager

</td><td>

Manages claims in the ESG domain.

</td><td>

Users with this role can do the following tasks:-   Create a claim
-   Edit a claim
-   Export a claim

</td><td>

sn\_grc\_claims.manager

</td></tr></tbody>
</table>## Tables

The following tables are installed with the Operational Sustainability Management application.

<table id="table_thf_cgm_frb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Material Topic

 \[sn\_esg\_material\_topic\]

</td><td>

Material topics to define ESG material issues

</td></tr><tr><td>

Unit family

 \[sn\_grc\_metric\_unit\_family\]

</td><td>

Categorize and group units

</td></tr><tr><td>

Unit conversion

 \[sn\_grc\_metric\_unit\_conversion\]

</td><td>

Set up unit conversion value for From and To units

</td></tr><tr><td>

Emission activity

 \[sn\_esg\_emission\_activity\]

</td><td>

An emission activity is any activity that leads to emissions

</td></tr><tr><td>

Emission factor

 \[sn\_esg\_emission\_factor\]

</td><td>

An emission factor is a coefficient that allows to convert activity data into greenhouse gas \(GHG\) emissions

</td></tr><tr><td>

Emission factor location

 \[sn\_esg\_emission\_factor\_location\]

</td><td>

To capture emission factor at location level

</td></tr><tr><td>

Calculated metric definition to Emission factor

 sn\_esg\_m2m\_calculated\_definition\_emission\_factor

</td><td>

Association between calculated metric definitions and emission factor

</td></tr><tr><td>

Metric to Goal

 \[sn\_esg\_m2m\_metric\_goal\]

</td><td>

Association between metric and goal

</td></tr><tr><td>

Metric to Target

 \[sn\_esg\_m2m\_metric\_target\]

</td><td>

Association between metric and target

</td></tr><tr><td>

Material Topic to Goal

 \[sn\_esg\_m2m\_material\_topic\_goal\]

</td><td>

Association between material topic and goal

</td></tr><tr><td>

Goal to Disclosure

 \[sn\_esg\_m2m\_goal\_disclosure\]

</td><td>

Association between goal and disclosure

</td></tr><tr><td>

Goal to Citation

 \[sn\_esg\_m2m\_goal\_citation\]

</td><td>

Association between goal and citation

</td></tr><tr><td>

Entity to Goal

 \[sn\_esg\_m2m\_entity\_goal\]

</td><td>

Association between entity and goal

</td></tr><tr><td>

Metric to Disclosure

 \[sn\_esg\_m2m\_disclosure\_metric\]

</td><td>

Association between metric and disclosure

</td></tr><tr><td>

Metric Definition to Disclosure

 \[sn\_esg\_m2m\_disclosure\_metric\_definition\]

</td><td>

Association between metric definition and disclosure

</td></tr><tr><td>

Related URL

 \[sn\_grc\_metric\_data\_task\_url\]

</td><td>

Used to upload relevant documents and resources for the data task.

</td></tr><tr><td>

Threshold

 \[sn\_grc\_metric\_threshold\]

</td><td>

Threshold used to measure the achieved progress of the metric target. This table is the parent table of sn\_grc\_metric\_metric\_threshold.

</td></tr><tr><td>

Metric Threshold

 \[sn\_grc\_metric\_metric\_threshold\]

</td><td>

Parent table of sn\_grc\_metric\_metric\_threshold

</td></tr><tr><td>

Disclosure Summary

 \[sn\_esg\_disclosure\_summary\]

</td><td>

Disclosure summary report to display related information such as citation, metric, metric data associated to the disclosure. It will be refreshed via a daily scheduled job.

</td></tr><tr><td>

Disclosure

 \[sn\_esg\_disclosure\]

</td><td>

Disclosure of the company's E,S, and G data.

</td></tr><tr><td>

Related Document

 \[sn\_esg\_disclosure\_url\]

</td><td>

Related document URL associated with the disclosure.

</td></tr><tr><td>

Goal Activity Summary

 \[sn\_esg\_goal\_activity\_summary\]

</td><td>

Goal activity summary report to display related info in a summarized format. It will be refreshed via a scheduled job.

</td></tr><tr><td>

Goal Summary

 \[sn\_esg\_goal\_summary\]

</td><td>

Top level goal information along with related sub-goal and target info

</td></tr><tr><td>

Heatmap Chart Color

 \[sn\_esg\_heatmap\_chart\_color\]

</td><td>

ESG program manager is able to configure the color for heatmap chart

</td></tr><tr><td>

ISSB citation

 \[sn\_esg\_content\_issb\_citation\]

</td><td>

Holds ISSB framework and citation content data.

</td></tr><tr><td>

Analysis

 \[sn\_grc\_forecast\_analysis\]

</td><td>

Holds the details of forecast analysis for forecast context and forecast method.

</td></tr><tr><td>

Analysis context

 \[sn\_grc\_forecast\_context\]

</td><td>

Holds the details of forecast context like Name, Metric definition, Periods to forecast and Previous periods.

</td></tr><tr><td>

Analysis data

 \[sn\_grc\_forecast\_data\]

</td><td>

Table that stores forecast data for future periods data for given a context and analysis.

</td></tr><tr><td>

Analysis parameter data

 \[sn\_grc\_forecast\_parameter\_data\]

</td><td>

Table that stores operands forecast data for future periods data for given a context and analysis.

</td></tr><tr><td class="sub-head" colspan="2">

If Policy and Compliance Management is installed

</td></tr><tr><td>

Control to Goal

 \[sn\_esg\_m2m\_control\_goal\]

</td><td>

Association between Goal and Control

</td></tr><tr><td>

Control Objective to Goal

 \[sn\_esg\_m2m\_control\_obj\_goal\]

</td><td>

Association between Control Objective and Goal

</td></tr><tr><td>

Citation to Disclosure

 \[sn\_esg\_m2m\_disclosure\_citation\]

</td><td>

Association between Citation and Disclosure

</td></tr><tr><td>

Policy to Goal

 \[sn\_esg\_m2m\_policy\_goal\]

</td><td>

Association between Policy and Goal

</td></tr><tr><td>

Base metric definition to citation

 \[sn\_esg\_m2m\_base\_metric\_definition\_citation\]

</td><td>

Association between Base metric definition and Citation

</td></tr><tr><td>

Base metric definition to target

 \[sn\_esg\_m2m\_base\_metric\_definition\_target\]

</td><td>

Association between Base metric definition and Target

</td></tr><tr><td>

Base metric definition to goal

 \[sn\_esg\_m2m\_base\_metric\_definition\_goal\]

</td><td>

Association between Base metric definition and Goal

</td></tr><tr><td class="sub-head" colspan="2">

If Integrated Risk Management is installed

</td></tr><tr><td>

Risk to Goal

 \[sn\_esg\_m2m\_risk\_goal\]

</td><td>

Association between Risk and Goal

</td></tr><tr><td>

Risk Statement to Goal

 \[sn\_esg\_m2m\_risk\_statement\_goal\]

</td><td>

Association between Risk Statement and Goal

</td></tr><tr><td class="sub-head" colspan="2">

If Operational Sustainability Integration with Socialsuite is installed

</td></tr><tr><td>

Socialsuite import logsn\_osm\_ma\_import\_log

</td><td>

Relationship between imported material topic data and Socialsuite materiality assessments

</td></tr></tbody>
</table>## Properties

The following properties are installed with the Operational Sustainability Management application.

<table id="table_h5y_fpm_frb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.ui.sn\_esg\_disclosure\_activity.fields

</td><td>

Disclosure activity formatter fields.

</td></tr><tr><td>

glide.ui.sn\_esg\_material\_topic\_activity.fields

</td><td>

Material topic activity formatter fields.

</td></tr><tr><td>

sn\_esg.metric\_approval

</td><td>

Enables ESG administrators to define either the simple approval flow or the advanced approval flow for all the metrics and metric definitions. **Note:** This property is available only when the sn\_grc\_appr plugin is activated and must be set while configuring the Operational Sustainability Management application.

 The choices are as follows:-   **Simple**: By choosing this option, the Approval section will be enabled both on the manual metric definition form and within the metrics. Using this section, you can designate approvers directly on the metric definition form.
-   **Advanced**: When you choose this option, the Approval section will be unavailable on the manual metric definition form and the metric form. Instead, approval can be configured by setting the approval conditions, tables, and approvers in the GRC: Approver Configurator application. This application also allows you to define multiple levels of approvals. For more information see, Using Approver Configurator for setting up approvals.

</td></tr><tr><td>

sn\_esg\_scope3.historical\_years\_selector

</td><td>

Enables you to configure the number of historical years for which you want to view the data on the Scope 3 dashboard.

</td></tr></tbody>
</table>## Scheduled jobs

The following scheduled jobs are installed with the Operational Sustainability Management application.

|Name|Description|
|----|-----------|
|Generate ESG goals summary|This job executes daily at 12 AM. This job clears all existing goals summary and creates new goal summaries for all active goals classified as "environmental,social,governance".|
|Generate ESG disclosure summary|This job is executes daily once at 12AM. This job deletes existing summary and creates disclosure summary for all types of disclosure like goals,citations,metrics.|
|Calculate ESG license count|This Job executes daily at 11:00 PM. It calculates the license based on active data in base metric definition where domain area is ESG.|
|Generate ESG goals activity summary|This job executes periodically for every 12 hours. This job deletes the existing goal activity summary and creates new goal activity summary for all goals classified on "environmental, social, governance".|

**Parent Topic:**[Operational Sustainability Management \(formerly ESG\) reference](../concept/reference-data-esg.md)

