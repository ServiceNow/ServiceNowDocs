---
title: Configure a metric definition
description: Configure a metric definition to create or modify the existing base system CI metrics displayed on the Investigation tab.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Setting up Investigation Framework in Service Operations Workspace, Setting up integrations in Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure a metric definition

Configure a metric definition to create or modify the existing base system CI metrics displayed on the Investigation tab.

## Before you begin

Role required: sn\_cimaf.sn\_cimaf\_admin

## Procedure

1.  Navigate to **All** &gt; **Metrics and CI Actions Framework** &gt; **Administration** &gt; **Metric Definitions**.

    These following existing metric definition tables are displayed:

    -   Asset usage
    -   Installed Applications
    -   Logged-in users
    -   Running processes
    -   Services
    -   System Information \(dsregcmd\)
    -   System Information \(msinfo32\)
    -   System overview
2.  Create a metric definition record.

    You can also select an existing metric definition record to modify the record.

    1.  Select **New**.

    2.  On the Metric definition form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the metric.|
        |Active|Option to activate the metric definition.|
        |CI Class|Particular CI class for which the metric is applicable.|
        |Description|Description of the metric definition.|
        |Schema|High-level structure in which the metrics retrieved from the provider are stored in the metric table.|

    3.  Select **Submit**.

3.  On the Adapter Configuration related list, create a record.

    Adapter configuration for the metric definition enables you to define the provider and the query, as well as transform flows or scripts.

    1.  Select **New**.

        You can also select an existing adapter configuration record to modify the record.

    2.  On the Adapter Configuration form, fill in the fields.

<table id="table_jv3_s42_cxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the adapter configuration.

</td></tr><tr><td>

Metric Definition

</td><td>

Metric definition for which the adapter configuration is created.

</td></tr><tr><td>

Provider

</td><td>

Provider for metrics, such as Agent Client Collector or Microsoft Endpoint Configuration Manager for Investigation.

</td></tr><tr><td>

Order

</td><td>

Sequence order in which the adapter configuration record applies to the metric definition when there are multiple configurations available.**Note:** The first applicable adapter configuration that is based on the **Order** value is only considered for fetching the metrics.

</td></tr><tr><td>

Duplicate request time limit \(seconds\)

</td><td>

Sets the number of seconds to prevent duplicate metric requests when one is already in progress.

</td></tr><tr><td class="sub-head" colspan="2">

Query

</td></tr><tr><td>

Query Action

</td><td>

Type of action that is used to retrieve the metric data from the provider. The value can be a flow or script.

</td></tr><tr><td>

Query Flow/script

</td><td>

Flow or script that is used to retrieve the metric from the provider.**Note:** In case no flow or script is defined, the default query flow of the provider is considered.

</td></tr><tr><td class="sub-head" colspan="2">

Transform

</td></tr><tr><td>

Transform Action

</td><td>

Type of action that is used to transform the metric data, which is retrieved by the provider, to output. The value can be a flow or script.

</td></tr><tr><td>

Transform Flow/script

</td><td>

Flow or script that is used to transform the metric data, which is retrieved by the provider, to output.**Note:** In case no flow or script is defined, the default transform flow of the provider is considered.

</td></tr></tbody>
</table>    3.  Select **Submit**.

4.  On the Provider Specific Adapter Configuration related list, create a record.

    Provider Specific Adapter Configuration table enables you to define and configure adapter configuration, such as query or command, for a specific provider, such as Agent Client Collector \(ACC\) or Microsoft Endpoint Configuration Manager \(MECM\) for Investigation.

    1.  Select **New**.

        You can also select an existing provider specific adapter configuration record to modify the record.

        A list of specific provider action configuration table is displayed, such as ACC Action Configuration and MECM Action Configuration.

    2.  Select the provider for which you want to create an adapter configuration.

    3.  On the Provider Specific Adapter Configuration form, fill in the fields.

<table id="table_m3t_bw2_cxb"><thead><tr><th>

Field

</th><th>

Option

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the provider specific adapter configuration.

</td></tr><tr><td>

Adapter Configuration

</td><td>

Adapter configuration for which the provider specific adapter configuration is created.

</td></tr><tr><td>

Active

</td><td>

Option to activate the configuration.

</td></tr><tr><td>

Check Definition

</td><td>

Check definition that is used for the execution and handling the output of the command or query. For example, app-ci-metrics-acc-adapter.osquery.**Note:** This is applicable only if the provider is Agent Client Collector for Investigation.

</td></tr><tr><td>

Query/Command

</td><td>

Query or command that the provider runs on the end machine.**Note:** This is applicable only if the provider is Agent Client Collector for Investigation.

</td></tr><tr><td>

Action Input

</td><td>

Input parameters required by flow action.**Note:** This field is applicable only if the provider is Microsoft Endpoint Configuration Manager for Investigation.

</td></tr><tr><td>

Flow Action

</td><td>

MECM spoke flow action to perform the read operation on the MECM device.**Note:** This field is applicable only if the provider is Microsoft Endpoint Configuration Manager for Investigation.

</td></tr><tr><td>

Output Flow Action

</td><td>

MECM spoke flow action to look up the read operation response from the MECM server.**Note:** This field is applicable only if the provider is Microsoft Endpoint Configuration Manager for Investigation.

</td></tr></tbody>
</table>    4.  Select **Submit**.

5.  On the Adapter Applicability Rule related list, create a rule.

    Adapter Applicability Rule table enables you to configure which CIs apply to the selected adapter configuration.

    1.  Select **New**.

        You can also select an existing adapter applicability rule record to modify the record.

    2.  On the Adapter Applicability Rule form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Adapter Configuration|Adapter configuration that applies to the adapter applicability rule.|
        |CI Conditions|
        |CI Class|CI class that applies the adapter configuration.|
        |Allow matching CI class extension|Option to apply the configurations to the child of a CI class.|
        |CI conditions|Condition builder to configure which CIs apply to the adapter configuration.|

    3.  Select **Submit**.


## What to do next

After the new metric definition is created, perform the UI configuration for displaying the metric definition on the Investigate tab of the incident record page. You must get the sys\_id of the metric definition and add it to the `sn_sow.SOWInvestigateConfig` script. You can also customize the display of the metric definition, such as the labels, units, and threshold values. For more information, see [Customize the Investigate tab](../concept/customize-the-incident-record-page.md#).

**Parent Topic:**[Setting up Investigation Framework in Service Operations Workspace](../concept/set-up-investigate.md)

