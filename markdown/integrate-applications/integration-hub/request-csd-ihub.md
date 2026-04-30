---
title: Request client software distribution
description: Client software distribution requires the Orchestration - Client Software Distribution plugin \(com.snc.orchestration.client\_sf\_distribution\), which is available by request with a subscription to Integration Hub.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Client Software Distribution, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Request client software distribution

Client software distribution requires the Orchestration - Client Software Distribution plugin \(com.snc.orchestration.client\_sf\_distribution\), which is available by request with a subscription to Integration Hub.

## Before you begin

Role required: admin

## About this task

The Client Software Distribution plugin activates the System Center Configuration Manager plugin that contains the [Microsoft SCCM spoke](../concept/microsoft-sccm-spoke.md) actions to deploy or revoke software using an SCCM server. For additional plugin dependencies, see [Plugins installed with client software distribution](../reference/csd-installed-plugins.md).

**Note:** The Client Software Distribution plugin runs in its own application scope.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Click **Request Plugin**.

3.  On the form, fill in the fields.

<table id="table_awx_bhf_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Target Instance

</td><td>

Instance on which to activate the plugin.

</td></tr><tr><td>

Plugin Name

</td><td>

Name of the plugin to activate.

</td></tr><tr><td>

Specify the date and time you would like this plugin to be enabled

</td><td>

Date and time that must be at least two business days from the current time.

 **Note:** Plugins are activated in two batches each business day in the Pacific time zone, once in the morning and once in the evening. If the plugin must be activated at a specific time, enter the request in the **Reason/Comments** field.

</td></tr><tr><td>

Reason/Comments

</td><td>

Information that would be helpful for the ServiceNow personnel who are activating the plugin. For example, if you need the plugin activated at a specific time instead of during one of the default activation windows, specify it in the comments.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Client Software Distribution using Integration Hub](../concept/csd-integrationhub.md)

