---
title: Create a serverless schedule for Fortinet firewall REST-based discovery
description: Create a serverless discovery schedule to discover Fortinet firewalls and FortiGate Virtual Domains \(VDOMs\) through REST-based discovery.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Fortinet firewall and FortiGate VDOM REST-based, Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create a serverless schedule for Fortinet firewall REST-based discovery

Create a serverless discovery schedule to discover Fortinet firewalls and FortiGate Virtual Domains \(VDOMs\) through REST-based discovery.

## Before you begin

-   Verify you have the IP address for the Fortinet firewall device.
-   Create an alias for the API key credential. For more information, see [Create an alias for the API key credential for Fortinet firewall REST-based discovery](create-alias-api-key-cred-fortinet.md).

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
        |Pattern|Pattern to be used for this schedule, which should be the Next Generation Fortinet Network Firewall - REST pattern.|
        |Proxy Host|Fully qualified domain name of the machine on which you’re installing the proxy server, which should be Global.|
        |Active|Enables this schedule for discovery.|

    4.  Select **Submit**.

4.  Set the pattern launcher parameters.

    1.  In the **Discovery Pattern Launcher Parameters** tab, select the record you created.

    2.  On the form, fill in the fields.

        |Parameter|Value|
        |---------|-----|
        |ip\_address|IP address of the firewall device.|
        |credentialsAlias|Name of the credential alias you created.|

    3.  Select **Submit**.


## What to do next

Either execute discovery immediately by selecting **Discover now** or wait until the predefined schedule triggers the discovery.

**Related topics**  


[Fortinet firewall and FortiGate VDOM REST-based discovery](../reference/fortinet-fw-vdoms-rest-discovery.md)

