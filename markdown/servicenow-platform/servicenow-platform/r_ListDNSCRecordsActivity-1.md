---
title: List DNS C-records activity
description: The List DNS C-records activity retrieves all canonical \(CNAME\) records from a specified Infoblox server.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
---

# List DNS C-records activity

The List DNS C-records activity retrieves all canonical \(CNAME\) records from a specified Infoblox server.

The DNS activities use the [REST web service activity](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) template to manage DNS records using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **DNS**.

## Input variables

<table id="table_fxb_kvh_ht"><thead><tr><th>

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
</table>## Output variables

|Variable|Description|
|--------|-----------|
|error|Displays the message for any REST error encountered.|
|reference|Reference value for a DNS CNAME record, such as: `record:cname/ZG5zLmJpbmRfY25hbWUkLl9kZWZhdWx0LmNvbS50ZXN0LmNuYW1l:cname.test.com/default`|
|cannonicalName|CNAME record.|
|name|Name of the network option returned, such as **domain-name-server**.|
|view|The assigned view of the DNS data. A given zone can have multiple views, which are accessed depending on the IP address of the source of the query. The **default** view of DNS data for this activity is the network view.|

## Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully listed the DNS C records.|
|Failure|Activity failed to list the DNS C records.|

