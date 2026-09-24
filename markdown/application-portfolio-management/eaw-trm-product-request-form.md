---
title: Request TRM product form
description: The Request TRM product form is used to submit a request to add a new software or hardware product to the Technology Reference Model \(TRM\) library. Optionally, add lifecycle records as part of the same request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-trm-product-request-form.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Form field information for Enterprise Architecture Workspace, Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture]
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

Unique, auto-generated identification number for the product request.

</td></tr><tr><td>

Approval

</td><td>

Status of the approval. The available values include:-   Not yet requested
-   Requested
-   Approved
-   Rejected

</td></tr><tr><td>

Short description

</td><td>

Brief description of the product request.

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

Type of the product. The list includes:-   Software
-   Hardware

 The **Type** selection determines which product and lifecycle fields are displayed on the form.

</td></tr><tr><td>

Other categories

</td><td>

Additional level of category classification of the TRM product. You can also filter for TRM products by using the values of this field.You can select multiple other category values.

 **Note:** This field is enabled only after a value is selected in the **Category** field.

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

Name of the software product. This field appears and is required when **Software** is selected in the **Type** field and the **New product** check box is not selected. This field is available when the Basic Software Asset Management plugin is installed on your instance.

</td></tr><tr><td>

Name

</td><td>

Name of the new software product. This field appears and is required when **Software** is selected in the **Type** field and the **New product** check box is selected. This field replaces the **Software product** field.

</td></tr><tr><td>

Operating system

</td><td>

Operating system on which the TRM product can be deployed. This field appears only when **Software** is selected in the **Type** field.

</td></tr><tr><td>

Hardware product

</td><td>

Name of the hardware product. This field appears and is required when **Hardware** is selected in the **Type** field. This field is available when the Hardware Asset Management plugin is installed on your instance.

</td></tr><tr><td>

Owner

</td><td>

User responsible for the TRM product. Defaults to the logged-in user.

</td></tr><tr><td>

Business Justification

</td><td>

Business justification for the product request.

</td></tr></tbody>
</table>## TRM product lifecycles tab

Use this tab to optionally add one or more lifecycle records as part of the product request. For field information, see [Request TRM product lifecycle form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-create-trm-prod-lifecycle-req-form.md).

**Note:** The **Create lifecycle** button is enabled only after all the mandatory fields on the **TRM product lifecycles** tab are filled in.

**Parent Topic:**[Form field information for Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-form-field-information.md)

**Related topics**  


[Request a TRM product in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-request-a-trm-products.md)

[Request a TRM product lifecycle in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-request-a-trm-product-lifecycle.md)

[Create a TRM product in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-create-trm-prod-lifecycle.md)

[Create TRM product lifecycles in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-create-trm-prod-lifecycle-req.md)

[Approve or reject TRM requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-approve-trm-req.md)

