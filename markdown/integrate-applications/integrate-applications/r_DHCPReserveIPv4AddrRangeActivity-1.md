---
title: DHCP Reserve IP v4 Address Range activity
description: The DHCP Reserve IP v4 Address Range activity reserves an IP address range for DHCP use.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
---

# DHCP Reserve IP v4 Address Range activity

The DHCP Reserve IP v4 Address Range activity reserves an IP address range for DHCP use.

The DHCP activities use the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) to manage IP addresses using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **DHCP**.

## Input variables

<table id="table_ens_bk3_ht"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

InfobloxServer

</td><td>

Name of the Infoblox DDI Grid Server.

</td></tr><tr><td>

startIpAddress

</td><td>

Beginning IPv4 address of the range to reserve.

</td></tr><tr><td>

endIpAddress

</td><td>

Ending IPv4 address of the range to reserve.

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
|DHCPIpAddressRange|Range of reserved IPv4 addresses.|
|error|Displays the message for any REST error encountered.|

## Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully reserved the specified IPv4 address range.|
|Failure|Activity failed to reserve the specified IPv4 address range.|

