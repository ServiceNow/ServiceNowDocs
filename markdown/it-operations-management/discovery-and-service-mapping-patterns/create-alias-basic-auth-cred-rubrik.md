---
title: Create a basic authentication credential alias for Rubrik discovery
description: Create an alias and add it to a basic authentication credential to discover Rubrik clusters.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/create-alias-basic-auth-cred-rubrik.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 1
breadcrumb: [Rubrik Cluster, Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Create a basic authentication credential alias for Rubrik discovery

Create an alias and add it to a basic authentication credential to discover Rubrik clusters.

## Before you begin

Confirm that a basic authentication account is configured with the Read-Only Administrator role in Rubrik.

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

        For more information, see [Basic authentication credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/r_BasicAuthCredentialsForm.md).

    6.  Select **Submit**.


## What to do next

Create a serverless discovery schedule. For more information, see [Create a serverless discovery schedule for Rubrik cluster discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/create-serverless-schedule-rubrik.md).

**Parent Topic:**[Rubrik Cluster discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/rubrik-discovery.md)

**Related topics**  


[Rubrik Cluster discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/rubrik-discovery.md)

