---
title: Request TRM product form
description: The Request TRM product form is used to submit a request to add a new software or hardware product to the Technology Reference Model \(TRM\) library. Optionally, add lifecycle records as part of the same request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-trm-product-request-form.html
release: australia
topic_type: reference
last_updated: "2026-07-22"
reading_time_minutes: 1
breadcrumb: [Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Request TRM product form

The Request TRM product form is used to submit a request to add a new software or hardware product to the Technology Reference Model \(TRM\) library. Optionally, add lifecycle records as part of the same request.

## Details tab

<table id="trm_product_request_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

A unique, auto-generated identification number for the product request.

</td></tr><tr><td>

Approval

</td><td>

Status of the approval. Choices include:-   Not yet requested
-   Requested
-   Approved
-   Rejected

</td></tr><tr><td>

Company

</td><td>

Company of the software or hardware product. Look up and select a company name from the list. This field is required.

</td></tr><tr><td>

Category

</td><td>

Category of the product. Look up and select a category from the TRM Categories page.

</td></tr><tr><td>

Type

</td><td>

Select the type of the product. The list includes:-   Software
-   Hardware

</td></tr><tr><td>

Other categories

</td><td>

An additional level of category classification of the TRM product. You can also filter for TRM products by using the values of this field.You can select multiple other category values.

</td></tr><tr><td>

New product

</td><td>

Select this check box if the product does not yet exist in the system. When selected, the **Software product** field is replaced by the **Name** field for entering the new product name.

</td></tr><tr><td>

Requested TRM phase

</td><td>

Phase of the product. Look up and select a phase from the TRM Phases page. This field is required.

</td></tr><tr><td>

Software product

</td><td>

Name of the software product. This field appears and is required when **Software** is selected in the **Type** field and the **New product** check box is not selected. This field is available when the Software Asset Management Foundation plugin plugin is installed on your instance.

</td></tr><tr><td>

Operating system

</td><td>

The operating system on which the TRM product can be deployed. This field appears only when **Software** is selected in the **Type** field.

</td></tr><tr><td>

Hardware product

</td><td>

Name of the hardware product. This field appears and is required when **Hardware** is selected in the **Type** field. This field is available when the Hardware Asset Management plugin is installed on your instance.

</td></tr><tr><td>

Business Justification

</td><td>

Business justification for the product request.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture Workspace reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-reference.md)

**Related topics**  


[Request a TRM product in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-request-a-trm-products.md)

