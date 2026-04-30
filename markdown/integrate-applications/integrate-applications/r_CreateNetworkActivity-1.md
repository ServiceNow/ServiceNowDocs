---
title: Create Network activity
description: The Create Network activity creates new networks on a specified Infoblox server.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Create Network activity

The Create Network activity creates new networks on a specified Infoblox server.

The network activities use the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) to manage network addresses using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **Network**.

## Input variables

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
</table>## Output variables

|Variable|Description|
|--------|-----------|
|NetworkCreated|Address of the network created.|
|error|Displays the message for any REST error encountered.|

## Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully created the network.|
|Failure|Activity failed to create the network.|

