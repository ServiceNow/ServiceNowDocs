---
title: Define an ERP source configuration for Coupa
description: Define an ERP source configuration that specifies the Coupa ERP source to which the ERP system connects. Map the integration payload with the Coupa tables.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Source-to-Pay integration with Coupa, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Define an ERP source configuration for Coupa

Define an ERP source configuration that specifies the Coupa ERP source to which the ERP system connects. Map the integration payload with the Coupa tables.

## Before you begin

Role required: admin

## About this task

By default, the base system includes one ERP source named Coupa, which refers to the parent connection for Coupa. If there are multiple Coupa instances, multiple ERP sources must be configured, and the child connections for these Coupa instances should be referenced.

Each ERP instance requires a unique ERP source configuration. For example, 10 ERP instances need 10 configurations.

## Procedure

1.  Navigate to **All** &gt; **Finance – ERP Integration** &gt; **ERP Source Configuration**.

2.  In the ERP Configurations view, select **Coupa**.

    This configuration is available as a part of the base system.

3.  To edit the ERP source, select **here**.

4.  Select the required ERP source for Coupa using the search option.

5.  To create a new ERP source, perform the following steps:

    1.  Select **here**.

    2.  Select the list search icon \(![List search icon](../../../common/image/List_SearchIcon.png)\).

    3.  Look up the required ERP source for Coupa.

    4.  In the ERP Source dialog, select **New**.

    5.  On the form, fill the fields.

        |Field|Description|
        |-----|-----------|
        |ERP Source|ERP source for which the integration is required. For example, Coupa.|
        |Short Description|Summary of the ERP source.|
        |Active|Option to activate the ERP source.|
        |Amount Precisions|Amount precision of the ERP source. For example, 2.|

        ![Define a new ERP source configuration for Coupa](../image/coupa-new-erp-source.png "Define a new ERP source configuration for Coupa")

    6.  Select **Submit**.

    A new ERP source is created. Verify that the connection alias is also unique for each ERP source.

    **Note:** Coupa integration can have multiple ERP sources. The Staging table displays the ERP source column, which you can use to distinguish which ERP the data belongs to.


## What to do next

By default, services mapping are provided for the Coupa base system. For other Coupa instances, you must perform the following steps:

-   Define service mappings manually for each integration service by accessing the Service Mappings related list. You can define element level mapping between Coupa table fields and payload elements.
-   Map the users and corresponding ERP User IDs by accessing the ERP User Mappings related list.

**Parent Topic:**[Configure Source-to-Pay integration with Coupa](../concept/configuring-source-to-pay-coupa-integration.md)

**Related topics**  


[ERP Source Configuration for Coupa](../concept/erp-source-configuration-coupa.md)

[Configure integration services for Coupa](configure-service-maps-coupa.md)

[Activate the schedule flows](activate-schedule-flows-coupa.md)

[Looking up primary data in Coupa](../concept/look-up-primary-data-coupa.md)

