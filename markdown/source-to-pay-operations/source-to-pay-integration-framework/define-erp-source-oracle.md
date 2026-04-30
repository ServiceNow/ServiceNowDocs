---
title: Define ERP source configuration for Oracle EBS
description: ERP source configuration determines the ERP source to which your ERP system connects. Map the integration payload with the Oracle EBS tables.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Source-to-Pay integration with Oracle EBS, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Define ERP source configuration for Oracle EBS

ERP source configuration determines the ERP source to which your ERP system connects. Map the integration payload with the Oracle EBS tables.

## Before you begin

Role required: sn\_shop.procurement\_administrator

## About this task

By default, the base system includes one ERP source named Oracle EBS, which refers to the parent connection for Oracle EBS. If there are multiple Oracle EBS instances, multiple ERP sources must be configured, and the child connections for these Oracle EBS instances should be referenced.

Each ERP instance requires a unique ERP source configuration. Therefore, 10 ERP instances need 10 configurations.

## Procedure

1.  Navigate to **All** &gt; **Finance – ERP Integration** &gt; **ERP Source Configuration**.

2.  In the ERP Configurations view, select **Oracle EBS**.

    This configuration is available as a part of the base system.

3.  To edit the ERP source, select **here**.

4.  Select the required ERP source for the Oracle EBS using the search option.

5.  To create a new ERP source, perform the following steps:

    1.  Select **New**.

    2.  On the form, fill the fields.

        |Field|Description|
        |-----|-----------|
        |ERP Source|ERP source for which the integration is required. For example, Oracle EBS.|
        |Short Description|Summary of the ERP source.|
        |Active|Option to activate the ERP source.|
        |Amount Precisions|Amount precision of the ERP source. For example, 2.|

        ![Define a new ERP source configuration for Oracle EBS](../image/oracle-ebs-new-erp-source.png "Define a new ERP source configuration for Oracle EBS")

    3.  Select **Submit**.

        A new ERP source is created. Verify that the connection alias is also unique for each ERP source.

        **Note:** Oracle EBS integration can have multiple ERP sources. The Staging table displays the ERP source column, which you can use to distinguish which ERP the data belongs to.


## What to do next

By default, the Oracle EBS base system provides 13 service mappings. For other Oracle EBS instances, you need to perform the following:

-   Define service mappings manually for each integration service by accessing the Service Mappings related list. You can define element level mapping between Oracle EBS table fields and payload elements.
-   Map the users and corresponding ERP User IDs by accessing the ERP User Mappings related list.

**Parent Topic:**[Configure the Source-to-Pay integration with Oracle EBS](../concept/configuring-source-to-pay-oracle-ebs-integration.md)

**Related topics**  


[ERP source configuration for Oracle EBS](../concept/erp-source-configuration-oracle.md)

[Configure integration services for Oracle EBS](configure-service-maps-oracle-ebs.md)

[Load data to ERP user-mapping table for Oracle EBS](load-data-erp-user-mapping-oracle-ebs.md)

[Look up primary data in Oracle EBS](../concept/look-up-primary-data-oracle-ebs.md)

[Scheduled jobs to look up primary data in Oracle EBS](../concept/scheduled-jobs-to-primary-data-oracle-ebs.md)

