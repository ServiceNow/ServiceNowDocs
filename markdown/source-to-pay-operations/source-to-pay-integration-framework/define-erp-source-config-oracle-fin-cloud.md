---
title: Define ERP source configuration for Oracle Financial Cloud
description: ERP source configuration determines the ERP source to which your ERP system connects. Map the integration payload with the Oracle Financial Cloud tables.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Define ERP source configuration for Oracle Financial Cloud

ERP source configuration determines the ERP source to which your ERP system connects. Map the integration payload with the Oracle Financial Cloud tables.

## Before you begin

Role required: sn\_shop.procurement\_administrator

## About this task

By default, the base system includes one ERP source named Oracle Financial Cloud, which refers to the parent connection for Oracle Financial Cloud. If there are multiple Oracle Financial Cloud instances, multiple ERP sources must be configured, and the child connections for these Oracle Financial Cloud instances should be referenced.

Each ERP instance requires a unique ERP source configuration. Therefore, 10 ERP instances need 10 configurations.

## Procedure

1.  Navigate to **All** &gt; **Finance – ERP Integration** &gt; **ERP Source Configuration**.

2.  In the ERP Configurations view, select **Oracle Financial Cloud**.

    This configuration is available as a part of the base system.

3.  To edit the ERP source, select **here**.

4.  Select the required ERP source for the Oracle Financial Cloud using the search option.

5.  To create a new ERP source, perform the following steps:

    1.  Select **New**.

    2.  On the form, fill the fields.

        |Field|Description|
        |-----|-----------|
        |ERP Source|ERP source for which the integration is required. For example, Oracle Financial Cloud.|
        |Short Description|Summary of the ERP source.|
        |Active|Option to activate the ERP source.|
        |Amount Precisions|Amount precision of the ERP source. For example, 2.|

        ![Define a new ERP source configuration](../image/oracle-fin-new-erp-source.png "Define a new ERP source configuration")

    3.  Select **Submit**.

        A new ERP source is created. Verify that the connection alias is also unique for each ERP source.

        **Note:** Oracle Financial Cloud integration can have multiple ERP sources. The Staging table displays the ERP source column, which you can use to distinguish which ERP the data belongs to.


## What to do next

By default, the Oracle Financial Cloud base system provides five service mappings. For other Oracle Financial Cloud instances, you need to perform the following:

-   Define service mappings manually for each integration service by accessing the Service Mappings related list. You can define element level mapping between Oracle Financial Cloud table fields and payload elements.
-   Map the users and corresponding ERP User IDs by accessing the ERP User Mappings related list.

