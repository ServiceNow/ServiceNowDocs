---
title: Create a serverless discovery schedule for IBM Flash System discovery
description: Create a serverless discovery schedule to run IBM Flash System storage discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/create-serverless-schedule-ibm-flash.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [IBM Flash System, Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create a serverless discovery schedule for IBM Flash System discovery

Create a serverless discovery schedule to run IBM Flash System storage discovery.

## Before you begin

-   Verify that the MID Server is active and can reach the following REST API endpoints on the IBM Flash System array:

    -   `POST /rest/v1/auth`
    -   `POST /rest/v1/lssystem`
    -   `POST /rest/v1/lsmdiskgrp`
    -   `POST /rest/v1/lsvdisk`
    -   `POST /rest/v1/lsportfc`
    -   `POST /rest/v1/lsenclosurecanister`
    -   `POST /rest/v1/lsdrive`
    -   `POST /rest/v1/lsfabric`
-   Create an alias for a basic authentication credential. For more information, see [Create an alias for a basic authentication credential for IBM Flash System discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/create-alias-basic-auth-cred-ibm-flash.md).
-   Verify that you have at least version 1.35.0 of Discovery and Service Mapping Patterns.
-   Retrieve the following values from your IBM Flash System array:
    -   Management IP address
    -   REST API port \(typically 7443\)

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Discovery Schedules**.

2.  Create the discovery schedule record.

    1.  Select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name for this discovery schedule.|
        |Discover|Scan type, which should be `Serverless`.|
        |MID server|Name of the MID Server to use for this schedule.|
        |Active|Option to enable this schedule for discovery.|

    3.  Select **Submit**.

3.  Create the execution pattern.

    1.  In the Discovery Schedules page, select the record you created.

    2.  In the **Serverless Execution Patterns** tab, select **New**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Descriptive name for this record.|
        |Pattern|Pattern to use for this schedule, which should be `IBM Flash System Storage`.|
        |Proxy Host|Fully qualified domain name of the machine on which a proxy server is installed, when applicable. Leave this field empty.|
        |Active|Option to enable this schedule for discovery.|

    4.  Select **Submit**.

4.  Set the pattern launcher parameters.

    1.  In the **Discovery Pattern Launcher Parameters** tab, select the record you created.

    2.  On the form, fill in the fields.

        |Parameter|Value|
        |---------|-----|
        |**credential\_alias**|ID of the credential alias you created.|
        |**ipaddress**|Management IP of the IBM Flash System array.|
        |**port**|REST API port of the IBM Flash System array.|

    3.  Select **Submit**.


## What to do next

Either execute discovery immediately by selecting **Discover now** or wait until the predefined schedule triggers the discovery.

**Parent Topic:**[IBM Flash System pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/ibm-flash-system-pattern.md)

**Related topics**  


[IBM Flash System pattern-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/ibm-flash-system-pattern.md)

