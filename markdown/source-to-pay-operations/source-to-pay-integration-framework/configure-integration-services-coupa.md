---
title: Configure integration services for Coupa
description: Configure integration services for Coupa. Provide the connection end point and the Coupa ERP credentials that you set up for your authentication profile. Also, create a separate web service record for each service request that you want to customize.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Source-to-Pay integration with Coupa, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Configure integration services for Coupa

Configure integration services for Coupa. Provide the connection end point and the Coupa ERP credentials that you set up for your authentication profile. Also, create a separate web service record for each service request that you want to customize.

Configure integration services for Coupa 

## Before you begin

-   Verify that the application scope is set to Coupa spoke.
-   Verify that the MID Server is installed and configured in your ServiceNow instance to connect to the ERP server. For more details, see [Installing the MID Server](https://www.servicenow.com/docs/access?context=mid-server-installation&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

    **Note:** The MID Server integration is required only for a Coupa integration using SOAP services.

-   For REST type service, REST API details, as provided by ERP.

Role required: admin

## About this task

If the application requires multiple Coupa ERP instances, create separate web services for each ERP instance. You can create Integration Service records for entities using the `sn_fcms_intg_service` table.

## Procedure

1.  Navigate to **All** &gt; **Finance – ERP Integration** &gt; **ERP Source Configuration**.

2.  Open the ERP source for which you need to configure Integration services.

    For example, Coupa.

3.  In the Integration Services list, select the service that you want to configure.

    ![Look up Legal Entities from Coupa](../../source-to-pay-operations/image/coupa-fulllpull.png "Look up Legal Entities from Coupa")

4.  On the integration service record, fill in the fields.

<table id="table_ygn_3bx_y2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity

</td><td>

Type of entity for which you want to configure the integration service.

</td></tr><tr><td>

Application

</td><td>

Name of the application. For example, Coupa.

</td></tr><tr><td>

ERP Source configuration

</td><td>

The ERP source mapped to the entity. For example, Coupa.

</td></tr><tr><td>

Active

</td><td>

Option to activate the interaction service. By default, the service is inactive.

</td></tr><tr><td>

Subflow

</td><td>

Subflow used to fetch primary data.

</td></tr><tr><td>

Properties

</td><td>

Properties of the service.

 The property creates a JSON record in the integration service, which is then passed to the ERP subflows to retrieve complete data.

 To pass JSON into the subflow, create a property named "query" and assign it a JSON query as its value, like this:

```
[
  {
    "parameter": "LEGAL_ENTITY_NAME",
    "operator": "=",
    "value": "Vision ADB",
    "operand": "NONE"
  }
]
```

 -   **Enabling Full Pull**:

Create a property named "`full_pull`" and set its value to `true`

-   **Enabling Delta Pull**:

Use this property to fetch the incremental data.

Set the value of the "`full_pull`" property to `false`.

</td></tr><tr><td>

Order

</td><td>

Order in which the entity should be displayed.

</td></tr></tbody>
</table>5.  Select **Update**.


**Parent Topic:**[Configure Source-to-Pay integration with Coupa](../concept/configuring-source-to-pay-coupa-integration.md)

**Related topics**  


[ERP Source Configuration for Coupa](../concept/erp-source-configuration-coupa.md)

[Define an ERP source configuration for Coupa](define-erp-source-coupa.md)

[Activate the schedule flows](activate-schedule-flows-coupa.md)

[Looking up primary data in Coupa](../concept/look-up-primary-data-coupa.md)

