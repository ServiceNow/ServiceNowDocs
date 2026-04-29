---
title: Create a serverless schedule for Cohesity storage system discovery
description: Create a serverless discovery schedule to discover Cohesity storage systems.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cohesity storage system, Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create a serverless schedule for Cohesity storage system discovery

Create a serverless discovery schedule to discover Cohesity storage systems.

## Before you begin

-   Verify the MID Server is set to Active and is reachable to Cohesity storage cluster.
-   Create an alias for the basic authentication credential. For more information, see [Create an alias for a basic authentication credential for Cohesity storage system discovery](create-alias-basic-auth-cred-cohesity.md).

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules**.

2.  Create the discovery schedule record.

    1.  Select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name for this discovery schedule.|
        |Discover|Scan type, which should be Serverless.|
        |MID server|Name of the MID Server to use for this schedule.|
        |Active|Enables this schedule for discovery.|

    3.  Select **Submit**.

3.  Create the execution pattern.

    1.  In the Discovery Schedules page, select the record you created.

    2.  In the **Serverless Execution Patterns** tab, select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Descriptive name for this record.|
        |Pattern|Pattern to be used for this schedule, which should be the Cohesity Storage System pattern.|
        |Proxy Host|Fully qualified domain name of the machine on which a proxy server is installed, when applicable. This field should be left empty.|
        |Active|Enables this schedule for discovery.|

    4.  Select **Submit**.

4.  Set the pattern launcher parameters.

    1.  In the **Discovery Pattern Launcher Parameters** tab, select the record you created.

    2.  On the form, fill in the fields.

        |Parameter|Value|
        |---------|-----|
        |cluster\_ip|The Cohesity cluster URL or IP address.|
        |credentialAlias|Name of the credential alias you created.|

    3.  Select **Submit**.


## What to do next

Either execute discovery immediately by selecting **Discover now** or wait until the predefined schedule triggers the discovery.

**Related topics**  


[Cohesity storage system discovery](../reference/cohesity-storage-system-discovery.md)

