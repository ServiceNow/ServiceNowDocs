---
title: Define ERP source configuration for SAP Ariba
description: ERP source configuration determines the ERP source to which your ERP system connects. Map the integration payload with the SAP Ariba tables.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2025-06-23"
reading_time_minutes: 2
breadcrumb: [Configuring the Source-to-Pay integration with SAP Ariba, Source-to-Pay integration with SAP Ariba, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Define ERP source configuration for SAP Ariba

ERP source configuration determines the ERP source to which your ERP system connects. Map the integration payload with the SAP Ariba tables.

## Before you begin

Role required: sn\_fcms\_intg.admin

## Procedure

1.  Navigate to **All** &gt; **Finance – ERP Integration** &gt; **ERP Source Configuration**.

2.  In the ERP Configurations view, select **SAP Ariba REST**.

    This configuration is available as a part of the base system.

3.  To edit the ERP source, select **here** from the label **To edit this record click here**.

    ![Edit the ERP Source for SAP Ariba](../image/sap-ariba-edit-config.png "Edit the ERP Source for SAP Ariba")

    1.  Select the list search icon \(![List search icon](../../../common/image/List_SearchIcon.png)\) to look up the required ERP source for SAP Ariba.

    2.  In the ERP Sources dialog, use the search option to select the ERP Source for SAP Ariba.

    3.  Select **Update**.

4.  To create an ERP source, do the following:

    1.  Select **here**.

    2.  Select the list search icon \(![List search icon](../../../common/image/List_SearchIcon.png)\) to look up the required ERP source for SAP Ariba.

    3.  In the ERP Source dialog, select **New**.

        ![New ERP Source for SAP Ariba](../image/sap-ariba-new-config.png "Create an ERP Source for SAP Ariba")

    4.  On the form, fill the fields.

        |Field|Description|
        |-----|-----------|
        |ERP Source|ERP source for which the integration is required. For example, SAP Ariba.|
        |Short Description|Summary of the ERP source.|
        |Active|Option to activate the ERP source.|
        |Amount Precisions|Amount precision of the ERP source. For example, 2.|

    5.  Select **Submit**.

        A new ERP source is created. Verify whether the connection alias is unique for each ERP source.

        **Note:** SAP Ariba integration can have multiple ERP sources. The Staging table displays the ERP source column, which helps identify the ERP system associated with the data.


**Parent Topic:**[Configuring the Source-to-Pay integration with SAP Ariba](configuring-source-to-pay-sap-ariba-integration.md)

**Related topics**  


[ERP source configuration for SAP Ariba](erp-source-configuration-sap-ariba.md)

[Configure integration services for SAP Ariba](configure-service-maps-sap-ariba.md)

[Look up primary data in SAP Ariba](look-up-primary-data-sap-ariba.md)

