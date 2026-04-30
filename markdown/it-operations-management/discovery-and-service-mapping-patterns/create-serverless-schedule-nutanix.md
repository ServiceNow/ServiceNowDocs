---
title: Create a serverless schedule for Nutanix Acropolis discovery
description: Create a serverless schedule to discover Nutanix Acropolis using REST API.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Nutanix Acropolis, Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create a serverless schedule for Nutanix Acropolis discovery

Create a serverless schedule to discover Nutanix Acropolis using REST API.

## Before you begin

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
        |MID server|Name of the MID Server with access to the Nutanix environment.|
        |Active|Enables this schedule for discovery.|
        |Run|Determines the run schedule of the discovery.|

    3.  Select **Submit**.

3.  Create the execution pattern.

    1.  In the Discovery Schedules page, select the record you created.

    2.  In the **Serverless Execution Patterns** tab, select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Descriptive name for this record.|
        |Pattern|Pattern to be used for this schedule, which should be Nutanix Components.|
        |Proxy Host|Fully qualified domain name \(FQDN\) of the machine where the proxy server is installed, which should be Global. This field is optional.|
        |Active|Enables this schedule for discovery.|

    4.  Select **Submit**.

4.  Set the pattern launcher parameters.

    1.  In the **Discovery Pattern Launcher Parameters** tab, select the record you created.

    2.  On the form, fill in the fields.

        |Parameter|Value|
        |---------|-----|
        |PRISM\_Address|IP Address or the FQDN associated with the Prism Central instance.|

    3.  Select **Submit**.


## What to do next

Either execute discovery immediately by selecting **Discover now** or wait until the predefined schedule triggers the discovery.

**Parent Topic:**[Nutanix Acropolis discovery](../reference/nutanix-pattern.md)

**Related topics**  


[Nutanix Acropolis discovery](../reference/nutanix-pattern.md)

