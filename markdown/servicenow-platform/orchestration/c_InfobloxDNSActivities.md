---
title: Infoblox DNS activities
description: The Infoblox DNS activities manage DNS records in your network using an Infoblox DDI Grid Server.The List DNS C-records activity retrieves all canonical \(CNAME\) records from a specified Infoblox server.The Register DNS A-record activity creates a DNS A record on a specified Infoblox server.The Register DNS C-Record activity creates a DNS canonical \(CNAME\) record on a specified Infoblox server.The List DNS Record activity generates a list of all the DNS entries on a specific InfoBlox server.The DNS Delete activity deletes DNS records of any type from in Infoblox server, such as C and A records.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Infoblox DDI activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Infoblox DNS activities

The Infoblox DNS activities manage DNS records in your network using an Infoblox DDI Grid Server.

Use these activities to register, list, or delete DNS records managed on an Infoblox server.

**Parent Topic:**[Infoblox DDI activity pack](c_InfobloxDDIActivityPack.md)

## List DNS C-records activity

The List DNS C-records activity retrieves all canonical \(CNAME\) records from a specified Infoblox server.

The DNS activities use the [REST web service activity](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) template to manage DNS records using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **DNS**.

### Input variables

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
</table>### Output variables

|Variable|Description|
|--------|-----------|
|error|Displays the message for any REST error encountered.|
|reference|Reference value for a DNS CNAME record, such as: `record:cname/ZG5zLmJpbmRfY25hbWUkLl9kZWZhdWx0LmNvbS50ZXN0LmNuYW1l:cname.test.com/default`|
|cannonicalName|CNAME record.|
|name|Name of the network option returned, such as **domain-name-server**.|
|view|The assigned view of the DNS data. A given zone can have multiple views, which are accessed depending on the IP address of the source of the query. The **default** view of DNS data for this activity is the network view.|

### Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully listed the DNS C records.|
|Failure|Activity failed to list the DNS C records.|

## Register DNS A-record activity

The Register DNS A-record activity creates a DNS A record on a specified Infoblox server.

The DNS activities use the [REST web service activity](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) template to manage DNS records using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **DNS**.

### Input variables

<table id="table_jrl_xrh_ht"><thead><tr><th>

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

Address of the network containing the IP address to register in the record.

</td></tr><tr><td>

hostName

</td><td>

Name of the actual server machine associate with the IP address in this record.

</td></tr><tr><td>

zone

</td><td>

The DNS zone associated with the record being created.

</td></tr><tr><td>

ipAddress

</td><td>

Specific IP address registered in this record.

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
|DNSARecord|Name of the record registered, expressed in the format: **record:host/&lt;encrypted code&gt;:&lt;network name&gt;/default**.|

### Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully created the DNS A record.|
|Failure|Activity failed to create the DNS A record.|

## Register DNS C-Record activity

The Register DNS C-Record activity creates a DNS canonical \(CNAME\) record on a specified Infoblox server.

The DNS activities use the [REST web service activity](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) template to manage DNS records using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **DNS**.

### Input variables

<table id="table_qsm_2nh_ht"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

InfobloxServer

</td><td>

Name of the Infoblox DDI Grid Server.

</td></tr><tr><td>

cname

</td><td>

The DNS cannonical record to create, as expressed by the **c\_name** value.

</td></tr><tr><td>

recordName

</td><td>

Name of the record to create.

</td></tr><tr><td>

zone

</td><td>

The DNS zone containing the cannonical record to create.

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

|Variable|Desctiption|
|--------|-----------|
|error|Displays the message for any REST error encountered.|
|DNSCRecord|Name of the CNAME record registered, expressed in the format: **record:cname/&lt;encrypted code&gt;:&lt;network name&gt;/default**.|

### Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully created the cannonical DNS record.|
|Failure|Activity failed to create the cannonical DNS record.|

## List DNS Record activity

The List DNS Record activity generates a list of all the DNS entries on a specific InfoBlox server.

The DNS activities use the [REST web service activity](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) template to manage DNS records using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **DNS**.

### Input variables

<table id="table_u5f_t1h_ht"><thead><tr><th>

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
|reference|Reference value for a DNS record, such as: `record:cname/ZG5zLmJpbmRfY25hbWUkLl9kZWZhdWx0LmNvbS50ZXN0LmNuYW1l:cname.test.com/default`|
|configure\_for\_dhcp|Returns the status of a DHCP fixed address object.|
|host|Host machine with which the DNS record is associated.|
|ipv4addr|The reserved IPv4 address associated with a DNS record.|
|name|Name of the network option returned. For example, the name of the DNS record object from the **reference** example is **cname.test.com**.|
|view|The assigned view of the DNS data. A given zone can have multiple views, which are accessed depending on the IP address of the source of the query. The **default** view of DNS data for this activity is the network view.|
|error|Displays the message for any REST error encountered.|

### Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully listed all the available DNS record.|
|Failure|Activity failed to list the available DNS record.|

## DNS Delete activity

The DNS Delete activity deletes DNS records of any type from in Infoblox server, such as C and A records.

The DNS activities use the [REST web service activity](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#) template to manage DNS records using an Infoblox DDI Grid Server. These activities are configured to use a MID Server with REST capabilities.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Infoblox DDI** &gt; **DNS**.

**Note:** It is faster to create a new record than recover one that has been deleted.

### Input variables

<table id="table_orf_4rg_ht"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

InfobloxServer

</td><td>

Name of the Infoblox DDI Grid Server.

</td></tr><tr><td>

RecordToDelete

</td><td>

Name of the DNS record to delete. The record is expressed in this format:**record:cname/ZG5zLmJpbmRfY25hbWUkLl9kZWZhdWx0LmNvbS50ZXN0LmNuYW1l:cname.test.com/default**

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
|DeletedRecord|Name of the deleted DNS record.|
|error|Displays the message for any REST error encountered.|

### Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity successfully deleted the specified DNS record.|
|Failure|Activity failed to delete the specified DNS record.|

