---
title: Infoblox IPAM activities
description: The Infoblox IPAM activities manage IP addresses in your network using an Infoblox DDI Grid Server.The IPAM Register IP Address activity registers an IP address in a network using Infoblox IPAM.The IPAM Reserve IP Address activity reserves an IP address in a network using Infoblox IPAM.The IPAM List IP Reservations activity returns an array of all IP Address within the named InfoBlox Server.The IPAM Delete activity deletes an IP Address within a named InfoBlox server.
locale: en-US
release: zurich
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Infoblox DDI activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Infoblox IPAM activities

The Infoblox IPAM activities manage IP addresses in your network using an Infoblox DDI Grid Server.

Use these activities to register, reserve, list, or delete IP addresses.

**Parent Topic:**[Infoblox DDI activity pack](c_InfobloxDDIActivityPack.md)

## IPAM Register IP Address activity

The IPAM Register IP Address activity registers an IP address in a network using Infoblox IPAM.

The output of this activity produces an InfoBlox IP address record that can be used for other IPAM functions in the format `fixedaddress/<encrypted key>:<reserved ip address>/<view>`.

The IPAM activities use the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) to manage IP addresses using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **IPAM**.

### Input variables

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
</table>### Output variables

|Variable|Description|
|--------|-----------|
|error|Displays the message for any REST error encountered.|
|IPAddressRecord|IPAM record of the registered IP address.|

### Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully registered the specified IP address.|
|Failure|Activity failed to register the specified IP address.|

## IPAM Reserve IP Address activity

The IPAM Reserve IP Address activity reserves an IP address in a network using Infoblox IPAM.

The output of this activity produces an InfoBlox IP address record that can be used for other IPAM functions in the format `fixedaddress/<encrypted key>:<reserved ip address>/<view>`.

The IPAM activities use the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) to manage IP addresses using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **IPAM**.

### Input variables

<table id="table_p2w_pjx_ft"><thead><tr><th>

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

Mac address of the computer for which this IP address is reserved.

</td></tr><tr><td>

network

</td><td>

Address of the network containing the reserved IP address. The Infoblox server reserves the next available IP address from this network.

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
|error|Displays the message for any REST error encountered.|
|IPAddressRecord|IPAM record of the reserved IP address.|
|IPAddress|Selected IP address to reserve.|

### Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully reserved the specified IP address.|
|Failure|Activity failed to reserve the specified IP address.|

## IPAM List IP Reservations activity

The IPAM List IP Reservations activity returns an array of all IP Address within the named InfoBlox Server.

The IPAM activities use the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) to manage IP addresses using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **IPAM**.

### Input variables

<table id="table_ufd_2bx_ft"><thead><tr><th>

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

The output of this activity produces an array of reserved IP addresses in the format `fixedaddress/<encrypted key>:<reserved ip address>/<view>`.

|Variable|Description|
|--------|-----------|
|reference|Reference value of a reserved IP address contained in an array of addresses, such as `fixedaddress/ZG5zLmZpeGVkX2FkZHJlc3MkMTAuMC4xMDMuMTEuMC4u:0.0.0.11/default" ipv4addr: "0.0.0.11"`|
|ipv4addr|The reserved IPv4 address.|
|network\_view|Routing domain associated with the network returned.|
|error|Displays the message for any REST error encountered.|

### Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully retrieved the list of reserved IP addresses from the Infoblox server.|
|Failure|Activity failed to retrieve the list of reserved IP addresses from the Infoblox server.|

## IPAM Delete activity

The IPAM Delete activity deletes an IP Address within a named InfoBlox server.

The IPAM activities use the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) to manage IP addresses using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **IPAM**.

### Input variables

<table id="table_onx_3ww_ft"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

InfobloxServer

</td><td>

Name of the Infoblox DDI Grid Server.

</td></tr><tr><td>

itemToDelete

</td><td>

The IP address to delete, in the format `fixedaddress/<encrypted key>:<reserved ip address>/<view>`.

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
|DeletedRecord|IPAM record of the deleted IP address.|
|error|Displays the message for any REST error encountered.|

### Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully deleted the specified IP address.|
|Failure|Activity failed to delete the specified IP address.|

