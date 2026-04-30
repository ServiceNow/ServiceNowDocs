---
title: Define ERP source configuration for SAP
description: ERP source configuration determines the ERP source to which your ERP system connects. Map the integration payload with the SAP tables.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Source-to-Pay integration with SAP, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Define ERP source configuration for SAP

ERP source configuration determines the ERP source to which your ERP system connects. Map the integration payload with the SAP tables.

Define ERP source configuration for SAP. 

## Before you begin

Role required: sn\_fcms\_intg.admin

## About this task

By default, the base system includes one ERP source named SAP, which refers to the parent connection for SAP. If there are multiple SAP instances, multiple ERP sources must be configured, and the child connections for these SAP instances should be referenced.

Each ERP instance requires a unique ERP source configuration. Therefore, 10 ERP instances need 10 configurations.

## Procedure

1.  Navigate to **All** &gt; **Finance – ERP Integration** &gt; **ERP Source Configuration**.

2.  In the ERP Configurations view, select one of the following ERP source configurations based on your requirement:

    -   **SAP ECC ERP**
    -   **SAP S4 HANA Cloud**
    -   **SAP S4 HANA OData**
    This configuration is available as a part of the base system.

3.  To edit the ERP source, select **here**.

4.  Select the required ERP source for the SAP ECC or SAP S4 HANA using the search option.

5.  To create a new ERP source, perform the following steps:

    1.  Select **New**.

    2.  On the form, fill the fields.

        |Field|Description|
        |-----|-----------|
        |ERP Source|ERP source for which the integration is required. For example, SAP ECC or SAP S4 HANA.|
        |Short Description|Summary of the ERP source.|
        |Active|Option to activate the ERP source.|
        |Amount Precisions|Amount precision of the ERP source. For example, 2.|

        ![Define a new ERP source configuration for S4 HANA OData](../image/sap-integration-new-erp-source.png "Define a new ERP source configuration for S4 HANA OData")

    3.  Select **Submit**.

        A new ERP source is created. Verify that the connection alias is also unique for each ERP source.

        **Note:** SAP integration can have multiple ERP sources. The Staging table displays the ERP source column, which you can use to distinguish which ERP the data belongs to.


## What to do next

By default, the SAP base system provides 14 integration services. For other SAP instances, you must perform the following:

-   To modify each integration service, you can open the integration service and select **here** to. You can define element level mapping between SAP table fields and payload elements.
-   Map the users and corresponding ERP User IDs by accessing the ERP User Mappings related list.

**Parent Topic:**[Configure the Source-to-Pay integration with SAP](../concept/configuring-source-to-pay-sap-integration.md)

**Related topics**  


[ERP Source Configuration for SAP](../concept/erp-source-configuration-sap.md)

[Configure integration services for SAP](configure-service-maps-sap.md)

[Look up primary data in SAP](../concept/look-up-primary-data-sap.md)

[Manually execute flows or subflows in SAP \(Inbound\)](manually-trigger-subflows-sap.md)

[Scheduled jobs to look up primary data in SAP](../concept/scheduled-jobs-to-primary-data-sap.md)

