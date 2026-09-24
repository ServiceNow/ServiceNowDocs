---
title: Request TRM Product Lifecycle form
description: The Request TRM Product Lifecycle form is used to submit a request from the service catalog to add one or more lifecycle records to an existing TRM product.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/trm-product-lifecycle-request-form.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Form field information for Enterprise Architecture Workspace, Enterprise Architecture Workspace reference, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Request TRM Product Lifecycle form

The Request TRM Product Lifecycle form is used to submit a request from the service catalog to add one or more lifecycle records to an existing TRM product.

## TRM Product Lifecycle Request form fields

|Field|Description|
|-----|-----------|
|Short description|Brief description of the product lifecycle request.|
|Business Justification|Business justification for the product lifecycle request.|
|TRM Product|Name of the TRM product to add lifecycles to. Look up and select the product from the TRM Products page. This field is required.|
|Business Application|Name of the business application. Look up and select a business application to associate it with the TRM product lifecycle.|

## TRM product lifecycles section — software products

The **TRM product lifecycles** section appears after you select a TRM software product in the **TRM Product** field. Select **Add** to open the **Add Row** dialog and add a lifecycle record.

|Field|Description|
|-----|-----------|
|Version|Version of the software product. This field is required. To use a wildcard, end the version with an asterisk \(\*\).|
|Edition|Edition of the software product.|
|TRM phase|Phase of the product lifecycle. Look up and select a phase from the TRM Phases page. This field is required.|
|Phase start date|Start date of the product lifecycle phase. This field is required.|
|Phase end date|End date of the product lifecycle phase.|

## TRM product lifecycles section — hardware products

The **TRM product lifecycles** section appears after you select a TRM hardware product in the **TRM Product** field. Select **Add** to open the **Add Row** dialog and add a lifecycle record.

|Field|Description|
|-----|-----------|
|Hardware Model|Hardware model for the lifecycle record. This field is required.|
|Model number|Model number of the hardware model. This field is automatically populated when you select a hardware model.|
|Barcode|Barcode of the hardware model. This field is automatically populated when you select a hardware model.|
|TRM Phase|Phase of the product lifecycle. Look up and select a phase from the TRM Phases page. This field is required.|
|Phase start|Start date of the product lifecycle phase. This field is required.|
|Phase end|End date of the product lifecycle phase.|

**Parent Topic:**[Form field information for Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/eaw-form-field-information.md)

**Related topics**  


[Request a TRM product lifecycle from the service catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/add-edit-trm-lifecycle-req.md)

[Request a TRM product from the service catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/add-edit-trm-prod-req.md)

[Request TRM Product form the Service Catalog form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/trm-prod-req-catalog-form.md)

