---
title: Infoblox network activities
description: The Infoblox network activities manage networks using an Infoblox DDI Grid Server.The Create Network activity creates new networks on a specified Infoblox server.The Get Network Details activity retrieves the information about a specific network on an Infoblox server.The Delete Network activity deletes a network from an Infoblox server.The List Registered Networks activity retrieves all the networks associated with an Infoblox server.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Infoblox DDI activity pack, Orchestration activity packs, Classic Orchestration, Data and Automation]
---

# Infoblox network activities

The Infoblox network activities manage networks using an Infoblox DDI Grid Server.

Use these activities to create, list, or delete networks on an Infoblox server.

**Parent Topic:**[Infoblox DDI activity pack](c_InfobloxDDIActivityPack.md)

## Create Network activity

The Create Network activity creates new networks on a specified Infoblox server.

The network activities use the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) to manage network addresses using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **Network**.

### Input variables

<table id="table_mm2_skw_ft"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

InfobloxServer

</td><td>

Name of the Infoblox DDI Grid Server.

</td></tr><tr><td>

network

</td><td>

Address of the network to create.

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
|NetworkCreated|Address of the network created.|
|error|Displays the message for any REST error encountered.|

### Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully created the network.|
|Failure|Activity failed to create the network.|

## Get Network Details activity

The Get Network Details activity retrieves the information about a specific network on an Infoblox server.

The network activities use the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) to manage network addresses using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **Network**.

### Input variables

<table id="table_tkp_ppq_ft"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

InfobloxServer

</td><td>

Name of the Infoblox DDI Grid Server.

</td></tr><tr><td>

network

</td><td>

Address of the network whose details you want to see.

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

The output variables from this activity are objects on the Infoblox server used to identify network details. For more information, refer to the Infoblox documentation.

<table id="table_rn1_qqq_ft"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Displays the message for any REST error encountered.

</td></tr><tr><td>

NetworkOptions

</td><td>

The **NetworkOptions** array contains these attributes:-   **reference**: Reference value for the network requested. This value is in the form of `network/ZG5zLm5ldHdvcmskMTAuMS4wLjAvMTYvMA:10.1.0.0%2F1`
-   **options**: The **options** array contains these attributes:
    -   **name**: Name of the network option returned, such as **domain-name-server**.
    -   **num**: Index number of the option. For example, the index for **domain-name-server** is **6**.
    -   **use\_option**: Indicates whether a DHCP option is used at that level in the network heirarchy. Set this value to **True** to override the Grid Level DHCP option with this option at the network level.
    -   **value**: Value to use for this option. For example, the value for the **domain-name-server** option is the IP address of the server machine.
    -   **vendor\_class**: The class of the network object. The options are **DHCP**, **DNS**, or **IPAM**.

</td></tr></tbody>
</table>### Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully retrieved network details from the Infoblox server.|
|Failure|Activity failed to retrieve network details from the Infoblox server.|

## Delete Network activity

The Delete Network activity deletes a network from an Infoblox server.

The network activities use the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) to manage network addresses using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **Network**.

### Input variables

<table id="table_wyl_phq_ft"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

InfobloxServer

</td><td>

Name of the Infoblox DDI Grid Server.

</td></tr><tr><td>

networkToDelete

</td><td>

Reference number of the network to delete from the Infoblox server. You can obtain this value either by using the List Registered Networks activity or when creating a network with the Create Network activity. An example of the network reference value is: **network/ZG5zLm5ldHdvcmskMTUuMC40NS4wLzI0LzA:15.0.45.0/24/default**.

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
|DeletedNetwork|Reference number of the deleted network from the Infoblox server.|
|error|Displays the message for any REST error encountered.|

### Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully deleted the network.|
|Failure|Activity failed to delete the network.|

## List Registered Networks activity

The List Registered Networks activity retrieves all the networks associated with an Infoblox server.

The network activities use the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) to manage network addresses using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **Network**.

### Input variables

<table id="table_mch_cyp_ft"><thead><tr><th>

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
|reference|Reference value of a registered network.|
|network|Network address.|
|network\_view|Routing doman associated with the network returned.|
|error|Displays the message for any REST error encountered.|

### Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully retrieved the list of registered networks available on the Infoblox server.|
|Failure|Activity failed to retrieve the list of registered networks available on the Infoblox server.|

