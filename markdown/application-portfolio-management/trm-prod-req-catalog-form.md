---
title: Request TRM Product form the Service Catalog form
description: The Request TRM Product form is used to submit a request for adding a new software or hardware product to the Technology Reference Model \(TRM\) library from the service catalog. Optionally, include one or more lifecycle records with the request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/trm-prod-req-catalog-form.html
release: australia
topic_type: reference
last_updated: "2026-07-24"
reading_time_minutes: 3
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Request TRM Product form the Service Catalog form

The Request TRM Product form is used to submit a request for adding a new software or hardware product to the Technology Reference Model \(TRM\) library from the service catalog. Optionally, include one or more lifecycle records with the request.

## Request TRM Product form fields

<table id="table_lhw_qbv_3zb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Company

</td><td>

Company of the software or hardware product. Look up and select a company from the list.

</td></tr><tr><td>

Category

</td><td>

Category of the product. Look up and select a category from the TRM Categories page.

</td></tr><tr><td>

Other categories

</td><td>

An additional level of category classification of the TRM product. This field is enabled only after a value is selected in the **Category** field.

</td></tr><tr><td>

Type

</td><td>

The type of the product. Select **Software** or **Hardware**. The fields displayed in the form change based on the type selected.**Note:** The fields **New Product**, **Software Product**, and **Hardware Product** are displayed only when you have the Software Asset Management Foundation plugin and the Hardware Asset Management plugin installed on your instance.

</td></tr><tr><td>

New Product

</td><td>

Select this check box if the product does not yet exist in the system. When selected, the **Software Product** or **Hardware Product** field is replaced by the **Name** field.

</td></tr><tr><td>

Software Product

</td><td>

Name of the software product. This field appears and is required when **Software** is selected in the **Type** field and the **Is New Product** check box is not selected. This field is available when the Software Asset Management Foundation plugin is installed on your instance.

</td></tr><tr><td>

Operating System

</td><td>

The operating system on which the product can be deployed. This field appears only when **Software** is selected in the **Type** field.

</td></tr><tr><td>

Hardware Product

</td><td>

Name of the hardware product. This field appears and is required when **Hardware** is selected in the **Type** field and the **New Product** check box is not selected. This field is available when the Hardware Asset Management plugin is installed on your instance.

</td></tr><tr><td>

Name

</td><td>

Name of the new software or hardware product. This field appears when the **New Product** check box is selected. This field replaces the **Software Product** or **Hardware Product** field.

</td></tr><tr><td>

Requested TRM Phase

</td><td>

Phase of the product. Look up and select a phase from the TRM Phases page. This field is required.

</td></tr><tr><td>

Business Justification

</td><td>

Business justification for the product request.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-reference.md)

**Related topics**  


[Request a TRM product from the service catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/add-edit-trm-prod-req.md)

[Request a TRM product lifecycle from the service catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/add-edit-trm-lifecycle-req.md)

[Request TRM Product Lifecycle form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/trm-product-lifecycle-request-form.md)

[Request a TRM product in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-request-a-trm-products.md)

[Request a TRM product lifecycle in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-request-a-trm-product-lifecycle.md)

[Create a TRM product in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-trm-prod-lifecycle.md)

[Create TRM product lifecycles in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-trm-prod-lifecycle-req.md)

