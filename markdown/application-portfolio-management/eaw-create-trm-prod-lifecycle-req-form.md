---
title: Request TRM product lifecycle form
description: The Request TRM product lifecycle form is used to submit a request to add one or more lifecycle records to a TRM product. After you submit the request, an email notification is sent to the Enterprise Architect group for approval.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-create-trm-prod-lifecycle-req-form.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Form field information for Enterprise Architecture Workspace, Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Request TRM product lifecycle form

The Request TRM product lifecycle form is used to submit a request to add one or more lifecycle records to a TRM product. After you submit the request, an email notification is sent to the Enterprise Architect group for approval.

## Parent lifecycle request fields

The top of the form captures the parent lifecycle request record. After you enter the details, the child lifecycle records you add in the **TRM product lifecycles** section below are created and linked to this parent request.

<table id="table_lifecycle_req_top"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

A unique, auto-generated identification number for the parent lifecycle request.

</td></tr><tr><td>

Approval

</td><td>

Status of the approval. Choices include:-   Not yet requested
-   Requested
-   Approved
-   Rejected

</td></tr><tr><td>

Short description

</td><td>

A brief description of the parent lifecycle request.

</td></tr><tr><td>

Business Justification

</td><td>

Business justification for the parent lifecycle request.

</td></tr><tr><td>

TRM product

</td><td>

Name of the existing TRM product to add lifecycles to. Look up and select the product from the TRM Products page. This field is required. The fields in the **TRM product lifecycles** section below change based on whether the selected product is a software or hardware product.

</td></tr><tr><td>

Business Application

</td><td>

Name of the business application. Look up and select a business application to associate it with the TRM product lifecycle.

</td></tr></tbody>
</table>## TRM product lifecycles section — software products

When you select a software product in the **Type** field of the Details tab, select **Add version and edition** to add lifecycle fields.

**Note:** You can add up to 5 version and edition combinations, with a maximum of 10 phases per combination.

<table id="table_lifecycle_software"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Version

</td><td>

The version of the TRM software product. This field is required.To create a TRM software product lifecycle with a wildcard, end the version with an asterisk \(\*\).

</td></tr><tr><td>

Edition

</td><td>

The edition of the TRM software product.

</td></tr><tr><td>

TRM phase

</td><td>

Phase of the product lifecycle. Look up and select a phase from the TRM Phases as defined in the Setup page \(Enterprise Architecture Workspace &gt; Setup &gt; TRM Phases\). This field is required.

</td></tr><tr><td>

Phase start date

</td><td>

Start date of the product lifecycle phase. This field is required.

</td></tr><tr><td>

Phase end date

</td><td>

End date of the product lifecycle phase.

</td></tr></tbody>
</table>## TRM product lifecycles section — hardware products

When you select a hardware product in the **Type** field of the Details tab, select **Add model** to add lifecycle fields. Adding lifecycle records is optional.

**Note:** You can add up to 5 hardware models, with a maximum of 10 phases per hardware model.

|Field|Description|
|-----|-----------|
|Hardware model|The hardware model for the lifecycle record. This field is required.|
|Model number|The model number of the hardware model. This field is automatically populated when you select a hardware model.|
|Barcode|The barcode of the hardware model. This field is automatically populated when you select a hardware model.|
|TRM phase|Phase of the product lifecycle. Look up and select a phase from the TRM Phases as defined in the Setup page \(Enterprise Architecture Workspace &gt; Setup &gt; TRM Phases\). This field is required.|
|Phase start date|Start date of the product lifecycle phase. This field is required.|
|Phase end date|End date of the product lifecycle phase.|

**Parent Topic:**[Form field information for Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-form-field-information.md)

**Related topics**  


[Create TRM product lifecycles in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-create-trm-prod-lifecycle-req.md)

[Request a TRM product lifecycle in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-request-a-trm-product-lifecycle.md)

