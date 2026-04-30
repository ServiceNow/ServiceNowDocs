---
title: Configure an HR service for the DocuSign integration
description: Create or modify an HR service to request electronic signatures through the DocuSign service. Preconfigured flows to collect signatures for either an ad hoc document \(HR PDF document template\) or a DocuSign template are available to use. You must also configure an associated HR case template to set a default ad hoc document or DocuSign template for signing.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrating with the DocuSign service, HR Integrations, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure an HR service for the DocuSign integration

Create or modify an HR service to request electronic signatures through the DocuSign service. Preconfigured flows to collect signatures for either an ad hoc document \(HR PDF document template\) or a DocuSign template are available to use. You must also configure an associated HR case template to set a default ad hoc document or DocuSign template for signing.

## Before you begin

Role required: sn\_hr\_core.admin

## About this task

Depending on whether the user is signing an ad hoc document \(HR PDF document template\) or a DocuSign template, the following preconfigured HR services, flows, and HR case templates are available for your use and example. See [HR services](../concept/hr-service-administration.md) to learn more about HR service configuration, generally.

|Flow|Component|Name|
|----|---------|----|
|Ad hoc document flow|HR service|Request Signature using DocuSign on Adhoc Document|
|Flow|DocuSign Integration Flow - Adhoc Document|
|HR case template|Signature using DocuSign on Adhoc Document|
|DocuSign template flow|HR service|Request Signature using DocuSign Template|
|Flow|DocuSign Integration - DocuSign Template|
|HR case template|Signature using DocuSign Template|

## Procedure

1.  Configure an HR service for the DocuSign integration.

    1.  Navigate to **HR Administration** &gt; **HR Service Configuration**.

    2.  Click **New** or open a record.

    3.  On the HR service form, provide the following values.

        |Flow|Field|Value|
        |----|-----|-----|
        |Ad hoc document flow|HR service name|&lt;Name of the HR service&gt;|
        |Fulfillment type|Flow|
        |Flow|DocuSign Integration Flow - Adhoc Document|
        |DocuSign template flow|HR service name|&lt;Name of the HR service&gt;|
        |Fulfillment type|Flow|
        |Flow|DocuSign Integration - DocuSign Template|

    4.  Fill in the other fields on the form, as appropriate.

        For further details on creating an HR service, see [Configure an HR service](configure-hr-service.md).

        **Note:** In the HR Service Additional Information related list, make sure that the **PDF Template** field is included so that it appears on the HR case form when a request for this service is made. See [Configure the HR case form for an HR service](configure-case-form-for-hr-service.md#) for more information.

    5.  Right-click the form header and click **Save**.

2.  Configure an accompanying HR case template.

    1.  In the **Template** field, click the Lookup icon.

    2.  In the **HR Templates** list, click **New** or open a record.

    3.  From the **Add fields** list, select **PDF Template.**

    4.  In the **PDF Template** field, select the HR PDF document template that you want to make available for signing.

        **Note:**

        -   For the ad hoc document flow, make sure to select an HR PDF document template with the **Template type** field set to `HR PDF Templates`.ake
        -   For the DocuSign template flow, make sure to select an HR PDF document template with the **Template type** field set to `DocuSign Templates`.
    5.  Fill in the other fields on the form, as appropriate.

        For further details on creating an HR case template, see [Configure an HR case template](configure-hr-case-template.md).

    6.  Click **Submit**.

    7.  On the HR service form, click **Update**.


**Parent Topic:**[Integrating with the DocuSign service](../concept/docusign-integration-for-hr.md)

