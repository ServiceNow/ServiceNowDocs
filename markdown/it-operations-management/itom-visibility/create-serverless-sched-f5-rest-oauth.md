---
title: Create a serverless schedule for F5 BIG-IP REST OAuth 2.0 authentication-based discovery
description: Create a serverless discovery schedule to discover F5 BIG-IP load balancers through REST OAuth 2.0 authentication \(tokens\).
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [F5 BIG-IP, Load balancers, Network device discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Create a serverless schedule for F5 BIG-IP REST OAuth 2.0 authentication-based discovery

Create a serverless discovery schedule to discover F5 BIG-IP load balancers through REST OAuth 2.0 authentication \(tokens\).

## Before you begin

-   Verify you have the IP address for the F5 BIG-IP load balancer.
-   Create a basic authentication credential. For more information, see [Basic authentication credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_BasicAuthCredentialsForm.md).
-   Create a alias for the basic authentication credential. For more information, see [Credential aliases for Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/discovery-credential-alias.md).

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
        |Pattern|Pattern to be used for this schedule, which should be the F5 REST OAuth 2.0 authentication pattern.|
        |Proxy Host|Fully qualified domain name of the machine on which you’re installing the proxy server, which should be Global.|
        |Active|Enables this schedule for discovery.|

    4.  Select **Submit**.

4.  Set the pattern launcher parameters.

    1.  In the **Discovery Pattern Launcher Parameters** tab, select the record you created.

    2.  On the form, fill in the fields.

        |Parameter|Value|
        |---------|-----|
        |ip\_address|IP address of the F5 BIG-IP load balancer.|
        |credential\_alias|Name of the credential alias you created.|

    3.  Select **Submit**.


## What to do next

Either execute discovery immediately by selecting **Discover now** or wait until the predefined schedule triggers the discovery.

**Parent Topic:**[F5 BIG-IP load balancer discovery](../../discovery/concept/c_LoadBalancerF5BIGIP.md)

