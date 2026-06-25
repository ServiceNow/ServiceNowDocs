---
title: Create a serverless discovery schedule for NetApp SolidFire discovery
description: Set up a dedicated serverless discovery schedule for NetApp SolidFire cluster and node discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/create-serverless-schedule-solidfire.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-05-31"
reading_time_minutes: 2
breadcrumb: [NetApp SolidFire storage system, Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create a serverless discovery schedule for NetApp SolidFire discovery

Set up a dedicated serverless discovery schedule for NetApp SolidFire cluster and node discovery.

## Before you begin

-   Verify the MID Server is set to Active and can reach the target NetApp SolidFire cluster.
-   Create an alias for the basic authentication credential. For more information, see [Create a basic authentication credential alias for NetApp SolidFire discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/create-alias-basic-auth-cred-solidfire.md).
-   Obtain the management IP address of the target SolidFire cluster.

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules**.

2.  Create the discovery schedule record.

    1.  Select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name for this discovery schedule. For example, `Discover SolidFire`.|
        |Discover|Scan type. Select **Serverless**.|
        |MID server|Name of the MID Server to use for this schedule.|
        |Active|When selected, activates this schedule for discovery runs.|

    3.  Select **Submit**.

3.  Create the execution pattern.

    1.  In the Discovery Schedules page, select the record you created.

    2.  In the **Serverless Execution Patterns** tab, select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Descriptive name for this record.|
        |Pattern|Pattern to use for this schedule. Select the NetApp SolidFire Storage System pattern.|
        |Active|When selected, activates this schedule for discovery runs.|

    4.  Select **Submit**.

4.  Set the pattern launcher parameters.

    1.  In the **Discovery Pattern Launcher Parameters** tab, select the record you created.

    2.  On the form, fill in the fields.

        |Parameter|Value|
        |---------|-----|
        |**cluster\_ip**|Management IP address of the SolidFire cluster.|
        |**credentialsAlias**|ID of the credential alias you created for the SolidFire basic authentication credential record.|

    3.  Select **Submit**.


## What to do next

Either execute discovery immediately by selecting **Discover now** or wait until the predefined schedule triggers the discovery.

**Parent Topic:**[NetApp SolidFire storage system discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/solidfire-storage-pattern.md)

**Related topics**  


[NetApp SolidFire storage system discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/solidfire-storage-pattern.md)

