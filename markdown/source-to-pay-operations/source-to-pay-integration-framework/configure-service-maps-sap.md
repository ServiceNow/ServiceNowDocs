---
title: Configure integration services for SAP
description: For configuring integration services, provide the connection end point and the SAP ERP credentials that you set up for your authentication profile. Also, create a separate integration service record for each service request that you want to customize.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Source-to-Pay integration with SAP, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Configure integration services for SAP

For configuring integration services, provide the connection end point and the SAP ERP credentials that you set up for your authentication profile. Also, create a separate integration service record for each service request that you want to customize.

Configure integration services for SAP 

## Before you begin

-   Verify that the application scope is set to SAP ECC and SAP S4 HANA spoke.
-   Verify that the MID Server is installed and configured in your ServiceNow instance to connect to the ERP server. For more details, see Installing the MID Server.
-   For REST type service, REST API details, as provided by ERP.

Role required: sn\_fcms\_intg.admin

## About this task

If the application requires multiple SAP instances, create separate integration services for each ERP instance. You can create integration service records for entities using the `sn_fcms_intg_service` table.

## Procedure

1.  Navigate to **All** &gt; **Finance – ERP Integration** &gt; **ERP Source Configuration**.

2.  Open the ERP source for which you need to configure integration services.

    For example, SAP ECC or SAP S4 HANA.

3.  In the Integration Services list, select the service that you want to configure.

    ![Look up Legal Entities from SAP S4 HANA OData](../../source-to-pay-operations/image/sap-integration-full-pull.png "Look up Legal Entities from SAP S4 HANA OData")

4.  To modify the Integration service record, select **here**.

5.  On the Integration service record, fill in the fields.

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

Name of the application. For example, SAP ECC or SAP S4 HANA.

</td></tr><tr><td>

ERP Source configuration

</td><td>

The ERP source mapped to the entity. For example, SAP ECC or SAP S4 HANA.

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

 You can define the value for the properties based on your requirements. Here’s an example:

-   `filter`: `currency eq 'USD'`
-   `order_by`: `currencies`
-   `select`: `currency`
-   `page_size`: `100`
 -   **Enabling Full Pull**:

Use this property to fetch the complete data.

    -   Create a property named "`full_pull`" and set its value to `true`.
    -   Additionally, you can create another property like, "`initial_load_start_date_time`" and set its value to `2025-04-15T04:10:34`.
-   **Enabling Delta Pull**:

Use this property to fetch the incremental data.

Set the value of the "`full_pull`" property to `false`.

</td></tr><tr><td>

Order

</td><td>

Option to choose the order in which the entity should be displayed.

</td></tr></tbody>
</table>6.  Select **Update** to save the configuration changes.

    The integration service is configured for the selected entity.


**Parent Topic:**[Configure the Source-to-Pay integration with SAP](../concept/configuring-source-to-pay-sap-integration.md)

**Related topics**  


[ERP Source Configuration for SAP](../concept/erp-source-configuration-sap.md)

[Define ERP source configuration for SAP](define-erp-source-sap.md)

[Look up primary data in SAP](../concept/look-up-primary-data-sap.md)

[Manually execute flows or subflows in SAP \(Inbound\)](manually-trigger-subflows-sap.md)

[Scheduled jobs to look up primary data in SAP](../concept/scheduled-jobs-to-primary-data-sap.md)

