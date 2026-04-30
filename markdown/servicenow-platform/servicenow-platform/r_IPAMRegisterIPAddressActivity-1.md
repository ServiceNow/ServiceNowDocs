---
title: IPAM Register IP Address activity
description: The IPAM Register IP Address activity registers an IP address in a network using Infoblox IPAM.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
---

# IPAM Register IP Address activity

The IPAM Register IP Address activity registers an IP address in a network using Infoblox IPAM.

The output of this activity produces an InfoBlox IP address record that can be used for other IPAM functions in the format `fixedaddress/<encrypted key>:<reserved ip address>/<view>`.

The IPAM activities use the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) to manage IP addresses using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **IPAM**.

## Input variables

<table id="table_gfd_dnx_ft"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

InfobloxServer

</td><td>

Name of the Infoblox DDI Grid Server.

</td></tr><tr><td>

macAddress

</td><td>

Mac address of the computer for which this IP address is registered.

</td></tr><tr><td>

ipAddress

</td><td>

Specific IP address to register.

</td></tr><tr><td>

network

</td><td>

Address of the network containing the registered IP address.

</td></tr><tr><td>

restCredentials

</td><td>

The sys\_id of the REST credentials from the ServiceNow instance.

</td></tr><tr><td>

api\_version

</td><td>

Defines the version of WAPI to use for the integration endpoints. The default value is **2.0**. **Note:** This field is mandatory. If the field is empty, the orchestration activity will fail.

</td></tr><tr><td>

view

</td><td>

Name of the Infoblox network view. The default value is **default**. **Note:** If the field is empty, the operation is treated as happening in the default view.

</td></tr></tbody>
</table>## Output variables

|Variable|Description|
|--------|-----------|
|error|Displays the message for any REST error encountered.|
|IPAddressRecord|IPAM record of the registered IP address.|

## Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully registered the specified IP address.|
|Failure|Activity failed to register the specified IP address.|

