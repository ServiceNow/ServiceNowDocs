---
title: Define filters for My Requests
description: Define request filters to filter incidents, requests, or tasks under the Self-Service My Requests module in ServiceNow AI Platform, the My Requests widget in Service Portal, and the My Requests applet in the Now Mobile app.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Define filters for My Requests

Define request filters to filter incidents, requests, or tasks under the **Self-Service** &gt; **My Requests** module in ServiceNow AI Platform, the **My Requests** widget in Service Portal, and the My Requests applet in the Now® Mobile app.

## Before you begin

Role required: catalog\_admin or admin

Since the My Request Filter \[request\_filter\] table has been reparented to the Filter \[sys\_filter\] table, a few fields from the My Request Filter table have been migrated to fields in the Filter table. The **Short Description** field from the My Request Filter table has been migrated to the **Title** field in the Filter table. The **Table Name** field from the My Request Filter table has been migrated to the **Table** field in the Filter table.

**Note:** If the My Request Filter form is modified, the form still displays the **Short Description** and **Table Name** fields that are no longer valid. Delete these invalid fields from the form and add the **Title** and **Table** fields to the form.

## Procedure

1.  Navigate to **Service Catalog** &gt; **Catalog Administration** &gt; **My Request Filter**.

2.  On the form, fill the fields.

<table id="table_thv_lvy_sbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Name of the filter.

</td></tr><tr><td>

Table

</td><td>

Table on which the filter condition is applied.

</td></tr><tr><td>

Application

</td><td>

Application scope of the filter.

</td></tr><tr><td>

Active

</td><td>

If set to true, the filter is active.

</td></tr><tr><td>

Applies to

</td><td>

Interface for which the filter is applicable. Possible values:-   Desktop
-   Service Portal
-   Desktop/Service Portal
-   Mobile


</td></tr><tr><td>

Filter

</td><td>

Conditions to filter requests.

</td></tr><tr><td class="sub-head" colspan="2">

Portal Settings

</td></tr><tr><td colspan="2">

This section is displayed when the **Applies to** field is set to **Service Portal** or **All**.

</td></tr><tr><td>

Portal page

</td><td>

Portal page that opens when you click the request.

</td></tr><tr><td>

Primary field to display

</td><td>

Primary information displayed for the request.

</td></tr><tr><td>

Secondary fields to display

</td><td>

Secondary information displayed for the request.**Note:**

-   Add a maximum of three secondary fields.
-   Do not add an image field.
-   If the Request \[sc\_request\] table is selected, secondary field is not configured. If the request contains only one item, the Requested Item name is displayed. Else, it contains the requested item count.


</td></tr></tbody>
</table>3.  Click **Submit**.


**Parent Topic:**[Configuring Service Catalog](../concept/configuring-service-catalog.md)

**Related topics**  


[My Requests widget](https://www.servicenow.com/docs/access?context=my-request-widget-portal&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)

[Activate the page route map for the standard ticket page](https://www.servicenow.com/docs/access?context=config-pageroutemap-stpage&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)

