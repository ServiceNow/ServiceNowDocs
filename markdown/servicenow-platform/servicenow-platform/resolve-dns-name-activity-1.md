---
title: Resolve DNS Name activity
description: The Resolve DNS Name activity takes an IP address or a fully qualified domain name \(FQDN\), which it resolves into one or more IP addresses.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
---

# Resolve DNS Name activity

The Resolve DNS Name activity takes an IP address or a fully qualified domain name \(FQDN\), which it resolves into one or more IP addresses.

The domain name is sent through the MID Server to the domain name system \(DNS\) to resolve the name. If a single IP address is returned, it is stored in two variables:*resolved\_ip* and *resolved\_ips*. If multiple IP addresses are returned, the first IP address is stored in the *resolved\_ip* variable, and all the addresses are stored in the *resolved\_ips* variable. If an IP address is provided instead of an FQDN, this address is output directly to both variables. Your ServiceNow instance must have access to a MID Server configured to use Resolve DNS to run this activity.

This activity replaces an activity by the same name available in releases prior to Istanbul. If you have a workflow created in a previous version that uses the deprecated activity, your workflow will continue to work normally after upgrading to Istanbul. However, all new workflows must use the custom version of this activity. This activity was built with the [Probe activity template](../../orchestration-activity-designer/task/t_CreateAProbeActivity.md#), which gives workflow administrators the ability to store input and output variables in the [databus](../../orchestration-activity-designer/concept/c_OrchestrationDatabus.md#).

## Input variables

|Variable|Description|
|--------|-----------|
|FQDN|The fully qualified domain name to resolve or an IP address.|

## Output variables

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
</table>## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully resolved the DNS name.|
|Failure|Activity failed to resolve the DNS name.|

