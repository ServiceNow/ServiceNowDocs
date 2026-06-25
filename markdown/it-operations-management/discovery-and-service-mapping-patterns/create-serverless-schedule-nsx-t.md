---
title: Create a serverless schedule for NSX-T cluster discovery
description: Create a serverless discovery schedule to run the NSX Cluster pattern against a VMware NSX-T management cluster.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/create-serverless-schedule-nsx-t.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-05-03"
reading_time_minutes: 2
breadcrumb: [VMware NSX-T cluster, Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create a serverless schedule for NSX-T cluster discovery

Create a serverless discovery schedule to run the NSX Cluster pattern against a VMware NSX-T management cluster.

## Before you begin

-   Verify that you have at least version 1.31.0 of Discovery and Service Mapping Patterns.
-   Verify that you have the IP address of the NSX-T management cluster.
-   Create a credential alias with an applicative credential. For more information, see [Create an applicative credential alias for NSX-T cluster discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/create-applicative-cred-alias-nsx-t.md).

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules**.

2.  Create the discovery schedule record.

    1.  Select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name for this discovery schedule.|
        |Discover|Scan type for this schedule. Select **Serverless**.|
        |MID server|Name of the MID Server to use for this schedule.|
        |Active|Setting that activates this schedule for discovery.|

    3.  Select **Submit**.

3.  Create the execution pattern.

    1.  In the Discovery Schedules page, select the record you created.

    2.  In the **Serverless Execution Patterns** tab, select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Descriptive name for this record.|
        |Pattern|Pattern for this schedule. Select the NSX Cluster pattern.|
        |Proxy Host|Fully qualified domain name of the proxy server host. Select **Global**.|
        |Active|Setting that activates this schedule for discovery.|

    4.  Select **Submit**.

4.  Set the pattern launcher parameters.

    1.  In the **Discovery Pattern Launcher Parameters** tab, select the record you created.

    2.  On the form, fill in the fields.

        |Parameter|Value|
        |---------|-----|
        |ip\_address|IP address of the NSX-T management cluster.|
        |cred\_alias|Name of the credential alias you created.|

    3.  Select **Submit**.


## What to do next

Either execute discovery immediately by selecting **Discover now** or wait until the predefined schedule triggers the discovery.

**Parent Topic:**[VMware NSX-T cluster pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/nsx-t-cluster-pattern.md)

**Related topics**  


[VMware NSX-T cluster pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/nsx-t-cluster-pattern.md)

