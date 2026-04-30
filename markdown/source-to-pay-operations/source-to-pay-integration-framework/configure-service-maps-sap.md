---
title: Configure integration services for SAP ECC and SAP S4 HANA
description: For configuring integration services, provide the connection end point and the SAP ECC and SAP S4 HANA ERP credentials that you set up for your authentication profile. Also, create a separate integration service record for each service request that you want to customize.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2025-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring the SAP ECC and SAP S4 HANA integration, Source-to-Pay integration with SAP ECC and SAP S4 HANA, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Configure integration services for SAP ECC and SAP S4 HANA

For configuring integration services, provide the connection end point and the SAP ECC and SAP S4 HANA ERP credentials that you set up for your authentication profile. Also, create a separate integration service record for each service request that you want to customize.

## Before you begin

-   Verify that the application scope is set to SAP ECC and SAP S4 HANA spoke.
-   Verify that the MID Server is installed and configured in your ServiceNow instance to connect to the ERP server. For more details, see [Installing the MID Server](https://www.servicenow.com/docs/access?context=mid-server-installation&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
-   For REST type service, REST API details, as provided by ERP.

Role required: sn\_fcms\_intg.admin

## About this task

If the application requires multiple SAP ECC and SAP S4 HANA ERP instances, create separate integration services for each ERP instance. You can create integration service records for entities using the `sn_fcms_intg_service` table.

## Procedure

1.  Navigate to **All** &gt; **Finance – ERP Integration** &gt; **ERP Source Configuration**.

2.  Open the ERP source for which you need to configure integration services.

    For example, SAP ECC or SAP S4 HANA.

3.  In the Integration Services list, select the service that you want to configure.

    ![Look up Legal Entities from SAP S4 HANA OData](../image/sap-integration-full-pull.png "Look up Legal Entities from SAP S4 HANA OData")

4.  On the integration service record, fill in the fields.

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
</table>5.  Select **Submit**.


**Parent Topic:**[Configuring the Source-to-Pay integration with SAP ECC and SAP S4 HANA](../concept/configuring-source-to-pay-sap-integration.md)

**Related topics**  


[ERP Source Configuration for SAP ECC and SAP S4 HANA](../concept/erp-source-configuration-sap.md)

[Define ERP source configuration for SAP ECC and SAP S4 HANA](define-erp-source-sap.md)

[Look up primary data in SAP ECC and SAP S4 HANA](../concept/look-up-primary-data-sap.md)

[Manually trigger flows or subflows in SAP ECC and SAP S4 HANA \(Inbound\)](manually-trigger-subflows-sap.md)

[Scheduled jobs to look up primary data in SAP ECC and SAP S4 HANA](../concept/scheduled-jobs-to-primary-data-sap.md)

