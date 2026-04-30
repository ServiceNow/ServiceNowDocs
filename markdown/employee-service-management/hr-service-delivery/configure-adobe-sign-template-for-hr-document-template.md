---
title: Configure an HR service for the Adobe Sign integration
description: Create or modify an HR service to request electronic signatures through the Adobe Sign service. A preconfigured flow to collect signatures for either an adhoc document \(HR PDF document template\) or an Adobe Sign template is available to use.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Adobe Sign service, HR Integrations, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure an HR service for the Adobe Sign integration

Create or modify an HR service to request electronic signatures through the Adobe Sign service. A preconfigured flow to collect signatures for either an adhoc document \(HR PDF document template\) or an Adobe Sign template is available to use.

## Before you begin

Role required: sn\_hr\_core.admin

## About this task

For signing an adhoc document \(HR PDF document template\) or an Adobe Sign template, the following preconfigured HR service, flow, and HR case template are available for your use.

-   Case template: Signature using Adobe sign in
-   HR service: Signature using Adobe sign in
-   Flow: Adobe Sign Integration Flow

## Procedure

1.  Configure an HR service for the Adobe Sign integration.

    1.  Navigate to **HR Administration** &gt; **HR Service Configuration**.

    2.  Click **New** or open a record.

    3.  On the HR service form, provide the following values for an adhoc document and Adobe Sign document:

        -   HR service name: Signature using Adobe sign in
        -   Fulfillment type: Flow
        -   Flow: Adobe Sign Integration Flow
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

        -   For adhoc document, make sure to select an HR PDF document template with the **Template type** field set to `HR PDF Templates`.
        -   For the Adobe Sign template, make sure to select an HR PDF document template with the **Template type** field set to `Adobe Sign Templates`.
    5.  Fill in the other fields on the form, as appropriate.

        For further details on creating an HR case template, see [Configure an HR case template](configure-hr-case-template.md).

    6.  Click **Submit**.

    7.  On the HR service form, click **Update**.


**Parent Topic:**[Integrating with the Adobe Sign service](../concept/integrating-with-adobe-sign-service.md)

