---
title: Configure integration services for SAP Ariba
description: For configuring integration services, provide the connection end point and the SAP Ariba credentials that you set up for your authentication profile. Also, create a integration service record for each entity you want to customize.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Source-to-Pay integration with SAP Ariba, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Configure integration services for SAP Ariba

For configuring integration services, provide the connection end point and the SAP Ariba credentials that you set up for your authentication profile. Also, create a integration service record for each entity you want to customize.

## Before you begin

Role required: sn\_fcms\_intg.admin

## About this task

If the application requires multiple SAP Ariba instances, create separate entities for each ERP instance. You can create integration service records for entities using the `sn_fcms_intg_service` table.

## Procedure

1.  Navigate to **All** &gt; **Finance – ERP Integration** &gt; **ERP Source Configuration**.

2.  Open the ERP source for which you must configure integration services.

    For example, select SAP Ariba REST.

3.  In the Integration Services list, select the service that you want to configure.

    For example, select **Invoices**.

4.  To edit the ERP source, select **here** from the label **To edit this record click here**.

5.  On the integration service record, update the fields to modify the configurations.

<table id="table_ygn_3bx_y2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity

</td><td>

The type of entity for which you want to configure the integration service.

</td></tr><tr><td>

Application

</td><td>

Name of the application. For example, Primary Data Integration with SAP Ariba.

</td></tr><tr><td>

ERP Source configuration

</td><td>

The ERP source mapped to the entity. For example, SAP Ariba.

</td></tr><tr><td>

Active

</td><td>

The status of the interaction service. By default, the check box is inactive.

</td></tr><tr><td>

Subflow

</td><td>

The subflow used to fetch primary data.

</td></tr><tr><td>

Properties

</td><td>

Creates a JSON record in the integration service, which is then passed to the ERP subflows to retrieve complete data.

 To pass JSON into the subflow, create a property named "query" and assign it a JSON query as its value, like this:

```
[
  {
    "page_size”: “5”,
    "supplier_network_id": "AN01000000001",
    "system_Id": "ServiceNow3",
    "source_system": "SAP Ariba Network"
  }
]
```

</td></tr><tr><td>

Order

</td><td>

The order in which the entity should be displayed.

</td></tr></tbody>
</table>6.  Select **Submit**.

    The integration service is configured for the selected entity.


**Parent Topic:**[Configure the Source-to-Pay integration with SAP Ariba](configuring-source-to-pay-sap-ariba-integration.md)

**Related topics**  


[ERP source configuration for SAP Ariba](erp-source-configuration-sap-ariba.md)

[Define ERP source configuration for SAP Ariba](../task/define-erp-source-sap-ariba.md)

[Look up primary data in SAP Ariba](look-up-primary-data-sap-ariba.md)

