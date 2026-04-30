---
title: Probe activity pack
description: Orchestration provides an activity pack customized using the ServiceNow activity designer that runs probes on target hosts to return specific information.The Resolve DNS Name activity takes an IP address or a fully qualified domain name \(FQDN\), which it resolves into one or more IP addresses.The SNMP Query activity queries an SNMP device.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Probe activity pack

Orchestration provides an activity pack customized using the ServiceNow activity designer that runs probes on target hosts to return specific information.

These custom activities were built with the [Create a probe activity](../../orchestration-activity-designer/task/t_CreateAProbeActivity.md#), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

To use the custom probe activities, you must [request activation](../task/t_ActivateAnActivityPack.md) of the Orchestration - Probe plugin.

**Parent Topic:**[Orchestration activity packs](c_OrchestrationActivityPacks.md)

## Resolve DNS Name activity

The Resolve DNS Name activity takes an IP address or a fully qualified domain name \(FQDN\), which it resolves into one or more IP addresses.

The domain name is sent through the MID Server to the domain name system \(DNS\) to resolve the name. If a single IP address is returned, it is stored in two variables:*resolved\_ip* and *resolved\_ips*. If multiple IP addresses are returned, the first IP address is stored in the *resolved\_ip* variable, and all the addresses are stored in the *resolved\_ips* variable. If an IP address is provided instead of an FQDN, this address is output directly to both variables. Your ServiceNow instance must have access to a MID Server configured to use Resolve DNS to run this activity.

This activity replaces an activity by the same name available in releases prior to Istanbul. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Istanbul. However, all new workflows must use the custom version of this activity. This activity was built with the [Probe activity template](../../orchestration-activity-designer/task/t_CreateAProbeActivity.md#), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

### Input variables

|Variable|Description|
|--------|-----------|
|FQDN|The fully qualified domain name to resolve or an IP address.|

### Output variables

<table id="table_htz_4sk_pw"><thead><tr><th>

Variable

</th><th>

Desctiption

</th></tr></thead><tbody><tr><td>

ip

</td><td>

The first IP address of the resolved DNS name.

</td></tr><tr><td>

ips

</td><td>

Comma separated list of resolved IP addresses.

</td></tr><tr><td>

result

</td><td>

One of the following:-   **resolved**: Able to resolve the sprcified DNS name.
-   **unresolved**: Unable to resolve the specified DNS name.

</td></tr></tbody>
</table>### Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully resolved the DNS name.|
|Failure|Activity failed to resolve the DNS name.|

## SNMP Query activity

The SNMP Query activity queries an SNMP device.

Your ServiceNow instance must have access to a MID Server configured to use SNMP to run this activity.

This activity replaces an activity by the same name available in releases prior to Istanbul. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Istanbul. However, all new workflows must use the custom version of this activity. This activity was built with the [Probe activity template](../../orchestration-activity-designer/task/t_CreateAProbeActivity.md#), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

### Input variables

|Variable|Description|
|--------|-----------|
|hostname|Hostname or IP address of the SNMP device being queried.|
|oids|A list of unique object identifiers used to identify SNMP devices.|

### Output variables

|Variable|Description|
|--------|-----------|
|description|Description of the SNMP object.|
|timeout|Boolean value indicating whether or not the query timed out.|
|error|Indicates any error that occurred. If no error occurred, this value is null.|
|oid\_data|An array of data objects for all unique object identifiers.|

### Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully ran the query on the target device.|
|Failure|Activity failed to run the query on the target device. Failure could be caused by invalid credentials or a device that is not accessible.|

