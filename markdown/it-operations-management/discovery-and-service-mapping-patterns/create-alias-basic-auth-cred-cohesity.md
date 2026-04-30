---
title: Create an alias for a basic authentication credential for Cohesity storage system discovery
description: Create an alias and add it to a basic authentication credential to discover Cohesity storage systems.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Cohesity storage system, Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create an alias for a basic authentication credential for Cohesity storage system discovery

Create an alias and add it to a basic authentication credential to discover Cohesity storage systems.

## Before you begin

Verify you have a basic authentication account configured with proper permissions. For more information, see the [Verify API permissions](../reference/cohesity-storage-system-discovery.md#cohesity-api-permissions) section in [Cohesity storage system discovery](../reference/cohesity-storage-system-discovery.md).

Role required: discovery\_admin

## Procedure

1.  Create an alias.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Select **New**.

    3.  Enter a unique name for the alias and select **Credential** for the alias type in the **Type** field.

    4.  Select **Submit**.

2.  Configure a basic authentication credential for the new alias.

    1.  Navigate to **Discovery** &gt; **Credentials**.

    2.  Select **New**.

    3.  Select **Basic Auth Credentials**.

    4.  Unlock the **Credential alias** field and select the alias you created.

    5.  Configure the rest of the **Basic Auth Credentials** form fields.

    6.  Select **Submit**.

        For more information about Basic Auth Credentials form fields, see [Basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).


## What to do next

Create a serverless discovery schedule. For more information, see [Create a serverless schedule for Cohesity storage system discovery](create-serverless-schedule-cohesity.md).

**Related topics**  


[Cohesity storage system discovery](../reference/cohesity-storage-system-discovery.md)

