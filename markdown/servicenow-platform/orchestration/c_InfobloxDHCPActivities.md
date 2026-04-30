---
title: Infoblox DHCP activities
description: The Infoblox DHCP activities manage the IP addresses reserved for DHCP in your network.The DHCP Reserve IP v4 Address Range activity reserves an IP address range for DHCP use.The DHCP Delete IP Reservation activity deletes IP reservations in DHCP using either an IPv4 or IPv6 address range.The DHCP List IP Reservations activity generates a list of all the DHCP range reservations on a specific InfoBlox server.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Infoblox DDI activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Infoblox DHCP activities

The Infoblox DHCP activities manage the IP addresses reserved for DHCP in your network.

Use these activities to reserve, list, or delete IP addresses that are used for DHCP assignment in your network.

**Parent Topic:**[Infoblox DDI activity pack](c_InfobloxDDIActivityPack.md)

## DHCP Reserve IP v4 Address Range activity

The DHCP Reserve IP v4 Address Range activity reserves an IP address range for DHCP use.

The DHCP activities use the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) to manage IP addresses using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **DHCP**.

### Input variables

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
</table>### Output variables

|Variable|Description|
|--------|-----------|
|DHCPIpAddressRange|Range of reserved IPv4 addresses.|
|error|Displays the message for any REST error encountered.|

### Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully reserved the specified IPv4 address range.|
|Failure|Activity failed to reserve the specified IPv4 address range.|

## DHCP Delete IP Reservation activity

The DHCP Delete IP Reservation activity deletes IP reservations in DHCP using either an IPv4 or IPv6 address range.

An automation can obtain an Infoblox DHCP object to delete from either of these activities:

-   [DHCP List IP Reservations](c_InfobloxDHCPActivities.md#)
-   [DHCP Reserve IPv4 Address Range](c_InfobloxDHCPActivities.md#)

The DHCP activities use the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) to manage IP addresses using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **DHCP**.

### Input variables

<table id="table_p5r_zf3_ht"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

InfobloxServer

</td><td>

Name of the Infoblox DDI Grid Server.

</td></tr><tr><td>

ipToDelete

</td><td>

IP address range to delete, in the form: `range/<encrypted code>:<start range>/<end range>/default`

</td></tr><tr><td>

restCredentials

</td><td>

The sys\_id of the REST credentials from the ServiceNow instance.

</td></tr><tr><td>

api\_version

</td><td>

Defines the version of WAPI to use for the integration endpoints. The default value is **2.0**. **Note:** This field is mandatory. If the field is empty, the orchestration activity will fail.

</td></tr></tbody>
</table>### Output variables

|Variable|Description|
|--------|-----------|
|DHCPDeletedIpRange|Range of deleted IP addresses.|
|error|Displays the message for any REST error encountered.|

### Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully deleted the specified IP address range.|
|Failure|Activity failed to delete the specified IP address range.|

## DHCP List IP Reservations activity

The DHCP List IP Reservations activity generates a list of all the DHCP range reservations on a specific InfoBlox server.

The DHCP activities use the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) to manage IP addresses using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **DHCP**.

### Input variables

<table id="table_jcn_m23_ht"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

InfobloxServer

</td><td>

Name of the Infoblox DDI Grid Server.

</td></tr><tr><td>

restCredentials

</td><td>

The sys\_id of the REST credentials from the ServiceNow instance.

</td></tr><tr><td>

api\_version

</td><td>

Defines the version of WAPI to use for the integration endpoints. The default value is **2.0**. **Note:** This field is mandatory. If field is empty, the orchestration activity will fail.

</td></tr><tr><td>

view

</td><td>

Name of the Infoblox network view. The default value is **default**. **Note:** If the field is empty, the operation is treated as happening with no view and returns the values with data from all views.

</td></tr></tbody>
</table>### Output variables

|Variable|Description|
|--------|-----------|
|reference|Reference value for an array of DHCP address ranges in this format: `range/<encrypted code>:<start range>/<end range>/default`|
|network|Address of the network containing the IP address range.|
|network\_view|Routing doman associated with the network returned.|

### Conditions

|Variables|Description|
|---------|-----------|
|Success|Activity successfully returned an array of DHCP IP address ranges.|
|Failure|Activity failed to return an array of DHCP IP address ranges.|

