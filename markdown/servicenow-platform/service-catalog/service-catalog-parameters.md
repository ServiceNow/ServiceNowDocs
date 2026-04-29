---
title: Service Catalog parameters
description: You can use the Service Catalog parameters to identify the parent mapping configuration for a request, and join the service catalog flow from any other flow. For example, from an incident flow, you can create a request, and associate the request with the incident.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service Catalog parameters

You can use the Service Catalog parameters to identify the parent mapping configuration for a request, and join the service catalog flow from any other flow. For example, from an incident flow, you can create a request, and associate the request with the incident.

These parameters are passed in the application URL.

<table id="table_lwt_xsv_1cb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sysparm\_parent\_sys\_id

</td><td>

sys\_id of the source record that is passed to the target record generated from it.Format is **sysparm\_parent\_sys\_id**= &lt;sys\_id of the parent&gt;. For example, sysparm\_parent\_sys\_id=85071a1347c12200e0ef563dbb9a71c1.

</td></tr><tr><td>

sysparm\_parent\_table

</td><td>

Name of the parent table from which the catalog request is created.Format is **sysparm\_parent\_table**=&lt;name of the parent table&gt;. For example, sysparm\_parent\_table=incident.

</td></tr><tr><td>

sysparm\_view

</td><td>

Type of the catalog view.Format is **sysparm\_view**=&lt;name of the catalog view&gt;. For example, sysparm\_view=catalog\_default.

 **Note:** This is only applicable in Platform.

</td></tr><tr><td>

sysparm\_processing\_hint

</td><td>

Specifies a processing hint.Format is **sysparm\_processing\_hint**=setfield:request.parent=&lt;incident sys\_id&gt;. For example, sysparm\_processing\_hint=setfield:request.parent=85071a1347c12200e0ef563dbb9a71c1.

 **Note:** If specified, this parameter overrides the configuration in the **Request Parent Mapping** sub-module.

</td></tr></tbody>
</table>**Parent Topic:**[Service Catalog Reference](../concept/service-catalog-reference.md)

**Related topics**  


[Create a request from an incident](https://www.servicenow.com/docs/access?context=create-request-from-incident&version=australia&pubname=australia-it-service-management&ft:locale=en-US)

